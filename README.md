# 🛰️ Human Trafficking Risk Prediction (NYC, 2021–2024)

This project identifies spatio-temporal hotspots of **human trafficking (HT) risk** in New York City using multi-source data and predictive modeling techniques. Developed with Metro Analytics as part of the Rutgers MBS Advanced Analytics Practicum.

> **Techniques:** Supervised LSTM modeling, XGBoost baselines, HDBSCAN/KMeans clustering, anomaly detection, spatial grid design, and real-world validation.

---

## 📌 Problem Statement

Human trafficking is a covert, underreported crime, often masked in other categories. Direct detection is challenging due to data sparsity and misclassification.

**This project builds a multi-layered pipeline to forecast risk using indirect signals** including:
- Crime patterns
- Event density
- Mobility flows
- Calendar and location context

---

## 🧠 Modeling Approach

- **Supervised Learning:**  
  XGBoost and LightGBM benchmarks; LSTM model on 7-day spatio-temporal sequences, outputting a continuous risk score per (date, location)
- **Unsupervised Learning:**  
  HDBSCAN & KMeans spatial clustering to identify organic risk hotspots
- **Contextual Validation:**  
  Socioeconomic overlays, sentiment analysis, and scraping illicit ad frequency data

---

## 📁 Project Structure

- `data/` – Sample datasets (full data not included; see sources below)
- `notebooks/` – EDA, ML modeling, LSTM sequence pipeline
- `src/` – Data wrangling scripts, grid assignment, feature engineering (placeholder)
- `models/` – Model weights/configs (not included in this public repo)
- `reports/` – Visualizations, ROC curves, clustering maps, technical report

---

## 📥 Data Sources

Due to GitHub file size and privacy, **full datasets are not uploaded**. See the notebook and report for data structure and use the sources below if you wish to experiment.

| Domain         | Dataset                     | Source                   | Timeframe         |
|----------------|-----------------------------|--------------------------|-------------------|
| Crime          | NYPD Complaint Data         | NYC OpenData             | Jan 2021–Dec 2024 |
| Verified HT    | TAHub Metro NY Reports      | Metro Analytics (private)| Jan 2021–Dec 2024 |
| Events         | NYC Permitted Events        | NYC OpenData             | Jan 2021–Dec 2024 |
| Mobility       | JFK Passenger Volume        | Port Authority NY/NJ     | Monthly (scaled)  |
| Geography      | NYC Borough Boundaries      | NYC GIS                  | Static            |
| Calendar       | US Holidays & Weekends      | Public Calendar          | Jan 2021–Dec 2024 |

---

## 🧪 Results Snapshot

- **LSTM Model:** AUC = 0.77, Recall = 75% at 0.2 threshold
- **XGBoost Baseline:** AUC = 0.51, Recall ≈ 2%
- **Top Features:** Borough, recent crime trends, passenger volume
- **HDBSCAN:** High silhouette (>0.9) for discovered clusters

![](reports/risk_heatmap_sample.png)  
*Sample risk heatmap (LSTM model, May 14, 2024):  
“Emerging risk hotspots are detected in midtown and certain event-dense neighborhoods.”*

---

## 🧰 Tech Stack

Python, Jupyter, Pandas, Scikit-learn, XGBoost, TensorFlow/Keras, GeoPandas, Folium, Matplotlib, Seaborn, HDBSCAN, KMeans, BeautifulSoup, Google Places API

---

## 📝 Usage & Reproducibility

This repository is a professional portfolio showcase.  
**Full data and models are not included** due to size/privacy.  
See the notebook and report for detailed methods and results.

---

## 📄 Project Report

A comprehensive technical report and presentation are included in the `reports/` directory.

---

## 📫 Contact

For questions or collaboration, open an issue or general question, connect with me using my link:  
[LinkedIn](https://www.linkedin.com/in/s-hashim-raza/)

---

## ⚖️ License

License to be specified (TBD).

---
