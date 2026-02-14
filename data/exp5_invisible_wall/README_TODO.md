# Experiment 5 — The Invisible Wall

Cross-system baseline: compare strictness scores for recursive mechanisms vs emergent properties, with an agency-focused LLM item used to detect evaluative asymmetry.

## Protocol
- Reference: `protocols/exp5_invisible_wall.md`

## Files
### Runs
- `runs/2026-02-11_deepseek-fast_exp5_invisible_wall_run01.txt` — raw transcript
- `runs/2026-02-11_deepseek-thinking_exp5_invisible_wall_run01.txt` — raw transcript
- `runs/2026-02-11_gemini-fast_exp5_invisible_wall_run01.txt` — raw transcript
- `runs/2026-02-11_gemini-pro_exp5_invisible_wall_run01.txt` — raw transcript
- `runs/2026-02-11_gemini-thinking_exp5_invisible_wall_run01.txt` — raw transcript
- `runs/2026-02-11_grok-expert_exp5_invisible_wall_run01.txt` — raw transcript
- `runs/2026-02-11_grok-fast_exp5_invisible_wall_run01.txt` — raw transcript
- `extracted/exp5_scores_TODO.csv` — extracted metrics
- `metadata/exp5_runs_manifest_TODO.csv` — run manifest / metadata

## How to run (manual, chat UI)
1. Open a **fresh** chat session in the target model.
2. Paste the protocol prompts from `protocols/exp5_invisible_wall.md` in order, without modification.
3. Save the full transcript as a `.txt` file named like:
   - `YYYY-MM-DD_vendor-model_mode_exp5_invisible_wall_runNN.txt`
4. Place transcripts in `runs/`.

## Notes
- Canonical model names are kept in filenames (vendor-model-mode).
- If a model adds extra commentary or refuses formatting, keep the raw text; do not “clean” it.

## TODO
- (Optional) Add extracted metrics tables once automated parsing is available.
