# Social Media Archive

Published social content archive. One file per publishing session.

## Structure
_social/
  YYYY-MM/
    YYYY-MM-DD-topic.md

## File Format
Each file uses this front matter:

```
---
date: YYYY-MM-DD
platforms: [twitter, facebook, instagram, threads, bluesky]
status: published
late_scheduled: YYYY-MM-DDTHH:MM:SS
---
```

## Rules
- Commit AFTER Late confirms scheduled — not before
- Drafts do not belong here
- One commit per publishing session
