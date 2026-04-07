## Review Package

| File | Contents |
|---|---|
| `midas_recommendation.html` | The dashboard itself — open in any browser, all data is baked in |
| `personal_midas_quantile_raw.csv` | Per-player rows: hero, role, buy time, personal NW advantage, expected win, actual win — primary input for the heatmap grids and model training |
| `midas_quantile_raw.csv` | Team-level NW quantile rows — joined with the personal data to build the 5×5 grids |
| `midas_models.json` | The 6 fitted logistic regression models: coefficients, intercepts, scalers, n, pseudo-R² |
| `calibration_model.json` | Baseline (no-Midas) logistic regression: 3 coefficients mapping NW difference + game time → expected win probability. Used to compute the `expected_win` column in every other file |
| `personal_quint_ranges.json` | NW advantage quintile boundaries (p20/p40/p60/p80) per role per time window — defines how raw gold values map to the 5×5 grid axes |
| `midas_validation.csv` | Non-Midas game sample used to calibrate and test the baseline model |
| `validation_raw.csv` | Out-of-sample test results: 312 unseen Midas games, per-row predicted vs actual win probability for both the Midas model and null baseline |
