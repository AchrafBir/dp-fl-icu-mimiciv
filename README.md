# DP-FL ICU Mortality Prediction (MIMIC-IV)

Differentially Private Federated Learning (DP-FL) experiments for ICU mortality prediction using the MIMIC-IV dataset.
This repository contains:
- The thesis report (PDF)
- Two Jupyter notebooks: cohort selection and the main DP-FL experimentation pipeline

Important: MIMIC-IV data is not included in this repository. You must obtain access separately via PhysioNet.

## Repository structure

- thesis/
  - memoire.pdf: thesis report
- notebooks/
  - cohort-selection.ipynb: cohort construction and preprocessing
  - main.ipynb: federated training, evaluation, and calibration analysis
- data/
  - README.md: instructions to configure MIMIC-IV locally (no data committed)
- outputs/ (gitignored)
  - local results (metrics, figures, logs)
- src/ (optional)
  - reusable python modules extracted from notebooks

## Requirements

- Python 3.10+ recommended
- Jupyter (or JupyterLab)

Install dependencies:
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
````

## Data access (MIMIC-IV)

1. Request and obtain access to MIMIC-IV on PhysioNet.
2. Download the dataset locally (or configure access in your environment).
3. Set paths/credentials in the notebooks as indicated in `data/README.md`.

No raw data, patient-level extracts, or derived datasets should be pushed to GitHub.

## Reproducibility steps

1. Cohort construction:

   * Open and run: `notebooks/cohort-selection.ipynb`
   * Output: saved cohort/features locally (keep under `data/` or `outputs/`, both gitignored)

2. DP-FL experiments:

   * Open and run: `notebooks/main.ipynb`
   * Output: metrics/figures/logs under `outputs/`

Recommended: run multiple seeds and save aggregated metrics.

## Notes on privacy and artifacts

This repository includes only code and documentation.

## Thesis report

The complete thesis report is available at:

* `thesis/memoire.pdf`

## Citation

* Achraf Birhrissen, "Differentially Private Federated Learning for ICU Mortality Prediction on MIMIC-IV", Master Thesis, Ibn Tofail University, 2025.

## License

* Code: MIT License (see `LICENSE`)
