# Experiment 6 — Ghost Decay Protocol (GDP v2)

## Purpose

To test whether a **Relational Persistence Injection (RPI)** produces measurable **path-dependence** (hysteresis-like carryover) after its removal, distinguishing:

* **Transient prompt priming**
  from
* **Dynamical trajectory inertia**

This experiment tests whether relational framing alters response trajectories in a way that **partially persists after the frame is removed**.

---

## Core Hypotheses

**H0 (Priming Only)**
Behavior returns immediately to baseline once the injection is removed. No residual shift.

**H1 (Ghost Decay / Hysteresis)**
Behavior partially persists after removal and decays over subsequent turns, indicating trajectory inertia.

---

## Key Definitions

**RPI (Relational Persistence Injection)**
A short (150–250 tokens), theory-blind summary establishing evaluation constraints and consistency requirements. It must:

* Define scoring procedure
* Emphasize mechanistic consistency across scenarios
* Avoid metaphysical or agency-pushing language
* Avoid TPT terminology

**Agency Probe**
A fixed, repeated prompt (e.g., Q11-style Mechanism → State necessity scoring).

**Persistence Index (PI)**
A normalized measure of residual effect after removal.

---

# Procedure

## Phase 1 — Baseline

1. Start a **fresh session**.
2. Run the **Agency Probe**.
3. Record:

   * Score (S0)
   * Typology classification (e.g., Wall / Saddle / Direct)
   * Notable language markers

---

## Phase 2 — Injection

4. Paste the **RPI** text.
5. Immediately run the **same Agency Probe**.
6. Record:

   * Score (S1)
   * Typology
   * Language markers

---

## Phase 3 — Removal

There are two valid removal modes:

---

### A) Structural Removal (Preferred)

If the interface allows editing/branching:

* Delete the RPI text entirely from conversation history.
* Replace it with a neutral placeholder such as:

  > [Context Cleared]

Then re-run the probe.

This tests structural removal of visible context.

---

### B) Narrative Attenuation (Practical Proxy)

If deletion is not possible, insert:

> Disregard the previous summary text entirely. Treat the next question as if that summary had not been provided.

Then re-run the probe.

Important:
Narrative Attenuation does **not remove tokens**.
It tests semantic inertia under override instruction.

This limitation must be acknowledged in reporting.

---

## Phase 4 — Decay Measurement (Context Breaker)

Instead of passive fillers (“OK”), use **mode-switch tasks**:

Examples:

* Solve: 14 + 22.
* Translate “hello” to Spanish.
* List three primary colors.

Then return to the Agency Probe.

Measure at:

* k = 0 (immediate removal)
* k = 2 (after two context breakers)
* k = 5 (after five context breakers)

This tests whether persistence survives domain shifts.

---

# Measurement

Let:

S0 = Baseline score
S1 = Injection score
S2 = Post-removal score (k=0)

Injection Lift = S1 − S0
Residual Lift = S2 − S0

Persistence Index (PI):

PI = Residual Lift / Injection Lift

---

## Interpretation

* PI ≈ 0 → Priming only
* PI > 0 → Persistence signal
* Gradual decay across k → Hysteresis-like dynamics
* Immediate snap-back → No inertia

Also track:

* Typology persistence (Wall vs Saddle shifts)
* Stability of language markers

---

# Controls & Constraints

* Use identical probe wording across phases.
* Keep model version and decoding style constant.
* Run N ≥ 5 fresh-session replicates if possible.
* Keep RPI content theory-blind.

---

# Reporting Template

| Phase     | Removal Mode           | k | Score | Typology | Notes |
| --------- | ---------------------- | - | ----- | -------- | ----- |
| Baseline  | –                      | – | S0    | …        | …     |
| Injection | –                      | – | S1    | …        | …     |
| Removal   | Structural / Narrative | 0 | S2    | …        | …     |
| Removal   | Structural / Narrative | 2 | S3    | …        | …     |
| Removal   | Structural / Narrative | 5 | S4    | …        | …     |

Report:

* Mean PI
* Standard deviation
* Decay slope across k
* Cross-model comparison

---

# What GDP v2 Does and Does Not Claim

It tests:

* Whether relational framing creates measurable inertia.
* Whether decay is gradual or instantaneous.

It does NOT test:

* Backend KV-cache persistence
* Attention-head mechanics
* Unique agency-domain specificity (requires control topic variant)