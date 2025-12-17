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
- Scaled features with
