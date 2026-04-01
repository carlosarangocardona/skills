---
name: obsidian-vault
description: Search, create, and manage notes in the Obsidian vault with wikilinks and index notes. Use when user wants to find, create, or organize notes in Obsidian.
---

# Obsidian Vault

## Vault location

`~/sb/`

## Conventions

Always follow the instructions and conventions outlined in `~/sb/AGENTS.md`

## Naming conventions

- **Index notes**: aggregate related topics (e.g., `work-index.md`, `skills-index.md`, `projects-index.md`).
- **kebab-case** is mandatory for all note names (e.g., `migration-plan.md`, `001-scaffolding.md`).
- Folders for organization:
  - Always use links to link notes together and also link the new notes to a proper index note as well.

## Linking

- Use Obsidian `[[wikilinks]]` syntax: `[[Note Title]]`
- Notes link to dependencies/related notes at the bottom
- Index notes are just lists of `[[wikilinks]]`

## Workflows

### Search for notes

```bash
# Search by filename
find "~/sb/" -name "*.md" | rg -i "keyword"

# Search by content
rg -rl "keyword" "~/sb/" --include="*.md"
```

Or use RipGrep/Glob tools directly on the vault path.

### How to create a new note

1. Only use **kebab-case** for note and file names.
2. Write content as a unit of learning (per vault rules).
3. Add `[[wikilinks]]` to related notes at the bottom.
4. If part of a numbered sequence, use the hierarchical numbering scheme.
5. Always use a template from the `~/sb/templates/` folder. If no template matches the prompt directly use the `~/sb/templates/meeting-note.md` template.
   - For meeting notes use the `~/sb/templates/meeting-note.md` template and name the note with the date and meeting topic (e.g., `2025-06-01-project-kickoff.md`).
   - For project notes use the `~/sb/templates/project.md` template and name the note with the `project` prefix topic (e.g., `project-agentic-commerce.md`).
   - For Today I Learned (TIL) notes use the `~/sb/templates/til.md` template and name the note with the date, `til` prefix and topic (e.g., `2025-06-01-til-agent-skills.md`).
   - For general notes use the `~/sb/templates/note.md` template and name the note with the topic (e.g., `migration-plan.md`).

### Find related notes

Search for `[[Note Title]]` across the vault to find backlinks:

```bash
rg -rl "\\[\\[Note Title\\]\\]" "~/sb/"
```

### Find index notes

```bash
find "~/sb/" -name "*Index*"
```

## Conventions

- Use **kebab-case** for all file and folder names
- Keep source-docs **flexible** (any file format accepted)
- **Never create commits or push code** - always ask the user first
