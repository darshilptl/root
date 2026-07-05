# Root — Desktop Application

> The interface layer of Root.
> Linear-inspired design. Minimal by design.

---

## The principle

Root is not a chatbot. The interface is not the product.

The intelligence running beneath the surface is the product. The desktop application exists for one purpose — to let you see what Root knows, adjust what Root can do, and give direct instruction when you want it.

Most of the time, you will not need to open it.

---

## Design direction

The interface follows a Linear-inspired design system. Clean. Fast. Zero visual noise. Every element earns its place.

The design principle: the interface should feel like an extension of the OS, not a separate application. It should appear when you need it and disappear when you do not.

**Typography** — system font stack. No decorative typefaces. Information hierarchy through weight and size, not colour.

**Colour** — minimal. One accent colour. Everything else is neutral. Dark mode first.

**Motion** — purposeful. Transitions exist to communicate state change, not to decorate.

**Density** — high information density without feeling cluttered. Every pixel is intentional.

---

## What the interface surfaces

**Activity view** — what Root has done in the current session and recent sessions. Every action logged with a reason and a timestamp. Traceable back to the permission that allowed it.

**Knowledge view** — what Root currently knows about you. The model it has built. Categories of understanding. How confident it is in each pattern. You can review, correct, or delete any entry.

**Permission editor** — a visual interface for `permission.yaml`. Every permission category visible. Toggle to enable or disable. Changes saved to the file. Take effect on next boot.

**Proactive queue** — what Root is planning to do before you ask. Actions it has queued based on learned patterns. You can approve, reject, or modify each one before it executes.

**Direct instruction** — a command interface for when you want to tell Root something explicitly. Not a chat window. A direct instruction field. Root executes within its permission boundaries.

---

## What the interface does not have

No dashboard with vanity metrics. No onboarding wizard. No notification centre. No social features. No settings page with fifty toggles.

If it does not help you understand what Root is doing or control what Root can do — it is not in the interface.

---

## Status

Interface specified. Design system defined.
Implementation private. Build starts after Interwave ships its core.

---

*Part of the Root Layer 0–9 architecture.*
*Full architecture — [spec/architecture.md](./architecture.md)*