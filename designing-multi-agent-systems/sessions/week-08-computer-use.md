# Week 8 — Computer-Use Agents & Interface Grounding

**Source plan:** `study-group/study-plan-details.md` (Week 8)

## Outcome (artifact)

A UI-agent feasibility rubric applied to two tasks (API vs UI automation).

Capture the rubric anywhere convenient (doc/whiteboard/notes) and share the link with the group.

## Reading (optional)

- Chapter 5

## Baseline exercise (20 min): UI-agent feasibility rubric

Pick two tasks:

- Task A: can be done via API
- Task B: would require UI interaction

Score each dimension Low/Medium/High:

```text
Task:

Observability (can we see state reliably?):
Action space size (few safe actions vs many risky ones):
Fragility (UI changes, flakiness):
Safety (risk of destructive actions):
Fallback (can a human easily take over?):
Auditability (can we log actions meaningfully?):

Decision:
- Use API agent / Use UI agent / Don’t automate

Required guardrails:
-
```

## Stretch exercise (optional, 10–20 min): Safety boundary definition

Define “hard limits” for a UI agent:

- pages/screens it can access
- actions it can take
- actions that always require approval
- stop conditions (e.g., repeated failures)
