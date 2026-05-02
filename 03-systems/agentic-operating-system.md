# Agentic Operating System

## Purpose

Use agents and apps to reduce administrative load, increase consistency, and help the human operators make better decisions without removing human judgment from high-risk work.

## Operating Domains

```mermaid
flowchart LR
  Lead[Lead Capture] --> Intake[Intake Agent]
  Intake --> Estimate[Estimating Support]
  Estimate --> HumanReview[Human Review]
  HumanReview --> Quote[Quote Follow-Up]
  Quote --> Job[Job Management]
  Job --> Field[Field Updates]
  Field --> Finance[Job Costing]
  Finance --> Review[Operating Review]
  Review --> Improve[System Improvements]
```

## Candidate Agents And Apps

| Domain | Agent Or App | Human In The Loop |
| --- | --- | --- |
| Marketing | Creates service-page drafts, campaign ideas, review requests, and local SEO briefs. | Filip or marketing owner approves publishing. |
| Lead intake | Summarizes inquiries, routes leads, schedules callbacks, checks missing information. | Mikolaj approves estimates and commitments. |
| Scheduling | Flags conflicts, crew availability, and customer timing issues. | Principal operator confirms schedule. |
| Estimating | Drafts scope, checklist, exclusions, and pricing notes from templates. | Edward approves estimate logic. |
| Job management | Creates task lists, daily summaries, customer updates, and issue logs. | Project lead confirms field reality. |
| Finance | Summarizes job costs, margin leakage, receivables, and cash risks. | Human reviews books and financial decisions. |
| HR | Screens candidates, prepares interview notes, tracks onboarding. | Human conducts interviews and employment decisions. |
| Training | Turns field knowledge into SOPs, checklists, and quizzes. | Edward validates trade accuracy. |
| Performance | Tracks quality, reliability, callbacks, and training needs. | Human manager handles feedback and discipline. |

## Non-Negotiables

- Agents do not make legal, employment, safety, licensing, or final pricing decisions without human approval.
- Agents should create drafts, summaries, alerts, and checklists.
- Humans retain accountability for customer commitments, hiring decisions, job safety, and financial commitments.

