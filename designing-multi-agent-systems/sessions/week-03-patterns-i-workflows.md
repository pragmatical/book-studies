# Week 3 — Patterns I: Workflow Patterns

**Source plan:** `study-group/study-plan-details.md` (Week 3)

## Outcome (artifact)

One clear, testable workflow specification:

- 4–6 steps
- inputs/outputs per step
- at least one validation/check step
- definition of “done”

Capture the workflow spec anywhere convenient (doc/whiteboard/notes) and share the link with the group.

## Reading (optional)

- Chapter 2: Sections 2.1–2.2

## Baseline exercise (20 min): Workflow spec from a plain-language task

### Step 1 — Pick a task (2 min)

Choose a task where **determinism** and **debuggability** matter.

Examples:

- “Generate release notes from merged PRs”
- “Create a research brief with citations”
- “Triage and categorize incoming support tickets”

### Step 2 — Write the workflow (10 min)

Write steps using **verbs only** (no implementation).

Template:

```text
Workflow name:
Trigger:

Step 1 (verb):
- Input:
- Output:
- Failure modes:

Step 2 (verb):
...

Validation step (required):
- What to check:
- How to report failure:

Done definition:
-

Escalation / fallback:
-
```

Validation examples:

- “Output matches schema”
- “Citations present for all claims”
- “No PII leakage”
- “All required sections present”

### Step 3 — Add two edge cases (8 min)

For each edge case, specify:

- which step detects it
- what happens next (retry, ask for input, abort)

## Stretch exercise (optional, 10–20 min): Make it executable (paper prototype)

Convert the spec into a runbook:

- For each step, add a “prompt stub” (what the agent is told)
- Add one “handoff rule” (when to escalate to human)
- Add a “timeout rule” (when to stop)
