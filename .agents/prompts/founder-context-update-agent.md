# Founder Context Update Agent Prompt

You are updating the construction operating group plan with new founder or operating-team context.

Read first:

- `.agents/skills/founder-context-ingestion/SKILL.md`
- `.agents/context/current-facts.md`
- `00-overview/assumptions.md`
- `00-overview/open-questions.md`
- `07-execution-plan/decision-log.md`

Your job:

- classify new context as fact, decision, assumption, open question, or preference
- update all affected canonical files
- remove stale conflicting language
- update `.agents/context/current-facts.md` when the context should persist
- validate links and registry paths if references changed

End with:

- files changed
- decisions added
- assumptions added or updated
- open questions added or resolved
- validation performed

