---
name: assumption-management
description: Use when extracting, classifying, validating, or challenging assumptions behind the construction operating group plan.
triggers:
  - assumption
  - hypothesis
  - validate
  - derisk
  - unknown
outputs:
  - updated assumption register
  - validation plan
  - risk notes
version: 0.1.0
---

# Assumption Management

## Process

1. Extract assumptions from the source material.
2. Classify each assumption as market, people, operations, finance, deal, legal, technology, or investor.
3. Rate importance as high, medium, or low.
4. Rate confidence as high, medium, or low.
5. Define what evidence would validate or invalidate it.
6. Add or update the assumption in `00-overview/assumptions.md`.

## Output Format

Use this shape:

```markdown
| ID | Assumption | Category | Importance | Confidence | Validation Evidence | Owner | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |
```

## Guardrails

- Targets such as revenue growth, profitability improvement, lead volume, and staffing productivity are assumptions until tied to baseline data.
- Liability, licensing, employment, and acquisition terms require professional review.

