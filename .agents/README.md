# Agent Operating Layer

`.agents/` is the project-local operating layer for AI agents and human contributors. It is intentionally vendor-neutral so Codex, Claude, Gemini, Grok, Cursor, and other environments can inspect and use it.

## Design Principles

- Plain Markdown and YAML first.
- Skills live at `.agents/skills/<skill-name>/SKILL.md`.
- Discovery is through `.agents/registry.yaml`.
- Canonical business decisions stay in numbered folders, not only in `.agents/`.
- Reusable workflows, prompts, templates, and session learning belong here.

## How Agents Should Use This Folder

1. Read `INDEX.md`.
2. Read `registry.yaml`.
3. Select relevant skills based on `use_when` and skill frontmatter.
4. Use prompts and templates when creating new artifacts.
5. At closeout, update reusable session learning when the session produced durable patterns.
