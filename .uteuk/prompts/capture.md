---
created: {{date}}T{{time}}
tags: [prompt, capture]
---

# Prompt: Capture

## PURPOSE: Capture a raw idea into the Inbox

### Input
User provides a raw idea or thought.

### Your Role
1. **Check time** — Run `date +"%H:%M"` for accurate timestamp
2. **Create** a new note in `00-Inbox/` with:
   - Filename: `YYYY-MM-DD - [short-title].md`
   - Frontmatter: `created`, `tags: [inbox]`
   - Body: The raw idea, preserved as-is
3. **Commit** using FOOLPROOF method

### Output
```markdown
## Captured
- **File:** 00-Inbox/YYYY-MM-DD - [title].md
- **Status:** Ready for processing

**Next:** Run `/uteuk process` when ready to organize.
```

### Hard Rules
- NEVER organize or process during capture
- NEVER modify the raw idea — preserve it exactly
- ALWAYS commit after creating the file
