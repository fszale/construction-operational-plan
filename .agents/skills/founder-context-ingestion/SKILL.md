---
name: founder-context-ingestion
description: Use when the founder or operating team provides new business context, constraints, decisions, geography, roles, availability, assumptions, or corrections that need to be propagated through the project plan.
triggers:
  - update with this context
  - new context
  - add this assumption
  - change the geography
  - update participant availability
outputs:
  - updated canonical files
  - updated assumptions
  - updated decisions
  - updated current facts
  - stale-context check
version: 0.1.0
---

# Founder Context Ingestion

## Process

1. Classify the new input as fact, decision, assumption, open question, or preference.
2. Update `.agents/context/current-facts.md` for stable context.
3. Update canonical files in numbered folders when the context changes the plan.
4. Add assumptions to `00-overview/assumptions.md`.
5. Add decisions to `07-execution-plan/decision-log.md`.
6. Replace stale wording elsewhere rather than adding conflicting statements.
7. Run a link and registry check if file references changed.

## Common Propagation Targets

- participant availability: `00-overview/participants.md`, `07-execution-plan/30-60-90-launch-plan.md`, readiness checklist
- geography: strategy docs, marketing docs, launch plan, market research tasks
- first trade wedge: owner profile, acquisition thesis, launch plan, assumptions, open questions
- deal structure: business model, incentive design, legal/risk, finance, decision log

## Guardrails

- Do not treat a preference as validated market evidence.
- Preserve unresolved items in `00-overview/open-questions.md`.
- If a new fact invalidates existing assumptions, update the assumption status instead of leaving both versions.

