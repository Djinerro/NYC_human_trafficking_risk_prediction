# 📁 Data Directory

## Overview
This directory contains sample data and instructions for sourcing and processing the full datasets used in the Human Trafficking Risk Prediction (NYC, 2021–2024) project. **Full datasets are not included** due to size, privacy, and licensing constraints.

## Contents

- **sample/**: Small, representative samples of each dataset for demonstration and testing.
- **scripts/**: (Optional) Scripts to help users download or process the original data.

## Data Sources & Sampling

| Domain      | Dataset                | Sample File                        | Original Source / Generation Method                | Notes                                     |
|-------------|------------------------|------------------------------------|---------------------------------------------------|-------------------------------------------|
| Mobility    | JFK Passenger Volume   | Passenger_volume_JFKinbound_2021_2024.csv | [Port Authority NY/NJ](https://www.panynj.gov/)   | Full file included (public)               |
| Verified HT | TAHub Metro NY Reports | sample_TAHub_NYC_Metro_Cases.csv   | Metro Analytics (non-public)                      | Anonymized sample, see methods            |
| Crime       | NYPD Complaint Data    | sample_nypd_complaints_2021_2024.csv | [NYC OpenData](https://opendata.cityofnewyork.us) | Sampled, 1000 rows from 2021              |
| Events      | NYC Permitted Events   | sample_filtered_events_v2.csv      | NYC OpenData                                      | Sampled 500 events                       |
| Geography   | NYC Borough Boundaries | sample_boroughs.geojson            | Generated with geopandas                          | See src/create_geo.py                     |
| Calendar    | US Holidays & Weekends | sample_calendar.csv                | Generated with holidays Python library            | See src/create_calendar.py                |

*See the [project report](../reports/Project%20Final%20Report_Advanced%20Analytics%20Practicum_MetroAnalytics%20Team2.pdf) for full data preprocessing details.*

## How to Recreate Full Datasets

Due to file size and privacy restrictions, the full datasets are not available in this repository. To recreate them:

1. **NYC OpenData (NYPD, Events, etc.):**
   - Visit the [NYC OpenData Portal](https://opendata.cityofnewyork.us).
   - Download the relevant datasets for the desired years.
   - Use the provided `scripts/process_raw_data.py` to preprocess and grid the data.

2. **TAHub Metro NY Reports:**
   - This data is non-public. If you are a Metro Analytics partner, request access via your sponsor.

3. **Mobility Data:**
   - Obtain monthly passenger statistics from [Port Authority NY/NJ](https://www.panynj.gov/).

4. **Geography and Calendar:**
   - Download borough boundaries from [NYC GIS](https://www1.nyc.gov/site/doitt/initiatives/gis-download.page).
   - US holidays from [timeanddate.com](https://www.timeanddate.com/holidays/us/).

## Data Ethics, Privacy, and Usage

- **No raw PII or sensitive data is included.**
- All data is for academic/research purposes only.
- For any questions about data access, contact the project maintainer.

---

## Example: Loading a Sample Dataset

```python
import pandas as pd
df = pd.read_csv('data/sample/sample_nypd_complaints_2021.csv')
print(df.head())
```

---

## Questions?
If you need help with data setup, please open an issue or contact [your.email@domain.com].
