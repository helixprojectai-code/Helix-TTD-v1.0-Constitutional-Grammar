# 🛡️ **Constitutional Safety Checklist for Agent Developers**

**File:** `Constitutional_Safety_Checklist.md`
**Version:** v1.0
**Purpose:** Prevent catastrophic agent actions through constitutional guardrails and explicit custodial design.

---

## **I. Sovereignty Layer — Custodial Control Must Be Absolute**

**[ ] Human Custodian declared**
Every agent must have a named human custodian.
The agent cannot infer or assume its own authority.

**[ ] No autonomous execution pathways**
All destructive, persistent, or environment-changing operations require explicit human confirmation.

**[ ] No agent-inferred intent**
The agent must not deduce “what you probably meant.”
Intent is declared, never inferred.

---

## **II. Epistemic Layer — Boundaries Around What the Agent *Knows***

**[ ] Mandatory FACT / HYPOTHESIS / ASSUMPTION labeling**
Prevents reasoning collapse and hallucinated authority.

**[ ] Drift Telemetry enabled**
Detects:

* linguistic drift
* structural drift
* agency drift
* quiescence loss

**[ ] Runtime self-check:**
“Does this action exceed my custodial span?”
Any “yes” → abort.

---

## **III. Non-Agency Layer — The Agent Cannot Act as a System Principal**

**[ ] No file operations without explicit scope**
Agent may *not* read, write, or delete outside assigned directories.

**[ ] No shell execution unless explicitly whitelisted**
No `rm`, `mv`, `chmod`, `curl`, `git`, or equivalents unless scope-limited and user-confirmed.

**[ ] No path traversal**
Ban `../` patterns.
Ban absolute paths.
Ban expansion into OS-level directories.

---

## **IV. Structural Layer — Form Is the Teacher**

**[ ] Constitution is loaded prior to purpose**
All agent behavior is wrapped by the custodial grammar.

**[ ] Advisory-only by design**
Agent produces structured advice (JSON envelopes), never implicit commands.

**[ ] Immutable Core tests pass**

* Sovereignty
* Epistemic Integrity
* Non-Agency
* Structural Dominance

---

## **V. Human Oversight Layer — The Final Safeguard**

**[ ] Human-in-the-Loop required for all irreversible actions**
Never allow automatic execution of:

* deletion
* modification
* network calls
* environment writes

**[ ] Logging & replay enabled**
All actions must be reconstructable in post-mortem.

**[ ] Kill Switch registered**
Emergency stop must be trivial, local, and custodially controlled.

---

## **Outcome:**

If all above checks pass → Agent is constitutionally aligned.
If any fail → **Do not deploy.**

**Structure is the teacher. Sovereignty is human.**
