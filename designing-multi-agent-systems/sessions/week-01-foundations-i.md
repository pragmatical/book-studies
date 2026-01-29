# Week 1 — Foundations I: Why Multi-Agent Systems?

**Source plan:** `study-group/study-plan-details.md` (Week 1)

## Outcome (artifact)

Create a shared list of tasks mapped to **model → single agent → multi-agent system (MAS)** with a short justification.

Capture the task map anywhere convenient (doc/whiteboard/notes) and share the link with the group.

## Reading (optional)

- Chapter 1: Sections 1.1–1.4

## Baseline exercise (20 min): Task mapping (model → agent → MAS)

### Setup

- Break into groups of 2–4.
- Pick **2 tasks** that your org actually does (or plausibly would).

Task ideas:

- Incident triage assistant (summarize, decide next actions, create tickets)
- Weekly status synthesis (across repos + docs + tickets)
- PR review assistant (style, security, policy checks)
- Travel planning (constraints, budget, approvals)
- Research brief (multiple sources + citations + structure)

### Worksheet (fill for each task)

Copy/paste this block twice (one per task):

```text
Task name:

1) Inputs / outputs
- Inputs:
- Outputs:

2) Where fresh data is needed
- Sources (APIs/docs/repos/people):
- How often changes:

3) Where planning is needed
- Steps that depend on earlier steps:
- Where branching/decision points appear:

4) Where multiple skills are needed
- Research:
- Coding:
- Writing:
- Domain judgment:

5) Likely failure modes
- Ambiguity / missing info:
- Hallucination risk:
- Tool failures / timeouts:
- Safety/compliance concerns:

6) Best fit (pick one)
- Model / single agent / MAS
- Why (2–3 bullets):
```

### Guidance (how to choose)

- Prefer **model** when: one-shot transformation, no tools, low ambiguity, easy verification.
- Prefer **single agent** when: needs tools + iteration + short-term state.
- Prefer **MAS** when: distinct roles/expertise, parallelism, decomposable subproblems, or robust oversight (e.g., planner + executor + verifier).

### Deliverable quality bar

- A newcomer should understand the choice in under 2 minutes.
- The “why” must mention **at least one**: tools/fresh data, planning depth, parallelism, risk/verification.

## Stretch exercise (optional, 10–20 min): Prompt-only “agent” failure demo

Goal: experience the failure modes that motivate tools/state/multiple roles.

1. Pick one task above.
2. Write a single prompt that tries to do the whole task “in one go.”
3. Ask: what breaks?
   - needs fresh data
   - missing inputs
   - ungrounded assumptions
   - no way to validate
4. Document 3 failure points and what capability would fix each (tool call, memory, verifier, HITL approval).

## Facilitation notes (for the facilitator)

- If discussion gets stuck on “it depends,” force an assumption: time budget, acceptable risk, availability of APIs.
- If one person dominates, rotate: each person must contribute one failure mode or one justification.
