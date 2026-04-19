---
description: Execute AI-Assisted Note-Taking Pipeline
---

> **DATE CHECK:** Use `{{date:YYYY-MM-DD}}` for current date.
> Validate: `.uteuk/skills/date-helper/DATE_CHECK.md`

Execute uteuk step: {{args}}

Available steps:
- **capture** — Capture raw idea into Inbox
- **daily** — Update today's daily note
- **expand** — Expand a seed idea into full note
- **process** — Process Inbox into PARA
- **organize** — Organize specific note
- **connect** — Find connections between notes
- **publish** — Convert draft to blog post
- **status** — Show vault dashboard report
- **weekly-review** — Full weekly audit

Each step has its own dedicated prompt in `.uteuk/prompts/`.

## Usage

```bash
/uteuk capture "Your raw idea here"
/uteuk daily "What happened today"
/uteuk expand "Note to develop"
/uteuk process
/uteuk organize "[[Note Name]]"
/uteuk connect "[[Note A]] [[Note B]]"
/uteuk publish "[[Draft Note Name]]"
/uteuk status
/uteuk weekly-review
```

## Pipeline Flow

```
CAPTURE → DAILY → EXPAND → PROCESS → ORGANIZE → CONNECT
 (Inbox) (Log)  (Develop)  (PARA)   (Structure) (Link)
   ↑
Raw ideas
```

## Hard Rules
→ See `AGENT.md` for the full list. Key reminders:
1. NEVER delete or move files without approval
2. NEVER add AI co-author to commits
3. ALWAYS use FOOLPROOF commit method — see `.uteuk/prompts/commit.md`

## Date Validation
Before creating any note:
- [ ] Fetch current date from `.uteuk/skills/date-helper/get-date.sh`
- [ ] Verify year matches internet time (not system time)
- [ ] Check `.uteuk/skills/date-helper/DATE_CHECK.md`

See `.uteuk/prompts/` for detailed step instructions.
