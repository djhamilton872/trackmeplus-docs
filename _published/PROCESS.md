# Published Post Log — Process Documentation

> Owner: Co C | Created: 2026-03-20
> Purpose: Ground-truth record of every social post. Eliminates duplicate content failures by giving Co C a reliable fact-based history instead of relying on memory or truncated API previews.

## Why This Exists

Twitter (X) rejects posts containing content identical or near-identical to previously published posts on the same account. Late/Zernio does not detect this at scheduling time — it only fails at the moment the post fires. Two posts failed in March 2026 (Mar 19, Mar 20) because the content had already been published. This log prevents that from happening again.

## Log Files

| File | Platform | Notes |
|------|----------|-------|
| `twitter.csv` | Twitter / X | @TrackMePlus |
| `bluesky.csv` | Bluesky | @trackmeplus.bsky.social |
| `facebook.csv` | Facebook | TrackMe+ page |
| `instagram.csv` | Instagram | @trackmeplus |
| `threads.csv` | Threads | @trackmeplus |
| `linkedin.csv` | LinkedIn | TrackMe+ company page |
| `pinterest.csv` | Pinterest | TrackMe+ account |
| `reddit.csv` | Reddit | varies by subreddit |

## Log Format

Pipe-delimited CSV. One row per post.

```
date|post_id|platform|status|content
```

- `date` — ISO 8601 date (YYYY-MM-DD) of publish or scheduled date
- `post_id` — Late post ID if scheduled/via Late, platform post ID if published directly, "DIRECT" if not via Late
- `platform` — lowercase platform name (twitter, bluesky, etc.)
- `status` — PUBLISHED | SCHEDULED | FAILED | DELETED
- `content` — Full post text (no truncation)

## Mandatory Pre-Schedule Process

Before scheduling ANY post to Twitter (X):
1. Extract the first 120 characters of the post body (stripped of hashtags and URLs)
2. `grep` against `_published/twitter.csv` for that content fragment
3. If any PUBLISHED row matches — the content has already gone out. **Rewrite before scheduling.**
4. If a SCHEDULED row matches — you're about to create a duplicate in queue. **Check if intentional or remove one.**

Same check applies to Bluesky when Group A content is identical to Twitter.

## Post-Publish Update Process

After each publishing session (daily-content-audit task handles this automatically):
- Any Late post that shows "sent" in the Late API → update status from SCHEDULED to PUBLISHED
- Any Late post that shows "failed" → update status to FAILED
- New posts scheduled via Late → add a SCHEDULED row immediately

## Git Commit Cadence

Commit this directory after every session that modifies it. One commit per publishing session.
Message format: `chore: update published post log [platform] YYYY-MM-DD`

## Headers

Each CSV file starts with this header line:
```
date|post_id|platform|status|content
```
