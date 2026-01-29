# Week 6 — Building Agents from Scratch I: Agent Anatomy

**Source plan:** `study-group/study-plan-details.md` (Week 6)

## Outcome (artifact)

An implementation-agnostic agent execution loop + a set of tool cards.

Capture the loop + tool cards anywhere convenient (doc/whiteboard/notes) and share the link with the group.

## Reading

- Chapter 4: Sections 4.1–4.7

## Baseline exercise (20 min): Agent loop + tool cards

### Part A — Execution loop (10 min)

Write an execution loop that’s independent of any framework.

Template:

```text
Loop name:

1) Prepare context
2) Decide next action
3) If tool needed, call tool
4) Observe tool result
5) Update memory/state
6) Check stop conditions
7) Produce final output

Stop conditions:
- Success:
- Budget/time:
- Uncertainty:
```

### Part B — Tool cards (10 min)

Create 2–3 “tool cards” for a chosen agent.

Template:

```text
Tool name:
Purpose:
Inputs:
Outputs:
Failure modes:
Safety notes:
Validation:
```

## Stretch exercise (optional, 10–20 min): Structured output contract

Pick one tool card and define a strict output contract:

- required fields
- allowed values
- how to handle missing/invalid fields

Also define one validation step: “reject if …”
