# Root

> Every AI you've ever used lives in a tab. Resets when you close it. Forgets you exist.
> Root lives on your machine. Learns who you are. Works before you ask.

---

## What this is

Root is an OS-level autonomous AI agent. Local. Offline-first. Yours completely.

It boots when your machine boots. It perceives what you are doing. It understands what you are trying to accomplish. It acts — within the boundaries you define — without waiting to be asked. And over time, through a self-learning pipeline that runs entirely on your hardware, it builds a model of you that no cloud service will ever have: how you think, how you work, what you reach for before you name it.

Every AI product you have used resets the moment you close the window. Root does not reset. It compounds.

This is not an assistant. It is not a chatbot. It is not a wrapper around an API.

It is infrastructure with intelligence. Built from layer zero.

---

## Why this exists

Every existing AI assistant fails at the same thing.

It does not know you. It cannot know you. It lives on someone else's server, processes your request, and forgets you the moment the session ends. The context you built last Tuesday is gone. The pattern it noticed last month — gone. The way you structure your thinking, the shortcuts you take, the problems you return to — invisible. Every conversation starts from zero.

This is not a product limitation. It is an architectural one. Cloud-dependent AI cannot learn you because learning you requires living with you. On your machine. In your environment. Across your actual work — not the work you choose to describe in a prompt.

Root is built on a different architectural premise entirely. The agent lives where the work happens. It learns from the work as it happens. It does not need to be told what you are doing because it already knows.

---

## The layer architecture

Root is designed across ten layers. Each layer has a single responsibility. Each one is necessary. None of them are optional.

**Layer 0 — OS Integration**
The foundation. Root registers at system level during boot. It exists before any application opens. This is where persistence is established — not as a background tab, but as a process that is as native to the machine as the OS itself.

**Layer 1 — Perception**
Root observes. Screen state, active applications, file system activity, input patterns — the full environmental context of what is happening on the machine at any moment. It does not record everything. It understands what is significant.

**Layer 2 — Intent and Reasoning**
Raw perception becomes understanding. What is the user trying to accomplish right now? Not what did they type — what do they mean? This layer bridges observation and action by establishing intent before anything is executed.

**Layer 3 — Planning**
Before Root acts, it plans. The goal is understood. The path to the goal is mapped. Dependencies are identified. Conflicts with the permission model are checked before a single action is taken. Nothing executes without a plan.

**Layer 4 — Knowledge**
Everything Root has learned about you, your work, your domain, your preferences — structured, retrievable, continuously updated. This is not a log. It is a knowledge base that grows more precise the longer Root runs.

**Layer 5 — Execution**
Actions happen here. File operations, application control, workflow automation, communication — anything Root is permitted to do. Execution is always traceable back to a plan, a reason, and an explicit permission.

**Layer 6 — Memory**
Two types. Short-term: the current session, the active task, the immediate context. Long-term: patterns observed over weeks and months, preferences established through repetition, the model of you that makes proactive intelligence possible. Memory is what separates an agent that assists from one that anticipates.

**Layer 7 — Self-Learning and Adaptation**
Root improves without being updated. The RAG pipeline ingests your work — not to surveil, but to understand. How you write. How you solve problems. What you prioritise. What you avoid. The model of you becomes more accurate with every session. At six months, Root knows things about how you work that you have never explicitly told it.

**Layer 8 — Security and Privacy**
Every action Root can take is bounded by what you have permitted. This is not a runtime check — it is an architectural constraint. The permission model is defined by you, enforced by the layer, and cannot be overridden by any other layer in the stack. Root does not do what you have not allowed. This is not a feature. It is the contract.

**Layer 9 — Proactive Intelligence**
The highest layer. Root does not wait. It uses everything below — perception, intent, memory, learning — to act before you ask. A task you do every Tuesday is done before you open the application. A pattern you repeat across projects is automated. A decision you are approaching is prepared for. This is what six months of learning makes possible.

---

## The self-learning pipeline

Root learns entirely on your hardware. Nothing leaves your machine.

The pipeline observes your work across sessions and builds a continuously refined model of three things: how you think, how you work, and what you reach for before you name it. It does not require you to narrate your work or provide feedback. It learns from the work itself.

The six-month arc is intentional. Root is not useful on day one the way a chatbot is useful on day one. It is useful the way a person who has worked alongside you for six months is useful — because it has actually watched you work, not because it was trained on a dataset of other people.

At six months, Root surprises you. Not with a notification. With a thing already done.

---

## The permission model

Root operates at OS level. That requires a contract.

Every category of action Root can take — file access, application control, network activity, communication, automation — is governed by a permission model you define and own. Root does not act outside it. No exception. No override.

The model is readable. You can see exactly what Root is and is not permitted to do at any time. You can change it. You can revoke categories entirely. Root does not negotiate with you about this.

This is the architectural principle that makes an OS-level agent trustworthy: not that it is incapable of acting outside its boundaries, but that it is designed from layer zero to treat those boundaries as absolute.

---

## What Root is not

Not a cloud service. Root runs entirely on your hardware. There is no server receiving your data, no API call leaving your machine, no subscription required for it to function.

Not a chatbot. Root does not wait for prompts. It perceives, reasons, plans, and acts. The chat interface exists for direct instruction — it is not the primary mode of interaction.

Not a general-purpose AI. Root knows you specifically. Its intelligence is built from your work, your patterns, your environment. It is not trained on the internet. It is trained on you.

Not spyware. Everything Root observes stays on your machine. The permission model is not a privacy policy — it is an enforced architectural constraint. Root cannot exfiltrate what the permission layer does not allow.

Not always-on surveillance. Root observes what is significant. It does not log your keystrokes. It does not record your screen. It understands context, it does not archive everything.

---

## The desktop interface

Root surfaces through a desktop application. Linear-inspired design — clean, fast, zero visual noise.

The interface is not the product. The intelligence running beneath it is. The interface exists to let you see what Root knows, adjust what Root can do, and give direct instruction when you want it. Most of the time, you will not need to open it.

---

## Status

Root is fully specified. The Layer 0–9 architecture is complete. The self-learning pipeline is designed. The permission model is defined. The desktop interface is planned.

Build starts after Interflow ships its core.

This is not a delay. It is a sequencing decision. Root is the most architecturally complex thing on the roadmap. It gets built when it can be built right — not when it can be built fast.

The specification is public because the thinking should be visible. The implementation is private because the product deserves to be built without being cloned before it exists.

---

## For engineers reading this

If you are a hiring manager, a CTO, or a senior engineer who has read this far — this document exists to show how Root was thought through, not to invite you to build it.

The layer architecture, the self-learning design, the permission model — these represent months of specification work done before a single line of code. That sequencing is intentional. The best systems are designed completely before they are built partially.

If you want to follow the build as it happens: [@darshilptl](https://twitter.com/darshilptl)

---

## A final note

Every AI company in the world is racing to build the most powerful model. Root is not competing in that race.

Root is competing in a different one — the race to build an AI that actually knows you. Not a version of you inferred from your search history. Not a persona constructed from your prompts. You. The way you actually think. The way you actually work. The way you actually move through a day.

That kind of intelligence cannot be built in a data centre. It has to live where you live.

That is what Root is building toward.

---

*Built by [Darshil Patel](https://darshilptl.com)*
*Specification public. Implementation private. Build in progress.*
