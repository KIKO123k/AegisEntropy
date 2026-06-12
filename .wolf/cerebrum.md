# Cerebrum

> OpenWolf's learning memory. Updated automatically as the AI learns from interactions.
> Do not edit manually unless correcting an error.
> Last updated: 2026-06-12

## User Preferences

<!-- How the user likes things done. Code style, tools, patterns, communication. -->

## Key Learnings

- **Project:** AegisEntropy-main
- ML pipeline for PortScan detection on CICIDS2017 (`Friday-WorkingHours-Afternoon-PortScan.pcap_ISCX.csv`). Pipeline order: `data_preprocessing.py` → `feature_selection.py` → `modeltrain.py` → `evaluate_model.py`; `predict.py` is standalone CLI inference.
- All scripts use `../`-relative paths — they must be run from inside `src/`.
- The dataset CSV lives in `data/` which is gitignored; it is NOT in the repo and must be obtained separately.
- On the HEAD branch, `FEATURES` (9 features) is centralized in `src/config.py`; the merged-in branch e24bc1ea duplicated the list inline in each script. When resolving conflicts, prefer the `config.py` import.
- Models train with 2 placeholder columns (`shadow_node_interaction`, `mtd_port_delta`, both 0) appended after the 9 features — scaler/models expect 11 columns in that order.
- Trained artifacts already exist in `models/` (rf, xgb, iso forest, scaler) and metrics in `results/metrics.csv` (RF/XGB ≈0.999 F1; Isolation Forest performs poorly, F1 0.079).

## Do-Not-Repeat

<!-- Mistakes made and corrected. Each entry prevents the same mistake recurring. -->
<!-- Format: [YYYY-MM-DD] Description of what went wrong and what to do instead. -->

## Decision Log

<!-- Significant technical decisions with rationale. Why X was chosen over Y. -->
