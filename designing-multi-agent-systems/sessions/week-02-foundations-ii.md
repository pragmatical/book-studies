# Week 2 — Foundations II: Agent & MAS Architecture

**Source plan:** `study-group/study-plan-details.md` (Week 2)

## Outcome (artifact)

- A shared “agent anatomy” model: **model, tools, memory, control loop, termination**
- A minimal MAS orchestration sketch (how agents take turns and how the system stops)

Capture the diagram and orchestration sketch anywhere convenient (doc/whiteboard/notes) and share the link with the group.

## Reading (optional)

- Chapter 1: Sections 1.4–1.9

## Baseline exercise (20 min): Agent anatomy + 3-turn role-play trace

### Part A — Agent anatomy diagram (10 min)

As a group, write a “diagram in words” with these components:

- **Model:** what it’s responsible for (decisions, tool selection, writing)
- **Tools:** what actions exist (and what the model is not allowed to do without tools)
- **Memory:** what state is carried (short-term chat, long-term notes)
- **Control loop:** what repeats and when
- **Termination:** stop conditions (success, time, budget, uncertainty)

Use this template:

```text
Agent Name:
Purpose:

Model responsibilities:
-

Tool list:
- Tool: input -> output (failure mode)

Memory:
- Short-term:
- Long-term:

Control loop:
1)
2)
3)

Termination conditions:
- Done when:
- Stop when:
```

### Part B — Role-play execution trace (10 min)

Roles:

- Person A = “Poet” (creative generator)
- Person B = “Critic” (verifier/editor)
- Person C = “Orchestrator” (decides next speaker + stop)

Task prompt (use one of these):

- “Draft a 1-page brief arguing for/against using MAS for incident triage.”
- “Write a checklist for safe tool usage in agents.”

Run exactly 3 turns and log:

- Turn number
- Speaker
- Message summary (1–2 lines)
- Orchestrator decision (“next speaker” + reason)
- Stop condition check (met/not met + why)

Deliverable: a readable mini-trace that shows **coordination** and **termination** clearly.

## Stretch exercise (optional, 10–20 min): Interpret a real trace

If someone has an agent trace (from any framework), do a “trace reading”:

1. Identify tool calls and why they were made.
2. Identify any loops (retries, repeated reasoning, repeated tool use).
3. Identify failure mode(s): missing input, tool error, hallucination.
4. Propose one change:
   - add a validation step
   - add an explicit stop condition
   - add HITL approval for risky actions
