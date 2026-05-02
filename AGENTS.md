# Agent Instructions

This repository is designed for Codex and other agents to collaborate with humans on a business operating plan.

## Required Startup Context

Before substantial work, read:

1. [README.md](/Users/fszale/projects/personal/construction-operational-plan/README.md)
2. [.agents/README.md](/Users/fszale/projects/personal/construction-operational-plan/.agents/README.md)
3. [.agents/INDEX.md](/Users/fszale/projects/personal/construction-operational-plan/.agents/INDEX.md)
4. [.agents/registry.yaml](/Users/fszale/projects/personal/construction-operational-plan/.agents/registry.yaml)
5. Any task-relevant `.agents/skills/<skill-name>/SKILL.md`

`.agents/` is the canonical project-local agent operating layer.

## Operating Rules

- Work from the existing folder structure.
- Keep edits tightly scoped to the requested workstream.
- Put scratch work in `09-contributor-workspace/`.
- Put reusable agent context in `.agents/`.
- Put canonical business content in the numbered folders.
- Add assumptions to `00-overview/assumptions.md`.
- Add open issues to `00-overview/open-questions.md`.
- Add material decisions to `07-execution-plan/decision-log.md`.
- When using research, cite the source and separate evidence from inference.
- Do not present legal, tax, insurance, employment, or securities guidance as final professional advice.

## Session Closeout

At the end of substantial sessions:

- Summarize reusable learning in `.agents/sessions/summaries/YYYY-MM-DD-session-summary.md`.
- Update `.agents/INDEX.md` if reusable prompts, templates, or skills were added.
- Promote repeated workflows into `.agents/skills/<skill-name>/SKILL.md`.
- List unresolved questions and next recommended agent tasks.
