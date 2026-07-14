# Appendix C — Equation-to-Cell Index

A navigation aid, not a validation — this is not a promise made anywhere in the thesis text. Its only
job is to let a reader go from "which equation/section is this?" straight to the right cell in
`model/CCS_TEA_Model.ipynb`, without duplicating code that would go stale the moment the notebook is
updated. For validated derivations, see Appendix A and Appendix B instead.

| Thesis section / equation | Notebook cell | What it implements |
|---|---|---|
| §5.2 Currency and cost-conversion protocol | Cell 2–3 | CEPCI/EUR-NOK constants |
| §5.1 Case study parameters | Cell 4–5 | Design capacity scenarios (Table 5.1) |
| **Eq. 5.1**, §5.1.2 Flue gas flow rate | Cell 6–7 | `flue_gas_flow_F()` — see **Appendix A** for full derivation and validation |
| §5.4.2 Kim & Léonard (2025) correlations | Cell 8–9 | **Eq. 5.3** TEC, **Eq. 5.4** compression, **Eq. 5.8** electrical duty, **Eq. 5.9** cooling duty, Eliasson/Energiforsk cross-check |
| §5.4.3 DOE/NETL multiplier chain (TEC→TOC) | Cell 10–11 | `tec_to_toc()` — Base 1.85×, FOAK 2.50× |
| §5.4.6 CAPEX scaling exponent and cost-level uncertainty | Cell 12–13 | Uniform(0.55, 0.75) scaling exponent; Beta(2,3) cost-level multiplier |
| §5.5 FOAK ramp-up levelisation (Rubin et al. 2013, **Eq. C10**) | Cell 14–15 | `levelised_CF()` |
| §5.4.8 Operating costs | Cell 16–17 | Steam cost, reboiler duty, retrofit adder, solvent degradation, fixed O&M |
| §5.9.3 Electricity price OU calibration | Cell 18–19 | `calibrate_ou_electricity()`, `simulate_ou_electricity_paths()`, `draw_levelised_electricity_prices_ou()` |
| §5.6 Transport module — S1 offshore | Cell 20–21 | Truck + ship routing, unit rates |
| §5.7 Onshore storage (S2/S3) — discrete LOW/HIGH | Cell 22–23 | `well_storage_NOK_t()` — well-cost structural scenarios |
| **Eq. 5.12**, §5.8 Master LCOC function | Cell 24–25 | `compute_LCOC()` |
| §5.9.2 Monte Carlo — Common Random Numbers | Cell 26–27 | `run_MC_CRN()` |
| Pairwise comparison probabilities | Cell 28–29 | P(S2<S1), P(S3<S1) under CRN |
| §5.8 Financial metrics — NCAE, breakeven ETS, required grant | Cell 30–31 | Breakeven ETS price calculation |
| §5.1, §5.4.6 Structural scenario sweeps | Cell 32–33 | A/B/C design capacity, concentration, biogenic, heat pump, Eliasson, NL phase |
| §5.9.4 Sensitivity analysis | Cell 34–35 | OAT tornado, Spearman rank correlation |
| §5.9.3 Stochastic price processes (GBM + OU) | Cell 36–37 | `calibrate_gbm()`, `simulate_GBM()` — see **Appendix B** for the known-answer synthetic test |
| §5.7.5 S3 hub 2D grid | Cell 38–39 | Distance × volume sweep, 500 MC iterations/cell |
| §6 Key visualisations (Figures 1–9) | Cell 40–61 | Semantic colour palette, all headline and diagnostic figures |
| Chapter 6 results summary tables | Cell 62–63 | Headline LCOC table (mean, P10/P50/P90) |
| Version history | Cell 64 | Change log from prior v7 to v7 (corrected) |

**Note on cell numbering:** cell indices are 0-based and count both markdown and code cells (i.e.
"Cell 6–7" means the markdown header at index 6 and its associated code cell at index 7). If the
notebook is edited after this appendix is written, cell numbers may shift — the section headers
inside the notebook itself (`## 4. Flue Gas Flow Rate (Eq. 5.1, §5.1.2)`, etc.) are the more durable
reference and are what this table was built from.
