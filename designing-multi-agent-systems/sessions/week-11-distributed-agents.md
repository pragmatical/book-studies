# Week 11 — Distributed Agents and Protocols

**Source plan:** `study-group/study-plan-details.md` (Week 11)

## Outcome (artifact)

- A boundary diagram (in words) and a decision: is distribution warranted?
- A protocol interface sketch for one boundary (what messages flow across it)

Capture the boundary + protocol sketch anywhere convenient (doc/whiteboard/notes) and share the link with the group.

## Reading (optional)

- Chapter 12

## Baseline exercise (20 min): Boundary + distribution decision

### Step 1 — Draw boundaries (in text) (8 min)

Pick one scenario.

Write:

- processes/systems involved
- what data can/can’t cross boundaries
- who owns each boundary

Template:

```text
Scenario:

Components:
-

Boundaries:
- Boundary A (between X and Y):
  - Allowed data:
  - Forbidden data:

Distribution decision:
- We should/should not distribute because:
- Biggest risk:
- Mitigation:
```

### Step 2 — “Is distribution worth it?” checklist (12 min)

Answer yes/no:

- Do we need separate trust zones?
- Do we need separate deployment/lifecycles?
- Is latency acceptable?
- Do we have observability across boundaries?

## Stretch exercise (optional, 10–20 min): Threat-model the boundary

List 3 threats and 1 mitigation each:

- data leakage
- spoofed messages
- privilege escalation
