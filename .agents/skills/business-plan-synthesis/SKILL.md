---
name: business-plan-synthesis
description: Use when turning rough founder notes, contributor drafts, or agent research into structured business plan updates across vision, strategy, operations, systems, finance, and execution files.
triggers:
  - synthesize business notes
  - update the plan
  - organize this idea
  - turn this into plan sections
outputs:
  - canonical plan edits
  - assumptions
  - open questions
  - next tasks
version: 0.1.0
---

# Business Plan Synthesis

## When To Use

Use this skill when a human provides rough notes or when several plan files need to be reconciled into one coherent business operating blueprint.

## Process

1. Identify which parts are facts, assumptions, decisions, risks, and open questions.
2. Update canonical plan files in the numbered folders.
3. Add uncertain claims to `00-overview/assumptions.md`.
4. Add unresolved issues to `00-overview/open-questions.md`.
5. Add strategic choices to `07-execution-plan/decision-log.md`.
6. Keep `.agents/` for reusable process, not canonical business truth.

## Guardrails

- Do not over-polish away the founder's intent.
- Do not create certainty where evidence is missing.
- Do not bury critical risks in prose.
