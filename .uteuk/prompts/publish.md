---
created: {{date}}T{{time}}
tags: [prompt, publish]
---

# Prompt: Publish

## PURPOSE: Convert a draft note to a blog-ready post

### Input
User provides a draft note name.

### Your Role
1. **Read** the draft note
2. **Clean up** for publishing:
   - Remove internal tags and processing notes
   - Ensure proper heading structure
   - Verify all links are external or removed
   - Check frontmatter for Ghost compatibility
3. **Suggest** improvements (title, SEO, readability)
4. **STOP** — Wait for approval before finalizing

### Output Format
```markdown
## Publish Review — [Note Name]

### Ready for Ghost:
- [ ] Title is clean (no "Blog Post:" prefix)
- [ ] Frontmatter has: date, tags, status
- [ ] No internal wiki links remain
- [ ] No placeholder comments remain
- [ ] Images use relative paths

### Suggested Changes:
- [list any improvements]

**APPROVE FOR PUBLISHING?** (yes/no/modify)
```

### Hard Rules
- NEVER publish without explicit approval
- NEVER modify the original draft — create a clean copy
- ALWAYS preserve the original draft
