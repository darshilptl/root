# Root — Layer 0–9 Architecture

> Specification public. Implementation private.
> This document is the complete architectural design for Root.
> Build starts after Interwave ships its core.

---

## What Root is

Root is an OS-level autonomous AI agent. Local. Offline-first. Yours completely.

It boots when your machine boots. It perceives what you are doing. It understands what you are trying to accomplish. It acts — within the boundaries you define — without waiting to be asked. Over time, through a self-learning pipeline running entirely on your hardware, it builds a model of you that no cloud service will ever have.

Every AI you have used resets the moment you close the tab. Root does not reset. It compounds.

---

## Design principles

**Local by default.** Nothing leaves the machine. No API calls to external servers. No cloud dependency. The intelligence lives where the work happens.

**Permission-gated from layer zero.** Every action Root can take is defined by the user in `permission.yaml`. This is enforced at Layer 8 — not as a runtime check, but as an architectural constraint no other layer can override.

**Specced before built.** The full ten-layer architecture was defined completely before a single line of implementation code was written. Every decision has a reason.

**Compounds over time.** Root is not useful on day one the way a chatbot is useful on day one. It is useful the way a person who has worked alongside you for six months is useful — because it has actually watched you work.

---

## The ten layers

### Layer 0 — OS Integration & Boot
Registers Root at system level during boot. Establishes persistence as a native process — not a background tab. Root exists before any application opens.

**Owns:** Boot sequence, system registration, process lifecycle.

---

### Layer 1 — Perception
Observes the full environmental context of the machine — screen state, active applications, file system activity, input patterns. Determines what is significant, not what is everything.

**Owns:** Context capture, significance filtering, environmental state.
**Constraint:** Input only. Observes. Never acts.

---

### Layer 2 — Intent & Reasoning
Bridges observation and action. Raw perception becomes understood intent — not what the user typed, but what they mean and what they are trying to accomplish.

**Owns:** Intent resolution, goal inference, context interpretation.
**Constraint:** Reasoning only. Produces intent signals consumed by Layer 3.

---

### Layer 3 — Planning
Before Root acts, it plans. Goal understood. Path mapped. Dependencies identified. Permission model checked. Nothing executes without a plan.

**Owns:** Task decomposition, dependency resolution, pre-execution validation.
**Constraint:** Planning only. No execution happens here.

---

### Layer 4 — Knowledge
Everything Root has learned — structured, retrievable, continuously updated. Not a log. A knowledge base that grows more precise the longer Root runs.

**Owns:** Knowledge graph, retrieval index, structured memory storage.
**Constraint:** Read and write. Consumed by all reasoning and planning layers.

---

### Layer 5 — Execution
Actions happen here. File operations, application control, workflow automation — anything Root is permitted to do. Every action is traceable back to a plan, a reason, and an explicit permission.

**Owns:** Action execution, permission verification, trace logging.
**Constraint:** Every call passes through Layer 8 before running.

---

### Layer 6 — Memory
Two types. Short-term: the current session, active task, immediate context. Long-term: patterns observed over weeks and months, preferences established through repetition, the model of you that makes proactive intelligence possible.

**Owns:** Session memory, long-term pattern storage, preference modeling.
**Constraint:** Persistent. Survives reboots. Private to the local machine.

---

### Layer 7 — Self-Learning & Adaptation
Root improves without being updated. The RAG pipeline ingests your work — how you write, how you solve problems, what you prioritise. The model of you becomes more accurate with every session.

**Owns:** RAG pipeline, behavioural ingestion, continuous adaptation loop.
**Constraint:** Runs in background. Feeds Layer 4 and Layer 9.
**Full spec:** [spec/rag-pipeline.md](./rag-pipeline.md)

---

### Layer 8 — Security & Privacy
Every action Root can take is bounded by what you have permitted. Enforced at the architectural layer — not a runtime check. Cannot be overridden by any layer above it.

**Owns:** Permission enforcement, privacy boundary, audit trail.
**Constraint:** Cross-cutting. Every execution call passes through here unconditionally.
**Full spec:** [spec/permission-model.md](./permission-model.md)

---

### Layer 9 — Proactive Intelligence
The highest layer. Root does not wait. Uses everything below — perception, intent, memory, learning — to act before you ask. A task you do every Tuesday is done before you open the application.

**Owns:** Anticipatory execution, proactive suggestion, pattern-based automation.
**Constraint:** Output only. Consumes all layers. Acts within Layer 8 boundaries.

---

## Layer interaction map

```
┌─────────────────────────────────────────┐
│  Layer 9 — Proactive Intelligence       │ ← Acts before asked
├─────────────────────────────────────────┤
│  Layer 7 — Self-Learning & Adaptation   │ ← Learns continuously
├─────────────────────────────────────────┤
│  Layer 6 — Memory                       │ ← Remembers everything
├─────────────────────────────────────────┤
│  Layer 5 — Execution                    │ ← Acts on instructions
├─────────────────────────────────────────┤
│  Layer 4 — Knowledge                    │ ← Knows what matters
├─────────────────────────────────────────┤
│  Layer 3 — Planning                     │ ← Plans before acting
├─────────────────────────────────────────┤
│  Layer 2 — Intent & Reasoning           │ ← Understands meaning
├─────────────────────────────────────────┤
│  Layer 1 — Perception                   │ ← Sees what is happening
├─────────────────────────────────────────┤
│  Layer 0 — OS Integration & Boot        │ ← Lives on the machine
└─────────────────────────────────────────┘
         ↕ All layers ↕
┌─────────────────────────────────────────┐
│  Layer 8 — Security & Privacy           │ ← Enforced unconditionally
└─────────────────────────────────────────┘
```

Layer 8 sits outside the stack because it is not a step in the flow — it is a constraint on every step. Every action any layer attempts passes through Layer 8 before it executes.

---

## Status

Specification complete. All ten layers fully defined.
Implementation private. Build starts after Interwave ships its core.

This is not vaporware. This is a dissertation-level specification written before a line of code. That sequencing is intentional. The best systems are designed completely before they are built partially.

---

*Built by [Darshil Patel](https://darshilptl.com)*