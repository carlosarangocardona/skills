---
name: obsidian-vault
description: Search, create, and manage notes in the Obsidian vault with wikilinks and index notes. Use when user wants to find, create, or organize notes in Obsidian.
---

# Obsidian Vault

## Vault location

`~/sb/`

Mostly flat at root level.

## Naming conventions

- **Index notes**: aggregate related topics (e.g., `Work Index.md`, `Skills Index.md`, `Projects Index.md`).
- **Title case** for all note names.
- Folders for organization:
  - Use the `~/sb/areas/` folder to divide notes into broad categories (e.g., `Home`, `Personal`, `Work`)
  - Use links and index notes as well.
  - Use the `~/sb/notes/` folder for general notes that don't fit into a specific area, or for temporary notes before organizing them.

## Linking

- Use Obsidian `[[wikilinks]]` syntax: `[[Note Title]]`
- Notes link to dependencies/related notes at the bottom
- Index notes are just lists of `[[wikilinks]]`

## Workflows

### Search for notes

```bash
# Search by filename
find "~/sb/" -name "*.md" | grep -i "keyword"

# Search by content
grep -rl "keyword" "~/sb/" --include="*.md"
```

Or use Grep/Glob tools directly on the vault path.

### Create a new note

1. Use **Title Case** for filename
2. Write content as a unit of learning (per vault rules)
3. Add `[[wikilinks]]` to related notes at the bottom
4. If part of a numbered sequence, use the hierarchical numbering scheme
5. Always try to use a template from the `~/sb/templates/` folder. If no template matches the prompt directly use the `note.md` template.

### Find related notes

Search for `[[Note Title]]` across the vault to find backlinks:

```bash
grep -rl "\\[\\[Note Title\\]\\]" "~/sb/"
```

### Find index notes

```bash
find "~/sb/" -name "*Index*"
```
