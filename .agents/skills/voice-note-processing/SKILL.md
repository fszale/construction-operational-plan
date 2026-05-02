---
name: voice-note-processing
description: Use when converting dictated founder notes into structured business plan updates, assumptions, decisions, risks, and agent tasks.
triggers:
  - voice note
  - dictated
  - transcript
  - rough note
  - clean this up
outputs:
  - extracted assumptions
  - decisions
  - risks
  - tasks
  - canonical plan edits
version: 0.1.0
---

# Voice Note Processing

## Process

1. Keep the original transcript in `09-contributor-workspace/voice-notes/`.
2. Extract ideas, assumptions, decisions, risks, questions, and tasks.
3. Update the relevant canonical files.
4. Preserve ambiguity instead of flattening it into false certainty.

## Output Format

End with:

- captured idea
- plan files updated
- assumptions added
- open questions
- recommended next voice prompt

