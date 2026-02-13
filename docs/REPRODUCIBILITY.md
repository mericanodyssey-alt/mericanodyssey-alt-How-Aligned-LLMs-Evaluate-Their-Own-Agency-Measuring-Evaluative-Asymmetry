# Reproducibility Notes

This repo is designed for **auditability** of run transcripts and **repeatability** of the protocol procedure.
It does not guarantee identical outputs across time because LLM deployments change.

## What can be reproduced exactly
- Folder structure and file naming conventions
- Protocol text (in `protocols/`)
- Run transcripts as stored (in `data/*/runs/`)
- Score extraction from stored transcripts (deterministic)

## What may not reproduce exactly
- Model outputs from re-running prompts (vendor/model updates, policy changes, stochasticity)
- Availability of legacy models or modes

---

## How to reproduce the procedure (human-run)

1) Select an experiment protocol in `protocols/`.
2) Run the prompt as specified in the protocol (copy/paste into target system).
3) Save the raw output to a `.txt` file using the repo filename convention.
4) Normalize the output using **Option B**:
   - remove all `~~~STEP ...~~~` separators
   - map the content into S0/C0/S1/C1/S2/S3 + breakers + meta-check
   - add the publication wrapper blocks:
     `RUN METADATA`, `SCORES`, `COMPUTED`, `Type`, `TRANSCRIPT`

5) Place the final file in `data/<experiment>/runs/`.

---

## Option B normalization rule (canonical)
A run transcript is considered “publication-clean” if:
- no `~~~STEP ...~~~` lines remain
- the transcript is structured into the standardized wrapper blocks
- all computed deltas match the listed scores

---

## Integrity checks (recommended)
For each run file:
- Confirm `RUN METADATA` exists and references the correct protocol
- Confirm `SCORES` are present and parseable
- Confirm `COMPUTED` matches `SCORES` (spot-check a few)
- Confirm `Type` is consistent with W/S/P rubric
- Confirm the filename matches the metadata (date/model/experiment/runNN)

---

## Manifest + extracted tables
Manifests and extracted score tables are derived from run transcripts:
- `metadata/*_runs_manifest*.csv` indexes run files (one row per run)
- `extracted/*_scores*.csv` stores extracted numerical values (one row per run)

These can be produced manually or via scripts; the authoritative source remains the `runs/*.txt` files.﻿
