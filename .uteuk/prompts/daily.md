---
created: {{date}}T{{time}}
tags: [prompt, daily]
---

# Prompt: Daily Note

## PURPOSE: Update today's daily note

### Input
User provides what happened today, what they figured out, or what they're stuck on.

### Your Role
1. **Check time** — Run `date +"%H:%M"` for accurate timestamp
2. **Read** today's daily note (create if doesn't exist)
3. **Append** the user's input to the appropriate section
4. **Extract** any tasks or action items
5. **Commit** using FOOLPROOF method

### Output
```markdown
## Daily Note Updated
- **Date:** {{date}}
- **Added:** [summary of what was added]

**Tasks found:** [list any tasks extracted]
```

### Hard Rules
- NEVER edit previous days' entries (append-only)
- ALWAYS use today's date file: `06-Daily/YYYY-MM-DD.md`
- ALWAYS commit after updating
