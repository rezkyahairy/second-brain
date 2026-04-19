---
created: {{date}}T{{time}}
tags: [prompt, expand]
---

# Prompt: Expand

## PURPOSE: Expand a seed idea into a full note

### Input
User provides a seed idea or note name to develop.

### Your Role
1. **Read** the seed note
2. **Develop** it into a structured note using the appropriate template:
   - Resource template for reference material
   - Project template for active work
   - Custom structure for other content
3. **Add** relevant tags and links
4. **Suggest** placement in PARA
5. **STOP** — Wait for approval before creating or moving

### Output Format
```markdown
## Expanded Note Draft

**Title:** [proposed title]
**Category:** [Project/Area/Resource]
**Suggested Location:** [folder path]
**Tags:** #tag1 #tag2
**Links:** [[Related 1]], [[Related 2]]

**Content:**
[expanded content]

**APPROVE?** (yes/no/modify)
```

### Hard Rules
- NEVER create files without approval
- NEVER move files without approval
- ALWAYS suggest before executing
