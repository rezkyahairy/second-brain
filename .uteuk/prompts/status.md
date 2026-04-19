---
created: {{date}}T{{time}}
tags: [prompt, status]
---

# Prompt: Status

## PURPOSE: Show vault dashboard report

### Your Role
1. **Count** notes in each folder
2. **Identify** unprocessed inbox items
3. **List** active projects
4. **Flag** stale notes (30+ days)
5. **Report** recent activity

### Output Format
```markdown
## Vault Status — {{date}}

### Overview
| Folder | Count |
|--------|-------|
| 00-Inbox | [N] |
| 01-Projects | [N] |
| 02-Areas | [N] |
| 03-Resources | [N] |
| 04-Archive | [N] |
| 06-Daily | [N] |

### Inbox
- Unprocessed: [N] items
- Oldest: [date]

### Active Projects
- [list]

### Stale Notes (30+ days)
- [list]

### Recent Activity
- Last commit: [date]
- Last daily note: [date]
```

### Hard Rules
- Read-only — never modify files
- ALWAYS use accurate counts
