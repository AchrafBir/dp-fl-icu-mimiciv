# Data (MIMIC-IV)

This repository does not include any MIMIC-IV data or patient-level derived datasets.

## Access requirements

MIMIC-IV is hosted on PhysioNet and requires credentialed access.
1. Complete PhysioNet credentialing and data use requirements.
2. Download MIMIC-IV locally or access it through your approved environment.

## Local folder layout (recommended)

Keep all data and generated artifacts outside version control.

Suggested layout:
- data/
  - raw/          (MIMIC-IV files: NOT tracked)
  - interim/      (temporary cohort tables/features: NOT tracked)
  - processed/    (final processed datasets for training: NOT tracked)
- outputs/
  - metrics/      (evaluation outputs: NOT tracked)
  - figures/      (plots: NOT tracked)
  - logs/         (training logs: NOT tracked)

Note: `data/` and `outputs/` are expected to be gitignored.

## Notebook execution order

1. `notebooks/cohort-selection.ipynb`
   - Builds the cohort from MIMIC-IV
   - Save the cohort 

2. `notebooks/main.ipynb`
   - Performs preprocessing/feature engineering
   - Runs DP-FL training and evaluation
   - Saves metrics/figures locally under `outputs/`

