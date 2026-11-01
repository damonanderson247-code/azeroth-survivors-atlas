# Updating the live Build Atlas via GitHub

1. Receive a new Run Recorder ZIP and inspect the actual source data/screenshot evidence. Separate assisted accelerated tests from 1× unassisted clears.
2. Fetch existing `data/updates.json` from the published GitHub repository.
3. Append a unique `runs[]` record, with `id`, `date`, `class`, `spec`, `boss`, `outcome`, `game_time`, `speed_multiplier`, `assisted`, `conditions`, `total_damage_m`, `avg_dps_k`, `final_boss_dps_k`, `summary`, `source`, and any verified damage breakdown. Unknown numbers stay omitted instead of guessed.
4. Where warranted, update `route_overrides["Class/Spec"]`. `field_evidence_append` appends evidence to an existing route; other properties (e.g. `status`, `measured_damage`, `test_next`, `measured_context`) overwrite the corresponding route field.
5. Commit **only `data/updates.json`** (and a small evidence screenshot if useful) to `main` through the GitHub connector. Pages refreshes the same website URL. Open the live website to confirm the new run appears.
6. Preserve history and avoid duplicating runs. If the user hasn't shared a new ZIP, nothing updates automatically.

The initial victory (Shadow Priest, 2026-11-01, 5× assisted) is already in `data/site.json` and must not be duplicated in `data/updates.json`.
