# Second Brain

A personal knowledge management system built on Obsidian, Git, and AI assistance.

## Structure

| Folder | Purpose |
|--------|---------|
| `00-Inbox/` | Raw captures — dump everything here first |
| `01-Projects/` | Active work with deadlines |
| `02-Areas/` | Ongoing responsibilities |
| `03-Resources/` | Reference material and MOCs |
| `04-Archive/` | Completed or inactive items |
| `05-Templates/` | Note templates |
| `06-Daily/` | Daily notes (append-only) |

## Workflow

1. **Capture** → dump raw ideas in `00-Inbox/`
2. **Process** → AI summarizes, finds connections, suggests placement
3. **Organize** → approve suggestions, AI moves files and adds links
4. **Express** → create blog posts, decisions, outputs from organized notes

## Setup

1. Clone this repo
2. Open in Obsidian
3. Install Obsidian Git plugin (auto-commit every 10 min)
4. Start capturing

## AI Configuration

This vault is configured for AI-assisted note-taking. Agents follow the pipeline in `AGENT.md`.

### Commands
```bash
/uteuk capture "Your raw idea here"
/uteuk process
/uteuk organize "[[Note Name]]"
/uteuk connect "[[Note A]] [[Note B]]"
/uteuk status
/uteuk weekly-review
```

### Prompts
All agent prompts live in `.uteuk/prompts/`:
- `capture.md` — Capture raw ideas
- `process.md` — Process inbox into PARA
- `organize.md` — Organize specific notes
- `connect.md` — Find connections between notes
- `expand.md` — Expand seed ideas into full notes
- `daily.md` — Update daily notes
- `publish.md` — Prepare drafts for publishing
- `status.md` — Vault dashboard
- `weekly-review.md` — Full weekly audit
- `commit.md` — FOOLPROOF git commit (no AI co-author)

### Hard Rules
- AI suggests, you decide. Never moves anything without asking.
- NEVER add AI co-author to git commits.
- ALWAYS use FOOLPROOF commit method.

## Agent-Specific Configs

- `CLAUDE.md` — Claude Code specific rules
- `QWEN.md` — Qwen Code specific rules
- `OPENCODE.md` — OpenCode specific rules
- `OPENCLAW.md` — OpenClaw specific rules

---
*Built with Obsidian + Git + AI*
