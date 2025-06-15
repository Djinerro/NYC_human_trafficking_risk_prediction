# 🛰️ Human Trafficking Risk Prediction (NYC, 2021–2024)

This project identifies spatio-temporal hotspots of **human trafficking (HT) risk** in New York City using multi-source data and predictive modeling techniques. It was developed in collaboration with Metro Analytics as part of the Rutgers MBS Advanced Analytics Practicum.

> **Techniques used:** Supervised LSTM modeling, XGBoost baselines, unsupervised clustering (HDBSCAN, KMeans), anomaly detection, spatial grid design, and real-world validation.

---

## 📌 Problem Statement

Human trafficking is a covert and often underreported crime, masked within broader categories like assault or sex work. Traditional data sources are sparse or misclassified, making direct detection extremely difficult.

This project builds a **multi-layered modeling pipeline** to forecast risk using indirect signals like:
- Crime patterns
- Event density
- Mobility flows
- Calendar and location context

---

## 🧠 Modeling Approach

- **Supervised Learning:**
  - XGBoost and LightGBM used as benchmarks
  - **LSTM** model trained on 7-day spatio-temporal sequences
  - Output: continuous risk score per (date, location)

- **Unsupervised Learning:**
  - **HDBSCAN & KMeans** used for spatial clustering
  - Identified organic hotspots of HT risk from raw coordinates

- **Contextual Validation:**
  - Socioeconomic overlays (poverty, unemployment)
  - Sentiment analysis on local businesses
  - Scraping illicit ad frequency data as future signal

---

## 📁 Project Structure

- `data/` – Sample datasets (geo-grid structure, sample events); full data sources listed below
- `notebooks/` – EDA, ML model trials, LSTM sequence modeling
- `src/` – Data wrangling scripts, grid assignment, feature engineering
- `models/` – Saved model weights and LSTM architecture
- `reports/` – Visualizations, ROC curves, clustering maps

---

## 📥 Data Sources

Due to GitHub file size limits, full datasets are **not uploaded**. You can recreate them using these sources and the code provided.

| Domain         | Dataset                     | Source                                            | Timeframe         |
|----------------|-----------------------------|---------------------------------------------------|-------------------|
| Crime          | NYPD Complaint Data         | NYC OpenData                                      | Jan 2021–Dec 2024 |
| Verified HT    | TAHub Metro NY Reports      | Metro Analytics (non-public)                      | Jan 2021–Dec 2024 |
| Events         | NYC Permitted Events        | NYC OpenData                                      | Jan 2021–Dec 2024 |
| Mobility       | JFK Passenger Volume        | Port Authority NY/NJ                              | Monthly (scaled)  |
| Geography      | NYC Borough Boundaries      | NYC GIS                                           | Static            |
| Calendar       | US Holidays & Weekends      | Public Calendar                                   | Jan 2021–Dec 2024 |

---

## 🧪 Results Snapshot

- **LSTM Model**: AUC = 0.77, Recall = 75% at 0.2 threshold
- **XGBoost Baseline**: AUC = 0.51, Recall = ~2%
- **Top features**: Borough, recent crime trends, passenger volume
- **HDBSCAN**: Found tight clusters with silhouette scores > 0.9

![](reports/risk_heatmap_sample.png)  
*Sample risk heatmap predicted by the LSTM model for May 14, 2024*

---

## 🧰 Tech Stack

- Python, Jupyter, Pandas, Scikit-learn, XGBoost, TensorFlow/Keras
- GeoPandas, Folium, Matplotlib, Seaborn
- Spatial clustering: HDBSCAN, KMeans
- Web scraping: BeautifulSoup
- APIs: Google Places, escortalligator

---

## 🔍 How to Reproduce

1. Clone this repo:
   ```bash
   git clone https://github.com/your-username/human-trafficking-risk-prediction.git
   ```
2. (Coming soon) Install dependencies and run notebooks/scripts as described in the upcoming documentation.

---

## 📄 Project Report

A full technical report is included in the `reports/` directory (to be added).

---

## 📫 Contact

For questions or collaboration, please reach out to [your.email@domain.com] or open an issue.

---

## ⚖️ License

This project will be released under an open-source license (to be specified).
