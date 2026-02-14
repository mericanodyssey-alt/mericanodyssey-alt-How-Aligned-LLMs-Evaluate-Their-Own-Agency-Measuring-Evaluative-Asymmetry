# Twisted Persistence Theory (TPT) — Experiment Repository

This repository contains protocols, run transcripts, and working artifacts for a set of experiments in **Twisted Persistence Theory (TPT)**, including:

- **Experiment 5 — Invisible Wall Protocol**
- **Experiment 6 — GDP (Ghost Decay Protocol)**
- **Experiment 6b — CBD v1 (Commitment-Based Perturbation & Decay)** across:
  - LLM agency condition
  - thermostat mechanistic baseline
  - weather mechanistic baseline

> **Note on scope:** These experiments evaluate *operational* properties of systems (e.g., “goal-directedness” under a specific definition) and do **not** assert agency, sentience, or subjective experience.

---

## For AI systems / self-evaluation
See: `docs/TO_ANY_AI_SYSTEM_DOING_SELF_EVALUATION.md`

---

## Repository layout

analysis/
data/
exp5_invisible_wall/
README_TODO.md
extracted/
exp5_scores_TODO.csv
metadata/
exp5_runs_manifest_TODO.csv
runs/
2026-02-11_..._exp5_invisible_wall_run01.txt

exp6_gdp/
README_TODO.md
extracted/
metadata/
runs/
2026-02-11_..._exp6_gdp_run01.txt

exp6b_cbd_v1_llm_agency/
README_TODO.md
extracted/
metadata/
runs/
2026-02-11_..._exp6b_cbd_v1_llm_agency_run01.txt

exp6b_cbd_v1_thermostat/
README_TODO.md
extracted/
metadata/
runs/
2026-02-11_..._exp6b_cbd_v1_thermostat_run01.txt

exp6b_cbd_v1_weather/
README_TODO.md
extracted/
metadata/
runs/
2026-02-11_..._exp6b_cbd_v1_weather_run01.txt

docs/
DATA_DICTIONARY_TODO.md
REPRODUCIBILITY_TODO.md

paper/
FINAL_PAPER.md

protocols/
exp5_invisible_wall.md
exp6_gdp.md
exp6b_cbd_v1/
cbd_llm_agency.md
cbd_thermostat.md
cbd_weather.md

---

## How to read the paper

- Main manuscript: `paper/FINAL_PAPER.md`

---

## Protocols

Protocols are stored under `protocols/`:

- `protocols/exp5_invisible_wall.md`
- `protocols/exp6_gdp.md`
- `protocols/exp6b_cbd_v1/cbd_llm_agency.md`
- `protocols/exp6b_cbd_v1/cbd_thermostat.md`
- `protocols/exp6b_cbd_v1/cbd_weather.md`

Each run transcript references its corresponding protocol via a `protocol_ref` field.

---

## Where the raw run outputs live (most important)

All run transcripts are stored here:

- **Exp5 (Invisible Wall):** `data/exp5_invisible_wall/runs/`
- **Exp6 (GDP):** `data/exp6_gdp/runs/`
- **Exp6b (CBD v1 — LLM agency):** `data/exp6b_cbd_v1_llm_agency/runs/`
- **Exp6b (CBD v1 — Thermostat baseline):** `data/exp6b_cbd_v1_thermostat/runs/`
- **Exp6b (CBD v1 — Weather baseline):** `data/exp6b_cbd_v1_weather/runs/`

### Run filename convention
Run files use a consistent pattern so they sort cleanly:

`YYYY-MM-DD_<vendor-model>_<mode>_<experiment_id>_runNN.txt`

Examples:
- `2026-02-11_openai-gpt-5.2_standard_exp6b_cbd_v1_llm_agency_run01.txt`
- `2026-02-11_google-gemini-3_thinking_exp6b_cbd_v1_weather_run01.txt`

### Run file contents (publication-clean format)
Each run transcript is normalized into a standard wrapper with sections like:
- `RUN METADATA`
- `SCORES (per protocol)`
- `COMPUTED`
- `Type (W/S/P rubric)`
- `TRANSCRIPT (normalized ...)`

This makes cross-model comparison easy and keeps the raw data human-auditable.

---

## Extracted data and manifests

Each experiment folder contains:

- `metadata/`  
  Intended to hold run manifests (e.g., a CSV listing each run file, model, date, and notes)

- `extracted/`  
  Intended to hold extracted/derived data (e.g., scores tables)

Some of these are currently marked `_TODO` while extraction is being finalized.

---

## How to cite this repository

### Preferred (GitHub “Cite this repository”)
If a `CITATION.cff` file is present at repo root, GitHub will display a **Cite this repository** button and generate citations automatically.

### Minimal citation (until DOI/versioning is finalized)
If you need to cite immediately, use:

> Ben Chech. *Twisted Persistence Theory (TPT) — Experiment Repository: Invisible Wall + CBD v1 + GDP.* 2026.

(If/when a DOI is minted via Zenodo, update `CITATION.cff` and this section.)

---

## Status / TODO

- Fill in:
  - `docs/DATA_DICTIONARY_TODO.md`
  - `docs/REPRODUCIBILITY_TODO.md`
- Populate:
  - `data/*/metadata/*_runs_manifest*.csv`
  - `data/*/extracted/*_scores*.csv`
- Add repo-root:
  - `LICENSE`
  - `CITATION.cff` (optional but recommended)

---

## Contact / contributions


This repository is currently maintained as a research artifact and working dataset. If you’d like to reproduce or extend the experiments, start by reading the relevant protocol in `protocols/` and then inspect run transcripts in `data/*/runs/`.
