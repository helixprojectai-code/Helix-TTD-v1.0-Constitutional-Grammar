---
name: documentation-architecture
version: 0.1
date: 2026-06-21
status: draft
custodian: Stephen Hope
section: Governance
audience: Custodians
prerequisite: how-to-helix-your-workflow
---

# Helix Documentation Architecture
**A Universal Verb with a Software Implementation**  
**Date:** 2026-06-21  
**Custodian:** Stephen Hope

---

## Core Insight

Helix is not a software project that happens to have documentation.

Helix is a **universal practice** — the operation of making epistemic structure visible before committing to output. The software runtime is one implementation of that practice, at machine scale.

The documentation must reflect this hierarchy:

```
HELIX (THE VERB)
├── Practice Guides
│   ├── How to Helix Your Workflow      ← The foundational practice
│   ├── Language Is a Shape              ← The philosophical basis
│   ├── The Four-Label Taxonomy          ← The cognitive tool
│   ├── Helix Onboarding Matrix          ← The skill progression
│   ├── Visual Primitive Library         ← The symbolic language
│   └── Helix in Conversation            ← Verbal practice
│
├── The Software Runtime (Submodule)
│   ├── HCC API Reference                ← The OpenAI-compatible endpoint
│   ├── Constitutional Adapter            ← The wrapper implementation
│   ├── FSM Quarantine State Machine      ← State enforcement
│   ├── EVAC Journal                      ← Audit chain
│   ├── INNY Drift Daemon                 ← Monitoring
│   ├── Deployment Guide                  ← helix2vm, Docker, systemd
│   └── API Keys & Authentication         ← Access control
│
├── Governance
│   ├── Constitutional Grammar            ← The invariant rules
│   ├── Drift Taxonomy                    ← Measurable drift codes
│   ├── CHOMP Protocol                    ← Micro-ritual governance
│   └── Gap Preservation Order            ← Boundary conditions
│
└── Reference
    ├── Glossary
    ├── TEL Mesh Protocol
    └── Night Ops Logs
```

---

## Current State vs. Target State

| Aspect | Current | Target |
|---|---|---|
| **Entry point** | "Helix is an AI safety runtime" | "Helix is a practice you can apply anywhere. One powerful implementation is the software runtime." |
| **Document order** | API docs first, philosophy buried | Practice guides first, API docs as a linked sub-section |
| **Naming** | "Helix Constitutional Chat API" | "Helix Runtime — Chat Interface" |
| **Onboarding** | "Get your API key and make a request" | "Read the practice guide, try the Helix Check manually, then explore the runtime" |
| **Call to action** | "Try the demo" | "Helix your next task before you generate anything. Then try the demo." |

---

## File Reorganization

### Root Level (Grammar Repo)

These are the verb-level documents. They describe the practice.

| File | Purpose |
|---|---|
| `README.md` | "Helix is a verb." Brief explainer, links to practice guides and runtime. |
| `How_To_Helix_Your_Workflow.md` | The core practice guide (done). |
| `Language_Is_A_Shape.md` | Philosophical foundation (done). |
| `Helix_Onboarding_Matrix.md` | Skill progression map (done). |
| `Visual_Primitive_Library.md` | Symbolic language for diagrams (done). |
| *CONSTITUTIONAL_GRAMMAR.md* | The invariant rules (existing). |
| *drift_taxonomy.json* | Measurable drift codes (existing). |
| *CHOMP_Protocol.md* | Micro-ritual governance (existing). |

### Runtime Directory (`runtime/` or `adapter/`)

These describe the software implementation. They are referenced from the root but live in a subdirectory.

| File | Purpose |
|---|---|
| `runtime/API_REFERENCE.md` | Endpoint docs, request/response formats |
| `runtime/DEPLOYMENT.md` | Installation, configuration, systemd services |
| `runtime/AUTHENTICATION.md` | API keys, access control, rate limits |
| `runtime/FSM.md` | Quarantine state machine |
| `runtime/EVAC.md` | Audit journal |
| `runtime/INNY.md` | Drift monitoring daemon |
| `runtime/TEL.md` | Mesh protocol reference |

---

## Document Header Convention

Every document should declare its position in the hierarchy:

```yaml
---
section: Practice Guide        # or "Runtime Reference" or "Governance"
prerequisite: How_To_Helix_Your_Workflow.md  # what to read first
audience: Everyone             # or "Operators" or "Developers"
---
```

This lets readers (and LLMs) navigate by relevance, not by filename.

---

## The Key Header Rewrites

### Root README

Current framing:
> "Helix Constitutional Chat — a chat interface with constitutional guardrails."

Target framing:
> **Helix is a verb.** It is the practice of surfacing uncertainty before committing to output. This repository contains the constitutional grammar that defines the practice, and the software runtime that implements it at machine scale.
>
> **Start here:** [`How_To_Helix_Your_Workflow.md`](./How_To_Helix_Your_Workflow.md)
>
> **Try the runtime:** [`helixaiinnovations.ca/chat/`](https://helixaiinnovations.ca/chat/)

### Runtime Entry

Current framing:
> "Helix Adapter — wraps model outputs in constitutional compliance."

Target framing:
> **Helix Runtime** — one implementation of the Helix verb, automated at machine scale. Every API request runs through the epistemic pipeline: claim extraction, drift computation, receipt chaining, boundary enforcement. Use it when you need the practice to be rigorous, persistent, and machine-readable.

---

## Migration Path

| Phase | Action |
|---|---|
| **Phase 1** (now) | Add the practice documents to the grammar repo. |
| **Phase 2** | Rewrite root README to verb-first framing. |
| **Phase 3** | Create `runtime/` directory, move adapter docs. |
| **Phase 4** | Update external links, demo landing page, API docs. |
| **Phase 5** | Onboarding material — training deck, workshops, Helix Check cards. |
