# Week 7 — Building Agents from Scratch II: Middleware, Memory & HITL

**Source plan:** `study-group/study-plan-details.md` (Week 7)

## Outcome (artifact)

A “minimum viable controls” checklist (safety + observability) and one policy.

Capture the checklist + policy anywhere convenient (doc/whiteboard/notes) and share the link with the group.

## Reading (optional)

- Chapter 4: Sections 4.8–4.13

## Baseline exercise (20 min): Minimum viable controls

Pick an agent scenario (e.g., PR reviewer, ticket triager, research assistant).

Fill this checklist:

```text
What to log (minimum):
- user request
- model outputs (or summary)
- tool calls (inputs/outputs)
- stop reason

What requires approval (HITL):
- external side effects (writes/deletes)
- sending messages to humans
- access to sensitive data

What to store in memory:
- short-term:
- long-term:

What to never store:
-
```

Then write one policy in the form:

```text
When [condition], require [approval/validation] and log [fields].
```

## Stretch exercise (optional, 10–20 min): Middleware hook design

Design three middleware hooks:

- Before model call
- Before tool call
- After tool call

For each hook, specify:

- input data
- what it can modify
- what it must record
