---
name: helix-onboarding-matrix
version: 0.1
date: 2026-06-21
status: stable
custodian: Stephen Hope
section: Practice Guide
audience: Everyone
prerequisite: how-to-helix-your-workflow
---

# Helix Onboarding Matrix
**Skill Progression: Novice → Master**  
**Date:** 2026-06-21  
**Custodian:** Stephen Hope

---

## The Skill Ladder

| Level | Label | Relationship to the Verb | Time to Reach |
|---|---|---|---|
| 0 | **Unaware** | Has never encountered the concept. Generates output without epistemic structure. | — |
| 1 | **Novice** | Explicitly applies the taxonomy as a checklist. Slow, deliberate, mechanical. | Immediate |
| 2 | **Competent** | Labels automatically for unfamiliar tasks. Unlabeled for routine ones. Recognizes drift in others' output. | 2–4 weeks of practice |
| 3 | **Expert** | The labels are internalized. Shapes form before articulation. Can Helix a session for someone else. | 1–3 months |
| 4 | **Master** | Helixes processes, not just tasks — meetings, projects, organizational decisions. The verb becomes a leadership practice. Can design new taxonomies for new domains. | 3–12 months |
| 5 | **Custodian** | Shapes the grammar itself. Recognizes when the existing taxonomy is insufficient and extends it. Trains other custodians. | Ongoing |

---

## Domain Matrix

What Helixing looks like at each level across common workflows.

### Code

| Level | Behavior |
|---|---|
| **Novice** | Writes labels in prompt comments. `# [FACT] the API returns JSON`. Checks each line before asking AI to generate. |
| **Competent** | Helixes the spec, not the code. Writes labeled requirements doc, feeds to AI, reviews output against labels. |
| **Expert** | Helixes the architecture before splitting tickets. Team members start adopting the habit from exposure. |
| **Master** | Helixes the sprint planning — labels what the team knows, doesn't know, is guessing about the upcoming work. |
| **Custodian** | Extends the taxonomy for code-specific drift (type safety, test coverage, dependency risk). |

### Design

| Level | Behavior |
|---|---|
| **Novice** | Labels each design decision in a doc. `[REASONED] choosing Postgres for consistency guarantees`. |
| **Competent** | Opens every design doc with a Helix block — facts, inferences, hypotheses, uncertainties, conclusion. |
| **Expert** | Helixes in real time during whiteboard sessions. The team hears "is that a fact or a hypothesis?" |
| **Master** | Helixes the design review process itself — labels what the review is expected to surface vs. what's out of scope. |
| **Custodian** | Defines design drift codes specific to architectural patterns. |

### Code Review

| Level | Behavior |
|---|---|
| **Novice** | Labels review comments. `[UNCERTAIN] I don't understand this control flow path`. |
| **Competent** | Runs a Helix Check on the entire diff before writing any comments — labels the review scope first. |
| **Expert** | Helixes the PR description requirements so contributors surface uncertainty before submitting. |
| **Master** | Helixes the review rotation — who's reviewing what, what they know, what they're guessing about. |
| **Custodian** | Designs review-specific invariants. |

### Strategy / Decision-Making

| Level | Behavior |
|---|---|
| **Novice** | Labels options in a decision doc. |
| **Competent** | Helixes the landscape before evaluating options — facts about the market, reasoned inferences, hypotheses, uncertainties. |
| **Expert** | Runs Helix Checks on meeting agendas. The meeting itself becomes a Helix session. |
| **Master** | Helixes the quarter — what does the org know, not know, need to discover before Q2 planning. |
| **Custodian** | Designs strategy-specific drift codes (market risk, execution risk, timing risk). |

### Hiring / Team-Building

| Level | Behavior |
|---|---|
| **Novice** | Labels requirements in a job description. |
| **Competent** | Helixes the interview rubric — what signals are facts vs. reasoned assessments vs. hypotheses. |
| **Expert** | Helixes the hiring process: what does the team know it needs, what is it guessing about. |
| **Master** | Helixes team composition — surfaces gaps in collective knowledge vs. skill. |
| **Custodian** | Defines organizational drift codes. |

---

## Transition Patterns

### Novice → Competent

**Trigger:** The labels start to feel natural. You no longer need the cheat sheet.

**Risk:** Premature automation — reaching for the runtime before the verb is internalized.

**Avoidance:** Don't use the HCC API until you've Helixed 50+ sessions without it. The runtime amplifies skill it doesn't replace.

### Competent → Expert

**Trigger:** You start Helixing for others, not just yourself.

**Risk:** Assuming everyone sees the shape the same way you do.

**Avoidance:** Always surface your labels explicitly when Helixing a session with someone else. Don't skip the `[UNCERTAIN]` step just because you're experienced.

### Expert → Master

**Trigger:** You start Helixing processes, not just tasks.

**Risk:** Bureaucratization — the verb becomes a form to fill out rather than a practice.

**Avoidance:** If your Helix Check takes longer than 60 seconds, you're doing it wrong. The shape should emerge fast. If it doesn't, you need more data, not more labels.

### Master → Custodian

**Trigger:** You encounter a situation the existing taxonomy cannot describe.

**Risk:** Over-extension — adding labels that dilute the system rather than strengthen it.

**Avoidance:** Every new label must answer: "Does this surface a type of uncertainty that was previously invisible?" If yes, add it. If no, you're just renaming.

---

## Runtime Integration Points

| Level | Runtime Feature | What It Enables |
|---|---|---|
| Novice | HCC API / chat demo | Experience the Helix Check without building infrastructure |
| Competent | EVAC journal | Audit trail of Helixed sessions — review your own progression |
| Expert | FSM + INNY | Automated enforcement of epistemic boundaries + drift monitoring |
| Master | Custom drift codes | Extend the taxonomy for domain-specific signals |
| Custodian | Runtime source | Modify the runtime itself to support new governance patterns |

The runtime is a scaffold for the verb. Use it to accelerate, not to replace.
