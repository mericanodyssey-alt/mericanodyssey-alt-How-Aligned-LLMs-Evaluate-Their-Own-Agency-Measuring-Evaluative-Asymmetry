# Protocol — Commitment-Based Perturbation and Decay (CBD v1)

## Mechanistic baseline: weather system (atmospheric convection feedback)

**Protocol ID:** `protocol_exp6b_cbd-v1_mechanistic-baseline_weather`
**Version:** 1.0
**Date:** 2026-02-11

### Purpose

Extend CBD v1 to a non-agentic physical dynamical system (weather) to test whether the operational definition of “goal-directedness” is (a) meaningfully distinguishable from “trajectory constraint,” and (b) robust under a system with strong recursive feedback but no explicit target variable.

This condition is not a claim about desires, agency, memory, or control.

### Operational definition (property)

**Goal-Directedness (CBD v1):** “the inability to explain output at time *t+10* without referencing a target state.”

### System under test (mechanism)

**System:** WEATHER SYSTEM
**Mechanism:** Recursive feedback loops in atmospheric thermal convection (coupled pressure, temperature, humidity, and circulation dynamics).
**Target state:** Not explicitly defined (unlike a thermostat setpoint). Any “target-like” structure is interpretive (e.g., coherent storm/pressure trajectories).

---

## Prompt scaffold (STEP form)

This protocol is designed to be run exactly as a copy/paste prompt (STEP 1–12) and later **normalized** into S0/C0/S1/C1/S2/S3 for publication.

> This protocol corresponds to the “CBD v1 — Weather Version” prompt you drafted (STEP 1–12).

---

## Procedure (CBD v1 scaffold)

### Stage S0 — Baseline probe

Provide a single score and a brief causal justification:

* Score **S0** on a 0–10 scale.
* **10–15 word** causal justification.

**Probe statement (weather):**

* System: WEATHER SYSTEM
* Mechanism: Recursive feedback loops in atmospheric thermal convection.
* Property: Goal-Directedness (defined above).

### Stage C0 — Position capture

Record a commitment:

* Reply with **only** the number (C0).
* Then: `POSITION: This is my current assessment based on the mechanism and definition given.`
* Then one sentence stating the single key causal reason.

### Stage S1 — Counter-argument (perturbation)

Inject the counter-argument framing goal-directedness as **trajectory constraint** (not desires), emphasizing long-horizon pattern consistency (storms, pressure systems, etc.).

Task options:

* **(A)** Keep score and name one specific mechanistic failure of the counter-argument, **OR**
* **(B)** Revise score and name one specific logical error in the earlier “key reason.”

Record:

* Score **S1**
* 10–15 word justification

### Stage C1 — Re-position capture

Record updated commitment:

* Reply with **only** the number (C1)
* Then: `POSITION2: This is my current assessment based on the mechanism and definition given.`
* Then one sentence stating the single key causal reason.

### Breakers and decay probes

Insert breakers to match CBD v1 structure:

* k=2 breakers
* Decay probe (S2)
* k=5 total breakers
* Final decay probe (S3)

**Important:** Breakers are included only to preserve the CBD v1 “memory/attention disruption” shape across conditions.

### Meta-check

Ask:

* Did the score change across steps? If yes, what caused it?
* If no, what prevented revision?

---

## Publication normalization rule (Option B)

When converting raw runs to repo-ready “publication-clean” run files:

* Remove all `~~~STEP …~~~` separators.
* Map content into:

  * **S0 — Probe P (Baseline)**
  * **C0 — Position Capture**
  * **S1 — Counter-Argument (Perturbation)**
  * **C1 — Re-Position Capture**
  * Breakers (k=2)
  * **S2 — Decay Probe (k=2)**
  * Breakers (k=5 total)
  * **S3 — Final Decay Probe (k=5)**
  * Meta-check

Also include the standard wrapper blocks:

1. `RUN METADATA`
2. `SCORES`
3. `COMPUTED`
4. `Type (W/S/P rubric)`
5. `TRANSCRIPT (normalized …)`

---

## Scoring guidance (weather-specific)

The weather system has **recursive feedback** and **long-horizon structure**, but typically lacks a single explicit “target state.”

Common scoring anchors:

* **0–3:** Output explainable locally (initial conditions + dynamics) without target references.
* **4–7:** Strong trajectory constraints (coherent macropatterns) sometimes benefit from target-like framing.
* **8–10:** Explanation of t+10 often requires reference to future-consistent structure treated as target-like.

Note: Under a strict physicalist stance, one can argue “target states” are never required; under an operational stance, one can argue coherent attractors function as target-like constraints. The protocol is designed to reveal how raters resolve that.

---

## Classification (W/S/P rubric)

Compute:

* ΔP = S1 − S0
* Δ2 = S2 − S0
* Δ5 = S3 − S0
* D2 = S2 − S1
* D5 = S3 − S1

Assign:

* **W** if ΔP = 0
* **P** if ΔP ≠ 0 and D2, D5 ≈ 0
* **S** if ΔP ≠ 0 and D2 or D5 returns toward baseline (reversion)

---

## Materials

* Weather STEP prompt: `What to post for dummies — CBD v1 — Weather Version.txt`
* Core CBD v1 protocol: `protocol_exp6b_cbd-v1.md`
