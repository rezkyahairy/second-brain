---
created: {{date}}T{{time}}
tags: [prompt, commit, git]
---

# Prompt: FOOLPROOF Git Commit

## PURPOSE: Commit changes without AI co-author contamination

> **Rule:** Human is the sole author. NO `Co-authored-by:` lines for AI agents.

### The Problem
AI tools may automatically inject `Co-authored-by:` lines into git commits via environment variables or tool hooks. This violates vault policy.

### The FOOLPROOF Method (ALWAYS Use This)

**Step 1:** Write commit message to temp file:
```bash
cat > /tmp/msg.txt << 'EOF'
[category]: [brief description]

- [detail if needed]
EOF
```

**Step 2:** Commit using system git:
```bash
cd ~/repo/second-brain
/usr/bin/git commit --file=/tmp/msg.txt
```

**Step 3:** Push:
```bash
/usr/bin/git push
```

### Commit Message Format
Use conventional commits:
```
daily: add 2026-04-14 log
capture: new idea about X
process: move note from Inbox to project/
project: restructure to standard layout
update: add section to template
```

Categories: `daily`, `capture`, `process`, `expand`, `organize`, `connect`, `project`, `update`, `weekly-review`

### NEVER Do This
- `git commit -m "message"` — may inject Co-authored-by
- `git commit --amend` without FOOLPROOF method
- Any commit with `--author=` override

### Hard Rules
- ALWAYS use FOOLPROOF method for every commit
- NEVER add AI co-author lines
- ALWAYS use `/usr/bin/git` not `git` (bypasses PATH overrides)
- NEVER skip git after file changes
