# Designing Multi-Agent Systems Study Group
<!-- markdownlint-disable MD024 -->

Using **Victor Dibia’s _Designing Multi-Agent Systems_** as the primary material.

Grab your copy: <https://buy.multiagentbook.com> (please check on expense guidelines with your manager)

Book GitHub Repository: <https://github.com/victordibia/designing-multiagent-systems>

---

## How each session runs (60 minutes)

Use the same structure every week to minimize “context debt” and make facilitation easier.

- **5 min — Arrival + agenda**: state today’s outcome (a shared artifact) and how decisions will be made.
- **10 min — “Everyone can participate” primer**: one person gives a short recap using the standing prompt.
- **30 min — Small-group exercise** (3–5 people): produce a concrete artifact.
- **10 min — Share-outs**: each group shares 1 insight + 1 open question.
- **5 min — Close**: quick retro + assign light prep (optional).

---

## 12-week schedule (table)

| Week | Theme | Reading | Session outcome (artifact) | Baseline exercise (low-dependency) | Stretch (optional) |
| --- | --- | --- | --- | --- | --- |
| 1 | [Foundations I: Why MAS?](study-plan-details.md#week-1--foundations-i-why-multi-agent-systems) | Preface (skim), Ch 1: 1.1–1.4 | Task list mapped to **model → agent → MAS** | Pick 2–3 tasks; fill 6-box template (inputs/outputs, fresh data, planning, multi-skill, failure modes, best fit) | Build a prompt-only “agent” and document where it fails |
| 2 | [Foundations II: Agent & MAS architecture](study-plan-details.md#week-2--foundations-ii-agent-and-mas-architecture) | Ch 1: 1.4–1.9 | “Agent anatomy” diagram + minimal orchestration sketch | Diagram model/tools/memory/control loop/termination; do a 3-turn role-play trace (poet/critic/orchestrator) | Inspect an existing execution trace from someone’s implementation |
| 3 | [Patterns I: Workflow patterns](study-plan-details.md#week-3--multi-agent-patterns-i-workflow-patterns) | Ch 2: 2.1–2.2 | One clear, testable workflow graph | Convert a plain-language task to a 4–6 step workflow; add inputs/outputs + at least 1 validation step | Implement the workflow in a repo framework of choice |
| 4 | [Patterns II: Autonomous patterns](study-plan-details.md#week-4--multi-agent-patterns-ii-autonomous-patterns) | Ch 2: 2.3–2.6 | Pattern-selection decision record for 2 scenarios | Use a “pattern picker” matrix (determinism, clarity, safety, cost); choose pattern; capture 2 risks + newcomer summary | Prototype an orchestration approach and compare behaviors |
| 5 | [UX principles for MAS](study-plan-details.md#week-5--ux-principles-for-multi-agent-systems) | Ch 3 | Usability review checklist for agentic UX | Score a product/flow on capability discovery, cost-aware delegation, observability/provenance, interruptibility; propose one quick win each | Add minimal logging + cancel/stop control to a sample agent |
| 6 | [Build agents I: Agent anatomy](study-plan-details.md#week-6--building-agents-from-scratch-i-agent-anatomy) | Ch 4: 4.1–4.7 | Implementation-agnostic agent execution loop | Create tool cards (name/input/output/failure/safety); place them in the loop | Implement 1 tool + structured output |
| 7 | [Build agents II: Middleware, memory, HITL](study-plan-details.md#week-7--building-agents-from-scratch-ii-middleware-memory--hitl) | Ch 4: 4.8–4.13 | “Minimum viable controls” checklist (safety + observability) | Decide what to log, what needs approval, what to store; write one policy (“When X, require Y and log Z”) | Implement a middleware hook for logging/approval/memory policies |
| 8 | [Computer-use agents & interface grounding](study-plan-details.md#week-8--computer-use-agents-and-interface-grounding) | Ch 5 | UI-agent feasibility rubric | Compare 2 tasks (API vs UI automation); fill rubric (observability, action space, fragility, safety, fallback) | Try a small UI automation demo with strong safety boundaries |
| 9 | [Workflows & orchestration from scratch](study-plan-details.md#week-9--multi-agent-workflows--orchestration-from-scratch) | Ch 6; Ch 7: 7.1–7.3 | Testable workflow spec + termination rule | Add checkpoint policy + termination rule + recovery rule to an existing workflow graph | Implement checkpoints/recovery and validate with a failure injection |
| 10 | [Evaluation & optimization](study-plan-details.md#week-10--evaluation-and-optimization-of-mas) | Ch 10; Ch 11: 11.2–11.3 | 5-task evaluation suite + scoring rubric | Brainstorm 10 tasks; pick 5; define measurable success (correctness/completeness/format + usefulness 1–5) | Implement LLM-as-judge and compare to rule-based scoring |
| 11 | [Distributed agents & protocols](study-plan-details.md#week-11--distributed-agents-and-protocols) | Ch 12 | Boundary diagram + “is distribution warranted?” decision | Draw process/system boundaries; identify data that can’t cross; decide if MCP/A2A is justified for one scenario | Sketch a protocol interface and threat-model the boundary |
| 12 | [Ethics, responsible AI, capstone](study-plan-details.md#week-12--ethics-responsible-ai-and-capstone-synthesis) | Ch 13 + (Ch 14 or 15) | One-page capstone “poster” design | Problem statement; agents+roles; tools+approvals; orchestration choice; evaluation plan; top 3 risks+mitigations | Partial implementation + demo trace |

---
