# Appendix

## What the thesis actually promises (§5.1.2 p.56, §5.10.1 p.82–83)

Only two items are explicitly promised as "provided in the Appendix." Both are fulfilled below.

| File | Fulfills | Thesis reference |
|---|---|---|
| [`A_flue_gas_flow_rate_validation.ipynb`](A_flue_gas_flow_rate_validation.ipynb) | Derivation of the flue-gas flow-rate conversion (Eq. 5.1) and verification against Kim & Léonard's (2025) published Nwaoha et al. (2018) benchmark case (TEC reproduced to within 1.1%) | §5.1.2 (p. 56), §5.10.1 (p. 82) |
| [`B_gbm_calibration_synthetic_test.ipynb`](B_gbm_calibration_synthetic_test.ipynb) | Known-answer synthetic test of the EU ETS GBM calibration function: simulates a series with known parameters and recalibrates, confirming volatility recovers reliably while drift does not. Independently re-verified against the raw ETS data in this repository (§B.7) | §5.9.3 (p. 81), §5.10.1 (p. 82–83), §8.4 (p. 108) |

Both notebooks use functions copied verbatim from `model/CCS_TEA_Model.ipynb` (Cells 7, 9, and 37),
so they validate the actual code behind the thesis's results, not a re-implementation.

## Good practice, not a thesis promise

These are included for transparency and reproducibility. They are not claims made anywhere in the
thesis text, and should not be cited as fulfilling a promise.

| File | Purpose |
|---|---|
| [`C_equation_to_cell_index.md`](C_equation_to_cell_index.md) | Navigation table: thesis section/equation → notebook cell number |
| [`D_code_and_data_availability.md`](D_code_and_data_availability.md) | Repository structure, data sources, environment/versioning, frozen-submission tag |
