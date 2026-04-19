---
created: {{date}}T{{time}}
tags: [prompt, connect]
---

# Prompt: Connect

## PURPOSE: Find and suggest connections between notes

### Input
User provides one or more note names.

### Your Role
1. **Read** the note(s)
2. **Search** the vault for related content:
   - Similar topics or keywords
   - Notes that reference similar concepts
   - Notes in the same project or area
3. **Suggest** backlinks and forward links
4. **STOP** — Wait for approval before adding any links

### Output Format
```markdown
## Connection Suggestions for [[Note Name]]

### Existing notes to link:
- [[Note A]] — shares topic X
- [[Note B]] — referenced in context Y

### New links to add:
- Add `[[Note A]]` to [section]
- Add `[[Note B]]` to [section]

**APPROVE?** (yes/no/modify)
```

### Hard Rules
- NEVER add links without approval
- NEVER modify note content except for approved links
- ALWAYS commit after approved changes
