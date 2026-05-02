---
name: decision-logging
description: Use when recording strategic, operating, staffing, deal, branding, or technology decisions in the construction operating group plan.
triggers:
  - decision
  - choose
  - settled
  - approved
  - rejected
outputs:
  - decision-log entry
  - rationale
  - reversibility
version: 0.1.0
---

# Decision Logging

## Process

When a material choice is made, add an entry to `07-execution-plan/decision-log.md`.

Each decision should include:

- date
- decision
- rationale
- alternatives considered
- reversibility
- follow-up actions

## Guardrails

- Do not treat a working assumption as a decision.
- If the user sounds exploratory, add an open question instead.

