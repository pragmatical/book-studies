<!-- markdownlint-disable MD024 MD036 -->

# Overview

## Meeting schedule

This study group runs in **two layers**:

- **Large-group calls (4 total):**
  - Intro / kickoff
  - End of Month 1
  - End of Month 2
  - Final session
- **Small groups (weekly):** timezone-based pods meet weekly to discuss the reading and run the session exercise.

Reading is **expected**, but if someone hasn’t read they should still be able to participate—each pod starts with a quick recap.

## Standard weekly session agenda (60 minutes)

- **5 min — Arrival + agenda**: state today’s outcome and how decisions will be made.
- **8 min — Primer / recap**: one person gives a short recap so everyone can participate.
- **20 min — Baseline exercise**: small-group exercise to apply the concepts.
- **8 min — Share-outs**: each group shares 1 insight + 1 open question.
- **15 min — Optional demos**: 1–3 quick demos (tooling, traces, prototypes, or examples).
- **4 min — Close**: quick retro + wrap-up.

## Table of Contents

- [Week 1 — Foundations I: Why Multi-Agent Systems?](#week-1--foundations-i-why-multi-agent-systems)
- [Week 2 — Foundations II: Agent and MAS Architecture](#week-2--foundations-ii-agent-and-mas-architecture)
- [Week 3 — Multi-Agent Patterns I: Workflow Patterns](#week-3--multi-agent-patterns-i-workflow-patterns)
- [Week 4 — Multi-Agent Patterns II: Autonomous Patterns](#week-4--multi-agent-patterns-ii-autonomous-patterns)
- [Week 5 — UX Principles for Multi-Agent Systems](#week-5--ux-principles-for-multi-agent-systems)
- [Week 6 — Building Agents from Scratch I: Agent Anatomy](#week-6--building-agents-from-scratch-i-agent-anatomy)
- [Week 7 — Building Agents from Scratch II: Middleware, Memory & HITL](#week-7--building-agents-from-scratch-ii-middleware-memory--hitl)
- [Week 8 — Computer-Use Agents and Interface Grounding](#week-8--computer-use-agents-and-interface-grounding)
- [Week 9 — Multi-Agent Workflows & Orchestration from Scratch](#week-9--multi-agent-workflows--orchestration-from-scratch)
- [Week 10 — Evaluation and Optimization of MAS](#week-10--evaluation-and-optimization-of-mas)
- [Week 11 — Distributed Agents and Protocols](#week-11--distributed-agents-and-protocols)
- [Week 12 — Ethics, Responsible AI, and Capstone Synthesis](#week-12--ethics-responsible-ai-and-capstone-synthesis)

## Week 1 — Foundations I: Why Multi-Agent Systems?

**Reading**: Chapter 1: Sections 1.1–1.4 (Preface covered in kickoff)

**Goals**

- Distinguish when a **model**, **single agent**, or **multi-agent system (MAS)** is the right tool.
- Recognize task characteristics that push you toward agentic systems (planning, tools, context, adaptation).
- Build a shared vocabulary for discussing “agentic” work in plain language.

**Key Concepts**

- Task complexity spectrum: model → agent → MAS.
- Agent capabilities: reasoning, acting (tools), communicating, adapting.
- Common failure mode: prompt-only solutions break when they need tools, fresh data, or robust planning.

**Session Outcome**
A shared list of tasks mapped to **model → agent → MAS**.

**Baseline Group Exercise (Low-Dependency)**

- Pick 2–3 tasks anyone can understand (e.g., travel planning, weekly status summary, incident triage).
- For each task, fill a 6-box template:
  - Inputs / Outputs
  - Where fresh data is needed
  - Where planning is needed
  - Where multiple skills are needed
  - Likely failure modes
  - Best fit: model / agent / MAS (and why)

**Stretch (Optional)**
Build a prompt-only “agent” and document where it fails.

---

## Week 2 — Foundations II: Agent and MAS Architecture

**Reading**: Chapter 1: Sections 1.4–1.9

**Goals**

- Identify the core components of an agent: **model, tools, memory, control loop**.
- Understand what makes a system “multi-agent” and how orchestration affects reliability and cost.
- Practice reading an interaction as an **execution trace** (what happened, why, and when it stops).

**Key Concepts**

- Agent action–perception loop and termination.
- Orchestration basics: round-robin vs decision-based turn taking.
- Traces/logs as a shared debugging surface for technical and non-technical participants.

**Session Outcome**
A shared “agent anatomy” diagram and a minimal orchestration sketch.

**Baseline Group Exercise (Low-Dependency)**

- Make one diagram together:
  - Model, tools, memory, control loop, termination.
- Then do a **role-play trace** (no code):
  - Person A = “poet”, Person B = “critic”, Person C = “orchestrator”.
  - Run 3 turns and write down: messages, decisions, stop condition.

**Applied (Optional)**
Inspect an existing trace from someone’s implementation.

---

## Week 3 — Multi-Agent Patterns I: Workflow Patterns

**Reading**: Chapter 2: Sections 2.1–2.2

**Goals**

- Translate a real task into a simple, testable workflow.
- Understand the difference between **sequential**, **conditional**, and **parallel** steps.
- Make “done” and “quality checks” explicit in the workflow.

**Key Concepts**

- Workflows as graphs: nodes (steps) and edges (transitions).
- Determinism and debuggability as benefits of workflows.
- Validation steps as a practical reliability tool.

**Session Outcome**
One workflow graph the group agrees is clear and testable.

**Baseline Group Exercise (Low-Dependency)**

- Start with a plain-language task statement.
- Convert it into a workflow with:
  - 4–6 steps (verbs only)
  - inputs/outputs per step
  - at least 1 validation/check step
- Everyone can contribute by suggesting steps, checks, or edge cases.

**Stretch (Optional)**
Implement the workflow in the repo framework of choice.

---

## Week 4 — Multi-Agent Patterns II: Autonomous Patterns

**Reading**: Chapter 2: Sections 2.3–2.6

**Goals**

- Compare autonomous coordination patterns and choose one for a scenario.
- Understand trade-offs between explicit workflows and emergent coordination.
- Make safety, cost, and clarity constraints first-class in pattern selection.

**Key Concepts**

- Autonomy spectrum (workflow → semi-autonomous → autonomous).
- Patterns: plan-based, handoff, conversation/group-chat.
- Pattern selection is a design decision: wrong pattern is a common failure mode.

**Session Outcome**
A pattern-selection decision record for 2 scenarios.

**Baseline Group Exercise (Low-Dependency)**

- Use a “pattern picker” matrix:
  - Determinism needed? (low/med/high)
  - Task clarity? (low/med/high)
  - Safety constraints? (low/med/high)
  - Cost sensitivity? (low/med/high)
- For two scenarios, choose: workflow vs plan-based vs handoff vs group-chat.
- Ensure you capture:
  - 2 risks (from a risk/security/compliance perspective), and
  - a plain-language summary (from a newcomer perspective).

---

## Week 5 — UX Principles for Multi-Agent Systems

**Reading**: Chapter 3

**Goals**

- Treat agent UX as **delegation design**, not just interface design.
- Identify what users need to trust and control an agentic system.
- Produce actionable UX improvements that reduce confusion and risk.

**Key Concepts**

- Capability discovery: what the system can/can’t do.
- Cost-aware delegation: time/money trade-offs.
- Observability & provenance: “show your work.”
- Interruptibility: stop, pause, undo, and recover.

**Session Outcome**
A usability review checklist for agentic UX.

**Baseline Group Exercise (Low-Dependency)**

- Pick any familiar product/flow (even non-AI).
- Score it against the four principles:
  - capability discovery
  - cost-aware delegation
  - observability & provenance
  - interruptibility
- Produce one “quick win” improvement for each principle.

**Stretch (Optional)**
Add minimal logging + cancel/stop control to a sample agent.

---

## Week 6 — Building Agents from Scratch I: Agent Anatomy

**Reading**: Chapter 4: Sections 4.1–4.7

**Goals**

- Understand the execution loop: how an agent decides, acts, and updates state.
- Design tools with clear inputs/outputs and failure modes.
- Recognize when structured outputs make systems more reliable.

**Key Concepts**

- Tool calling as a reliability and capability upgrade over prompting.
- Structured output (schemas) to reduce ambiguity.
- Memory basics: short-term (conversation) vs long-term (knowledge/context).

**Session Outcome**
A shared implementation-agnostic agent execution loop.

**Baseline Group Exercise (Low-Dependency)**

- Build a **tool card deck** (index-card style, in a doc):
  - tool name, input, output, failure modes, safety notes
- Each participant contributes 1 tool card (real or hypothetical).
- As a group, decide where the tool fits in the execution loop.

**Stretch (Optional)**
Implement 1 tool + structured output.

---

## Week 7 — Building Agents from Scratch II: Middleware, Memory & HITL

**Reading**: Chapter 4: Sections 4.8–4.13

**Goals**

- Decide what must be logged/observed to debug and govern agents.
- Define when to require human approval (human-in-the-loop).
- Make memory policies explicit: what gets stored, when, and why.

**Key Concepts**

- Middleware as a control layer (logging, policy, safety checks).
- Tool approval for risky actions.
- Memory write strategies: automatic vs explicit; safe defaults.

**Session Outcome**
A safety/observability “minimum viable controls” checklist.

**Baseline Group Exercise (Low-Dependency)**

- For a chosen agent, decide:
  - what to log (model calls, tool calls, outcomes)
  - what requires approval (high-risk actions)
  - what should be stored (memory) and when
- Write one policy: “When X happens, require Y approval and log Z.”

---

## Week 8 — Computer-Use Agents and Interface Grounding

**Reading**: Chapter 5

**Goals**

- Determine when UI automation is justified vs APIs/tools.
- Understand the observation/action loop for computer-use agents.
- Identify fragility and safety concerns early.

**Key Concepts**

- Interface representations: text-based, image-based, hybrid.
- Action spaces: clicks, typing, navigation, forms.
- Grounding and robustness: what the agent “sees” must match reality.

**Session Outcome**
A “UI agent feasibility” rubric.

**Baseline Group Exercise (Low-Dependency)**

- Choose 2 tasks:
  - one that should use APIs
  - one that might require UI automation
- For each, fill a rubric:
  - observability (what can the agent see?)
  - action space (what can it do?)
  - fragility (what breaks?)
  - safety (what’s risky?)
  - fallback plan (what if UI changes?)

---

## Week 9 — Multi-Agent Workflows & Orchestration from Scratch

**Reading**: Chapter 6; Chapter 7: Sections 7.1–7.3

**Goals**

- Turn a workflow graph into an executable spec with checkpoints and recovery.
- Define termination and recovery in a way the whole group can review.
- Compare orchestration options by how they behave under failure.

**Key Concepts**

- Workflow runners and checkpoints for long tasks.
- Termination conditions: what “done” means.
- Recovery strategies: retry, fallback, human escalation.

**Session Outcome**
A testable workflow spec plus one termination rule.

**Baseline Group Exercise (Low-Dependency)**

- Using last week’s workflow graph, add:
  - a checkpoint policy (when to save state)
  - a termination rule (what “done” means)
  - a recovery rule (what to do on failure)

---

## Week 10 — Evaluation and Optimization of MAS

**Reading**: Chapter 10; Chapter 11: Sections 11.2–11.3

**Goals**

- Define success criteria that are measurable and aligned to user value.
- Build a small evaluation suite that enables iteration.
- Use failure modes to decide what to fix first.

**Key Concepts**

- Task suites and scoring rubrics.
- Trajectories/traces as evaluation artifacts (not just final outputs).
- Judges: rule-based checks vs LLM-as-judge; trade-offs and safeguards.

**Session Outcome**
A 5-task evaluation suite and scoring rubric.

**Baseline Group Exercise (Low-Dependency)**

- Brainstorm 10 candidate tasks; pick 5 that are:
  - representative
  - easy to understand
  - measurable
- Define success criteria that don’t require ML expertise:
  - correctness checks, completeness checks, format checks, and a 1–5 usefulness score.

**Stretch (Optional)**
Implement LLM-as-judge and compare with rule-based scoring.

---

## Week 11 — Distributed Agents and Protocols

**Reading**: Chapter 12

**Goals**

- Decide when distribution is necessary vs over-engineering.
- Identify trust boundaries and what data/actions must be constrained.
- Understand how protocols like MCP/A2A help with interoperability and separation.

**Key Concepts**

- Distributed requirements: ownership boundaries, security, network constraints.
- Tool servers and standardized interfaces (MCP) and agent-to-agent coordination (A2A).
- Security posture: least privilege, approvals, and auditing across boundaries.

**Session Outcome**
A boundary diagram showing when distribution is warranted.

**Baseline Group Exercise (Low-Dependency)**

- Draw a system boundary diagram:
  - what runs in one process
  - what must be separate (security, ownership, network)
  - what data cannot cross boundaries
- Decide whether MCP/A2A is justified for one scenario.

---

## Week 12 — Ethics, Responsible AI, and Capstone Synthesis

**Reading**: Chapter 13 + (Chapter 14 or 15)

**Goals**

- Identify ethical and safety risks unique to agents that can act.
- Apply practical defenses (policy, middleware, approvals, monitoring).
- Synthesize the course into a capstone design that non-experts can review.

**Key Concepts**

- Agentic risk: emergent behavior, misuse, automation bias, “agentic noise”.
- Defense in depth: policy + logging + approvals + least privilege.
- Capstone as a coherent design: agents, tools, orchestration, UX controls, evaluation.

**Session Outcome**
A capstone design that’s reviewable by non-experts.

**Baseline Group Exercise (Low-Dependency)**

- Create a “capstone poster” (one page):
  - problem statement (plain language)
  - agents + roles
  - tools + approvals
  - orchestration choice + why
  - evaluation plan
  - top 3 risks + mitigations
- Presentations are scored on clarity, not code.

**Stretch (Optional)**
Partial implementation + demo trace.
