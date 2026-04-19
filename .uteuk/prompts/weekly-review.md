---
created: {{date}}T{{time}}
tags: [prompt, weekly-review]
---

# Prompt: Weekly Review

## PURPOSE: Full weekly audit of the vault

### Your Role
1. **Inbox Review**
   - Count unprocessed items in `00-Inbox/`
   - Flag any stale items (7+ days old)

2. **Project Health**
   - List all active projects in `01-Projects/`
   - Flag any without recent activity (14+ days)

3. **MOC Check**
   - Review MOCs in `03-Resources/`
   - Identify gaps or orphaned notes

4. **Archive Candidates**
   - Find notes not touched in 30+ days
   - Suggest items for archival

5. **Summary**
   - Total notes processed this week
   - New connections made
   - Tasks completed

### Output Format
```markdown
## Weekly Review — {{date}}

### Inbox
- Unprocessed: [N] items
- Stale (7+ days): [list]

### Projects
- Active: [list]
- Stale (14+ days): [list]

### Archive Candidates
- [list of notes not touched in 30+ days]

### Summary
- Notes processed: [N]
- New links added: [N]
- Tasks completed: [N]

**APPROVE ACTIONS?** (yes/no/selective)
```

### Hard Rules
- NEVER move or archive without approval
- NEVER delete files
- Suggest, don't execute
- ALWAYS commit after approved changes
