# Layer 0 — OS Integration & Boot

## Responsibility
Registers Root at system level during boot. Establishes persistence as a native process — not a background tab. Root exists before any application opens.

## What this layer owns
Boot sequence, system registration, process lifecycle.

## Scope
OS-level. Runs before any user application.

## Status
Specification complete. Implementation private.
Build starts after Interwave ships its core.

---
*Part of the Root Layer 0–9 architecture.*
*Full specification — root/spec/architecture.md*