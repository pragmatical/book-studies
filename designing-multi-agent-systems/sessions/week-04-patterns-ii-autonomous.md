# Week 4 — Patterns II: Autonomous Patterns

**Source plan:** `study-group/study-plan-details.md` (Week 4)

## Outcome (artifact)

A pattern-selection decision record for **two scenarios**, including risks and mitigations.

Capture the decision record anywhere convenient (doc/whiteboard/notes) and share the link with the group.

## Reading

- Chapter 2: Sections 2.3–2.6

## Baseline exercise (20 min): Pattern picker for 2 scenarios

### Step 1 — Choose two scenarios (3 min)

Pick scenarios with different constraints.

Examples:

- A: “Generate a weekly metrics report (deterministic, repeatable)”
- B: “Investigate an outage with evolving evidence (open-ended)”

### Step 2 — Fill the pattern picker matrix (10 min)

Score each dimension Low/Medium/High:

```text
Scenario:

Need determinism:
Need parallelism:
Need exploration/creativity:
Risk (security/compliance):
Need explainability/traceability:
Tolerance for cost:

Recommended pattern:
- Workflow / plan-based / handoff / group-chat / round-robin / hybrid

Why (3 bullets):
-
```

### Step 3 — Capture risks + mitigations (7 min)

For each scenario, write:

- 2 risks (e.g., runaway loops, tool misuse, unclear termination)
- 1 mitigation per risk (e.g., budget, explicit stop rule, HITL approval)

## Stretch exercise (optional, 10–20 min): Compare two orchestrations (tabletop)

Do a “tabletop simulation” of the same scenario under two patterns:

1. Workflow (fixed sequence)
2. Autonomous (planner chooses next step)

Log:

- where autonomy helps
- where autonomy hurts
- what guardrails you need for the autonomous version
