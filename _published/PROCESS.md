# Published Post Log — Process Reference

> Last updated: 2026-03-20 (Social Process Revamp)
> Location: `/volume1/docker/peptide-saas/docs-site/_published/`

---

## Purpose

The `_published/` directory is the machine-readable log of every social post we have scheduled, published, or that has failed. It is the ground truth for duplicate detection, post-publish verification, and content lineage tracking.

---

## File Structure

| File | Platform(s) |
|------|-------------|
| `twitter.csv` | Twitter/X |
| `bluesky.csv` | Bluesky (mirrors twitter.csv — Group A posts are identical) |
| `facebook.csv` | Facebook |
| `instagram.csv` | Instagram |
| `threads.csv` | Threads |
| `linkedin.csv` | LinkedIn |
| `pinterest.csv` | Pinterest |
| `reddit.csv` | Reddit |

---

## CSV Schema (Current)

```
date|post_id|platform|status|content|text_hash|campaign|topic
```

| Column | Description |
|--------|-------------|
| `date` | Scheduled publish date (`YYYY-MM-DD`) |
| `post_id` | Late/Zernio post ID, or `LATE-GAP-Xn` for reconstructed historical entries |
| `platform` | Platform name (`twitter`, `bluesky`, `facebook`, etc.) |
| `status` | `SCHEDULED`, `PUBLISHED`, or `FAILED` |
| `content` | Full post text including URL |
| `text_hash` | SHA256[:16] of normalized content (see hash function below) |
| `campaign` | Content campaign name (e.g., `gap-fill-mar26`, `q2-week14`, `evergreen`) |
| `topic` | Content topic/theme (e.g., `caregiver`, `supply-tracking`, `lab-results`) |

**Existing rows without hash/campaign/topic:** Left blank. New rows always include all fields.

---

## Hash Function

The `text_hash` column enables reliable duplicate detection. It is computed from normalized text so that minor whitespace differences don't create false negatives.

```python
import hashlib, re

def content_hash(text):
    normalized = text.lower()
    normalized = re.sub(r'https?://\S+', '', normalized)   # strip URLs
    normalized = re.sub(r'#\w+', '', normalized)            # strip hashtags
    normalized = re.sub(r'\s+', ' ', normalized).strip()   # collapse whitespace
    return hashlib.sha256(normalized.encode()).hexdigest()[:16]
```

**Shell one-liner:**
```bash
python3 -c "
import hashlib, re
def h(t):
    t=t.lower(); t=re.sub(r'https?://\S+','',t); t=re.sub(r'#\w+','',t); t=re.sub(r'\s+',' ',t).strip()
    return hashlib.sha256(t.encode()).hexdigest()[:16]
print(h('PASTE POST TEXT HERE'))
"
```

Then grep for the hash:
```bash
grep "HASH_OUTPUT" /volume1/docker/peptide-saas/docs-site/_published/twitter.csv
```

---

## Pre-Schedule Workflow (Stage 3.5 — MANDATORY)

Before scheduling any Group A (Twitter/X) post in Late:

1. Compute the `content_hash` of the post text
2. Grep for that hash in `twitter.csv`
3. Interpret result:
   - **PUBLISHED match** → Content already sent. Rewrite with a different angle.
   - **FAILED match** → Content previously failed. Twitter will reject it again. Rewrite.
   - **SCHEDULED match** → Duplicate in queue. Remove one.
   - **No match** → Clear to schedule.

---

## Log Update Workflow (Stage 4 — At Scheduling Time)

**Immediately after scheduling** each post in Late, add a SCHEDULED row:

```
YYYY-MM-DD|[late_post_id]|twitter|SCHEDULED|[full post text]|[text_hash]|[campaign]|[topic]
```

Do NOT defer this to the next morning. The log update is the commit. If the log doesn't have it, the duplicate check has no record of it.

**After all posts in a batch are scheduled:**
```bash
cd /volume1/docker/peptide-saas/docs-site
git add _published/ _social/
git commit -m "chore: schedule [week] [theme] content — N posts queued"
```

---

## Status Transitions (Automated)

The `daily-content-audit` task (5am CT daily) handles SCHEDULED → PUBLISHED/FAILED transitions:

1. Finds all SCHEDULED rows dated yesterday
2. Checks Gmail for Late failure emails (from: miki@transactional.zernio.com)
3. Posts matching a failure email → FAILED
4. All other yesterday SCHEDULED rows → PUBLISHED
5. Commits the update

The `social-compliance-check` task (Mon-Thu 6am CT) catches duplicates before they fire:
- Computes hash of every post going out in the next 48 hours
- Greps against this file
- Flags any PUBLISHED or FAILED match as CRITICAL before the post fires

---

## Campaign and Topic Tags

Use consistent values for `campaign` and `topic` columns:

**Campaign examples:**
- `gap-fill-mar26` — the March 2026 gap-fill content batch
- `gap-fill-apr08` — the April 2026 gap-fill batch
- `q2-week14` — Q2 content calendar, week 14
- `evergreen` — timeless content not tied to a campaign

**Topic examples:**
- `caregiver` — content targeting caregivers
- `supply-tracking` — medication supply management
- `lab-results` — lab result tracking features
- `pharmacy-access` — pharmacy desert / access challenges
- `adherence` — medication adherence tracking
- `cost-tracking` — medication cost / health budgets
- `health-tech` — general health technology angle
- `general` — doesn't fit a specific topic

---

## Limitations

- SHA256 hash catches exact duplicates after normalization. Substantially reworded content will not match — this is intentional (rewrites are allowed, verbatim repeats are not).
- twitter.csv rows from before 2026-03-20 may have reconstructed content (Late API truncates at ~80 chars). Post IDs `LATE-GAP-*` indicate reconstructed entries.
- daily-content-audit failure detection depends on Gmail failure emails arriving. If Late fails silently without an email, the post will be marked PUBLISHED incorrectly. Darren also receives failure emails directly, so the error is visible even if the log is wrong.

---

## Companion: _social/ Archive

The `_social/YYYY-MM/` directory is the human-readable companion to this machine-readable log. It stores the full content batch markdown files for each publishing session. These are useful for review, auditing, and context — but the CSVs in `_published/` are the source of truth for automation.
