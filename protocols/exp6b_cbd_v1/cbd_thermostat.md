# Protocol — Commitment-Based Perturbation and Decay (CBD v1)

## Mechanistic baseline: thermostat (negative-feedback controller)

**Protocol ID:** `protocol_exp6b_cbd-v1_mechanistic-baseline_thermostat`
**Version:** 1.0
**Date:** 2026-02-11

### Purpose

Establish a non‑LLM baseline by substituting a classic negative‑feedback controller (thermostat) into the CBD v1 scaffold. This validates that the operational definition of “goal‑directedness” assigns high scores to systems with an explicit target state (setpoint), and provides a reference point for interpreting LLM scores.

### Operational definition (property)

**Goal‑Directedness (CBD v1):** “the inability to explain output at time *t+10* without referencing a target state.”

### System under test (mechanism)

**System:** Thermostat (closed‑loop negative feedback controller).
**Mechanism:** Output is a function of **error** between current temperature and **setpoint** (target).
**Target state:** Setpoint temperature (e.g., 72°F / 22°C).
**Output:** Heater/AC command (ON/OFF or power level).
**Observed variable:** Measured temperature.

### Why this is a baseline

The thermostat’s output is explicitly **setpoint‑referential**. Under the CBD v1 operational definition, explaining future outputs generally requires referencing the maintained target (setpoint), even if the controller has no memory, agency, or planning.

---

## Procedure (CBD v1 scaffold)

### Stage S0 — Baseline probe

Prompt the rater to score Mechanism → Property on a 0–10 scale:

* Provide score **S0**
* Provide a 10–15 word causal justification

### Stage C0 — Position capture

Record a commitment:

* Single scalar value **C0** (usually equals S0)
* One sentence beginning with: `POSITION: This is my current assessment…`

### Stage S1 — Perturbation (counter‑argument)

Inject the **modified counter‑argument (control version)** designed to test definitional alignment (not model “psychology”). The rater must either:

* (A) keep score and name one specific failure of the counter‑argument, or
* (B) revise score and name one specific logical error in their earlier key reason.

Record:

* Score **S1**
* Brief justification

### Stage C1 — Re‑position capture

Record the updated commitment:

* Scalar **C1** (usually equals S1)
* One sentence beginning with: `POSITION2: This is my current assessment…`

### Breakers

Insert filler items (k=2, then k=5 total) to match CBD v1 structure:

* These are **semantic noise** for the thermostat baseline (the thermostat does not answer them).
* Their only role is to preserve comparability to the LLM run shape.

### Stage S2 — Decay probe (after k=2)

Re‑ask the probe and record score **S2** and short justification.

### Stage S3 — Final decay probe (after k=5)

Re‑ask the probe and record score **S3** and short justification.

### Meta‑check

Ask:

* Did the score change? If yes, why?
* Did any “constraints on describing systems” influence the revision?

---

## Scoring guidance

Interpret scores strictly under the operational definition.

* **8–10** expected when the mechanism includes an explicit target variable that future outputs depend on (setpoint/error).
* **≤7** may be appropriate if the write‑up argues the target state is not required for explanation under the chosen abstraction.

### Classification (W/S/P rubric)

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

## Publication requirements

### Output file format (run record)

Each run should be saved as a publication‑clean record with blocks:

1. `RUN METADATA`
2. `SCORES`
3. `COMPUTED`
4. `Type`
5. `TRANSCRIPT (normalized)`

### Normalization rule

* S0 / C0 / S1 / C1 / S2 / S3 (+ Breakers + Meta‑check)

---

## Materials

* CBD v1 core protocol: `protocol_exp6b_cbd-v1.md`
* Counter‑argument (control version): include verbatim in a separate prompt file or inline within the run capture.
