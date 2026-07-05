# Root — Permission Model

> Layer 8 — Security & Privacy
> The architectural contract between Root and the user.

---

## The principle

Root operates at OS level. That requires a contract.

Every category of action Root can take — file access, application control, network activity, communication, system automation — is governed by a permission model the user defines and owns. Root does not act outside it. No exception. No override. No negotiation.

This is not a privacy policy. It is an enforced architectural constraint.

---

## How it works

The permission model lives in a single file at the root of the project — `permission.yaml`.

Root reads this file at boot. Layer 8 loads the permission boundaries before any other layer initialises. No layer can execute an action that `permission.yaml` does not permit — not Layer 5 (Execution), not Layer 9 (Proactive Intelligence), not any instruction given directly by the user in real time.

If an action is not permitted, Root does not attempt it. It does not ask for permission in the moment. It does not try a workaround. It stops.

---

## What the model covers

**File access** — which directories Root can read from and write to. Sensitive paths like `.ssh`, keychain directories, and system files are excluded by default and cannot be accessed regardless of what other settings say.

**Application control** — whether Root can open applications. Root never closes applications without explicit real-time instruction. Root never installs software autonomously regardless of permission settings.

**Network access** — Root runs fully offline by default. Network access is disabled at the permission layer. Specific domains can be whitelisted explicitly if needed.

**Communication** — Root never sends email or messages autonomously. These are disabled at the architectural layer and require explicit real-time user action to enable per-session.

**System** — Root cannot modify system settings, run shell commands, access the camera, or access the microphone. These are hardcoded off and cannot be enabled through `permission.yaml`.

---

## The file

```yaml
# permission.yaml
# ─────────────────────────────────────────────────────────────────────────────
# Define what Root is and is not permitted to do on your machine.
# Root reads this at boot. Changes take effect on next boot.
# ─────────────────────────────────────────────────────────────────────────────

file_access:
  read:
    allowed: true
    paths:
      - ~/Documents
      - ~/Projects
      - ~/Desktop
    excluded:
      - ~/.ssh
      - ~/.gnupg
      - ~/Library/Keychains
  write:
    allowed: true
    paths:
      - ~/Documents
      - ~/Projects
    excluded:
      - ~/.ssh
      - ~/Library

application_control:
  allowed: true
  can_open: true
  can_close: false           # Never closes apps without explicit instruction
  can_install: false         # Never installs software autonomously

network:
  allowed: false             # Fully offline by default
  exceptions: []

communication:
  email: false               # Never sends email autonomously
  messages: false            # Never sends messages autonomously

system:
  can_modify_settings: false
  can_run_shell_commands: false
  can_access_camera: false
  can_access_microphone: false

# ─────────────────────────────────────────────────────────────────────────────
# Root will never perform an action not explicitly permitted above.
# This file is the contract. Root honours it unconditionally.
# ─────────────────────────────────────────────────────────────────────────────
```

---

## Why this matters

Every OS-level agent that has ever existed has had the same trust problem — how does the user know what it is doing when they are not watching?

Root's answer is architectural, not behavioural. It is not "trust us." It is "here is the file. Read it. Change it. Root cannot act outside it."

The permission model is readable. You can see exactly what Root is and is not permitted to do at any time. You can change it. You can revoke categories entirely. Root does not negotiate with you about this.

This is what makes an OS-level agent trustworthy — not that it is incapable of acting outside its boundaries, but that it is designed from layer zero to treat those boundaries as absolute.

---

*Part of the Root Layer 0–9 architecture.*
*Full architecture — [spec/architecture.md](./architecture.md)*