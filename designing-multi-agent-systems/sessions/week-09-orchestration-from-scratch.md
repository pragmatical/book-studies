# Week 9 — Multi-Agent Workflows & Orchestration from Scratch

**Source plan:** `study-group/study-plan-details.md` (Week 9)

## Outcome (artifact)

A workflow spec updated with:

- checkpoint policy
- termination rule
- recovery rule

Capture the updated workflow spec anywhere convenient (doc/whiteboard/notes) and share the link with the group.

## Reading

- Chapter 6
- Chapter 7: Sections 7.1–7.3

## Baseline exercise (20 min): Add checkpoints + termination + recovery

Start from a workflow you made in Week 3 (or create a quick one).

### Step 1 — Checkpoint policy (7 min)

Define:

- where to checkpoint (after which steps)
- what to store (inputs/outputs/state)
- how to resume

Template:

```text
Checkpoint points:
- After step X store:

Resume strategy:
-
```

### Step 2 — Termination rule (7 min)

Define explicit stop rules:

- success criteria
- max iterations
- max tool calls
- max elapsed time

### Step 3 — Recovery rule (6 min)

Pick one failure (tool timeout, bad schema, missing input) and define:

- retry policy
- fallback (ask user, switch strategy, abort)
- what gets logged

## Stretch exercise (optional, 10–20 min): Failure injection tabletop

Pick a step and pretend it fails 3 times.

- Does the system loop forever?
- Does it degrade gracefully?
- What would a human want to see in the trace?
