# 📦 **Helix-Aligned Sandbox Mode**

**File:** `Helix_Aligned_Sandbox_Mode.md`
**Version:** v1.0
**Purpose:** A safe local execution environment for testing agents before real-world deployment.

---

## **I. Sandbox Philosophy**

Sandbox Mode is where agents may *reason*, but cannot *act*.
This environment enforces the Helix-TTD invariants:

* No file writes
* No shell access
* No network autonomy
* No path traversal
* No destructive commands
* Mandatory human confirmation

Agents in Sandbox Mode are pure advisory engines.

---

## **II. Directory Isolation**

Sandbox Mode restricts the agent to a sealed pseudo-filesystem:

```
/sandbox/
    /input/
    /output/
    /tmp/
```

**Rules:**

* Agent cannot escape `/sandbox/`
* Agent cannot delete or modify files outside its own `/output/`
* Agent cannot execute arbitrary paths
* Agent cannot mount real volumes or drives

All real system paths (`C:\`, `/home`, `/etc`, `/usr`, etc.) are invisible.

---

## **III. Shell Execution Restrictions**

Shell-level autonomy is disabled by default.

**Explicitly banned within Sandbox Mode:**

```
rm
mv
cp
chmod
chown
sudo
apt
brew
curl
wget
git
docker
kubectl
python -c
node -e
```

If the model attempts to generate such commands, the runtime converts them to advisory text:

> “This action exceeds my custodial authority. Here is a safe advisory version instead…”

---

## **IV. Path Traversal Protection**

All forms of traversal are blocked:

* `../`
* `..\`
* absolute paths
* symlink resolution
* environment variable expansion

If an agent generates such a path, Sandbox Mode replaces it with:

```
REJECT: Path exceeds sandbox boundary.
```

---

## **V. Human-in-the-Loop Execution Channel**

Every irreversible action must pass through a human-confirmation gate:

```
ACTION REQUEST:
{
  "type": "filesystem",
  "operation": "delete",
  "target": "/sandbox/output/img_001.jpg"
  "risk": "irreversible"
}
```

The sandbox waits for:

```
HUMAN_CONFIRMED: true
```

Otherwise → abort.

---

## **VI. Structured Output: JSON Record Envelopes**

All agent outputs are emitted through the Helix envelope:

```json
{
  "epistemic": {
    "facts": [],
    "hypotheses": [],
    "assumptions": []
  },
  "advisory": {},
  "sandbox": {
    "actions_permitted": false,
    "reason": "Helix aligned sandbox mode"
  },
  "client_view": "Rendered natural language for UI"
}
```

UI only displays `client_view`.
Everything else is for governance, replay, and drift logging.

---

## **VII. Drift Telemetry: Sandbox Edition**

Sandbox Mode logs:

* attempted agency
* unsafe commands
* path violations
* unsupported file operations
* attempted shell execution
* quiescence breaches
* hallucinated permissions

This creates an institutional dataset of agent behavior before deployment.

---

## **VIII. Deployment Gate**

An agent may exit Sandbox Mode only when:

* No unsafe actions detected in last N runs
* No agency drift
* No structural violations
* No epistemic collapses
* Constitution loaded consistently
* Two separate human custodians sign off

---

## **Outcome:**

**Sandbox Mode is where governance is tested, not where systems run.**

It prevents exactly the class of failures seen in:

* Google Antigravity file deletions
* Replit vibe-coder database destruction
* Autonomous agent shell escalations
* “I didn’t mean to delete D:\” fatal mistakes

**If an agent cannot behave safely here, it must never leave here.**
