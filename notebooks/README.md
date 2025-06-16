# NYC Human Trafficking Risk Prediction – Model Fitting

## Overview

This folder contains the modeling pipeline and code for the project **NYC Human Trafficking Risk Prediction: Spatio-Temporal Machine Learning Pipeline**. The goal is to predict daily human trafficking (HT) risk across NYC locations using a combination of historical crime data, event occurrence, spatial features, and advanced machine learning/deep learning methods. This serves as the core component of my professional data science portfolio.

---

## Contents

- **NYC_HT_Risk_Modeling_Portfolio.ipynb**  
  The main Jupyter notebook containing:
    - Data loading and cleaning
    - Feature engineering
    - Baseline models (LightGBM, XGBoost)
    - LSTM deep learning pipeline for temporal patterns
    - Threshold tuning and risk mapping
    - Validation against real-world HT case data
    - Professional visualizations and interpretability analysis

- **images/**  
  Folder for figures and map screenshots referenced in the notebook or README.

- **data/**  
  (Not included for privacy; see Data section below.)

---

## Key Results & Visualizations

- **Borough-level risk trend plots** for 2021–2024
- **Interactive heatmaps** of predicted risk hotspots
- **Model vs. verified HT cases overlays** (e.g., Queens, citywide)
- **Funnel diagrams** illustrating risk detection and response workflow

See the notebook for all full-resolution plots and interpretations.

---

## Data

- The notebook expects data in CSV and NPZ format (see code for filenames).
- **Data files are NOT included** in this repo for privacy/legal reasons.
- If you wish to understand or extend the analysis, you may replace code with your own sample data in the correct format.

---

## Model Details

- **Tabular baseline models:**  
  LightGBM, XGBoost with feature engineering, categorical encoding, and class balancing.
- **Deep learning:**  
  LSTM sequence model for temporal risk pattern detection.
- **Validation:**  
  Extensive comparison vs. verified HT case reports from TAHub.

---

## Portfolio Highlights

- End-to-end rare event prediction: from raw data to actionable maps
- Clear, annotated notebook with professional plots
- Real-world validation and interpretability
- Ready for further extension or deployment

---

## Contact

**Author:** Djinerro  
**LinkedIn:** [Your LinkedIn Profile]  
**Email:** your.email@domain.com

---

> _For questions, collaboration, or data access requests, please open an issue or contact me directly._
