# Creating Cohorts of Songs — Joana Coyle

## Overview
Song clustering analysis using **EDA, PCA, and K-Means** to create data-driven cohorts of songs and interpret the audio features that drive musical similarity.

---

## Dataset
- **1,610 songs** (`rolling_stones_spotify.csv`)
- Spotify audio features: danceability, energy, acousticness, instrumentalness, liveness, speechiness, tempo, duration, popularity, release year

---

## Workflow
### Data Inspection & Cleaning
- Verified no missing values or duplicates  
- Removed identifier columns (`id`, `uri`, `Unnamed: 0`)  
- Converted release dates to year  
- Retained outliers as valid musical variation  

### EDA & Feature Engineering
- Defined popular songs (popularity > 50)  
- Identified top albums by popular tracks  
- Checked correlations and multicollinearity (VIF)  
- Dropped redundant features (`valence`, `loudness`)  

### Dimensionality Reduction
- Scaled features with `StandardScaler`  
- Applied PCA to support effective clustering  

### Clustering
- K-Means clustering  
- Optimal k selected using Elbow + Silhouette methods  
- **Final model: k = 3 clusters**

---

## Results (Cluster Profiles)
- **Cluster 1 — Most Popular**  
  Higher danceability & acousticness, lower energy; average year ~1977  

- **Cluster 2 — Live / Extended Tracks**  
  Highest liveness & duration; average year ~2015  

- **Cluster 0 — High Energy / Experimental**  
  Highest energy, instrumentalness & speechiness; average year ~2001  

---

## Tools
Python · pandas · numpy · matplotlib · seaborn · scikit-learn · statsmodels

---

## Note
Some pandas Future Warnings appear due to upcoming default changes. These do not affect the analysis or results.

---

## Key Takeaway
Musical similarity is driven by **combinations of audio features**, not popularity alone.

---
## About
**EDA, PCA, and K-Means clustering to create song cohorts using Spotify audio features and interpret what drives musical similarity.**
