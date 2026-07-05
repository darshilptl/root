# Root — RAG Self-Learning Pipeline

> Layer 7 — Self-Learning & Adaptation
> How Root learns who you are without being told.

---

## The problem with every other AI

Every AI you have used starts from zero every time.

You open a new chat. You re-explain your context. You describe your project. You tell it how you think. It processes the session, gives you an answer, and forgets everything the moment you close the window.

The context you built last Tuesday is gone. The pattern it noticed last month — gone. The way you structure your thinking, the shortcuts you take, the problems you return to — invisible.

This is not a product limitation. It is an architectural one. Cloud-dependent AI cannot learn you because learning you requires living with you.

---

## What the RAG pipeline does

RAG — Retrieval-Augmented Generation — is the architectural mechanism that makes Root's learning possible.

The pipeline runs continuously in the background while Root is active. It observes your work across sessions and builds a continuously refined model across three dimensions.

**How you think.** The structure of your decisions. What you reach for first when solving a problem. How you move from question to answer. The mental models you apply repeatedly.

**How you work.** Your actual workflow — the sequence of applications, the files you return to, the tasks you do on specific days, the way you organise your projects.

**What you reach for before you name it.** The patterns beneath the patterns. The thing you always do before starting a new project but have never consciously articulated. Root notices this before you do.

---

## How it learns

The pipeline does not require narration. You do not feed it information. You do not tell it what you are doing. It infers from observation.

Each session, Layer 1 (Perception) captures environmental context. Layer 7 receives this context, processes it against everything previously learned, and updates the knowledge model in Layer 4. The update is incremental — each session makes the model slightly more accurate, not dramatically different.

The model is stored entirely on your local machine. Nothing is sent to an external server. Nothing is used to train any external model. Your behavioural data is yours and it stays yours.

---

## The six-month arc

Root is not useful on day one the way a chatbot is useful on day one.

Week one — Root is observing. The model is sparse. Actions are conservative. It does what you explicitly ask and nothing more.

Month one — patterns begin to emerge. Root starts recognising recurring tasks. Simple automations begin. The proactive layer starts forming hypotheses.

Month three — Root knows your work rhythms. It anticipates recurring tasks. It prepares context before you need it. The suggestions become accurate.

Month six — Root surprises you. Not with a notification. With a thing already done — before you opened the application to do it yourself. The model has enough depth to act anticipatorily with confidence.

This arc is intentional. An AI that knows you after six months is worth far more than a chatbot that impresses you on day one and forgets you by day two.

---

## What the pipeline does not do

It does not record your screen continuously. It captures context at significant moments, not as a surveillance feed.

It does not log your keystrokes. Keystroke data is never captured at any layer.

It does not train external models. The learning is local, personal, and private.

It does not share data across users. Root's model of you is built entirely from your behaviour and exists only on your machine.

---

## Status

Pipeline designed. Architecture complete.
Implementation private. Build starts after Interwave ships its core.

---

*Part of the Root Layer 0–9 architecture.*
*Full architecture — [spec/architecture.md](./architecture.md)*