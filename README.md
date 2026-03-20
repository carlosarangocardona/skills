# Skills Repository

A curated collection of reusable skills for OpenCode, designed to enhance productivity and streamline development workflows.

## Overview

This repository contains specialized skills that extend coding agents capabilities with domain-specific functionality. Each skill encapsulates particular workflows, best practices, and automation patterns to help users accomplish complex tasks more efficiently.

These skills are companion to the AI agents defined in the [ai-agents](https://github.com/carlosarangocardona/ai-agents) repository, creating an ecosystem for intelligent development workflows.

## Available Skills

### 1. **Interviewer**

Conduct rigorous design and planning reviews through systematic questioning.

- **Purpose**: Stress-test plans and designs by walking through each decision branch until reaching shared understanding
- **Use Cases**:
  - Validate architectural decisions before implementation
  - Get challenged on design choices
  - Ensure comprehensive planning coverage
- **Location**: `./interviewer/`
- **Credits**: Based on the [mattpocock skills](https://github.com/mattpocock/skills/blob/main/grill-me/SKILL.md)

Install:

```
npx skills add carlosarangocardona/interviewer

```

### 2. **Obsidian Vault**

Manage and organize notes in an Obsidian vault with consistent conventions.

- **Purpose**: Search, create, and organize notes with wikilinks and index notes
- **Use Cases**:
  - Maintain a personal knowledge base
  - Find related notes through backlinks
  - Follow a standardized naming and organization system
- **Location**: `./obsidian-vault/`
- **Vault Path**: `~/sb/`
- **Credits**: Based on [mattpocock's Obsidian vault skill](https://github.com/mattpocock/skills/blob/main/obsidian-vault/SKILL.md)

Install:

```
npx skills add carlosarangocardona/obsidian-vault

```

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

## References

These skills are based on:

- [Matt Pocock](https://github.com/mattpocock) skills.
