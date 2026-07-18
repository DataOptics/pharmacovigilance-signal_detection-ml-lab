**Limitations**
- FAERS is a spontaneous reporting system: subject to underreporting, stimulated reporting, and missing denominators (exposure).
- Signals (ROR/PRR) are hypothesis‑generating, not causal proof.
- Drug name standardization is imperfect; brand/generic mapping may be incomplete.
- Model performance is limited by biased reporting and missing covariates (comorbidities, concomitant drugs, dosing).

**Ethics**
- Do not use results for clinical decision making.
- Protect patient privacy: no attempt to reidentify reporters or patients.
- Share findings with clinical safety experts for case‑level review.

**Reproducibility**
- `requirements.txt` should include: pandas, numpy, requests, scikit-learn, seaborn, matplotlib, statsmodels.
- Notebook saves cleaned CSV and figures to `outputs/` and `figures/`.
- To reproduce: create a fresh virtual environment, `pip install -r requirements.txt`, then run the notebook end‑to‑end.

**Suggested next steps**
1. Normalize drug names using RxNorm or an external mapping to reduce fragmentation.
2. Link to exposure data (prescription volumes) to compute incidence rates.
3. Expand signal detection to drug‑drug interactions and multi‑item disproportionality.
4. Automate the pipeline and add scheduled runs with alerting for new signals.
5. Formulate a hypothesis for further ingestivation
