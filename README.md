# Creating Cohorts of Songs — Joana Coyle

## Objective
Use exploratory data analysis (EDA) and clustering to create **cohorts of songs** using Spotify audio features, and interpret what makes songs group together.

## Dataset
- `rolling_stones_spotify.csv` (1,610 songs)
- Audio features include: acousticness, danceability, energy, instrumentalness, liveness, speechiness, tempo, duration, popularity, and release year.

## What I did
### 1) Data inspection & cleaning
- Checked duplicates + missing values (none found)
- Dropped irrelevant/identifier columns (`Unnamed: 0`, `id`, `uri`)
- Converted `release_date` to datetime and extracted `year`
- Reviewed outliers with boxplots and kept them (real musical variation)

### 2) EDA & feature engineering
- Defined “popular songs” as popularity > 50
- Found top albums with most popular songs:
  - Sticky Fingers (Remastered)
  - Exile On Main Street (2010 Re-Mastered)
- Checked multicollinearity (VIF) + correlation
- Dropped redundant features: `valence` and `loudness`

### 3) Dimensionality reduction
- Scaled features with StandardScaler
- Applied PCA and selected components for clustering

### 4) Clustering
- Used KMeans
- Selected k using Elbow + Silhouette score
- Best result: **k = 3 clusters**

## Results (Cluster Profiles)
- **Cluster 1:** Most popular; higher danceability + acousticness; lower energy/liveness/speechiness; avg year ~1977  
- **Cluster 2:** Highest liveness + duration; lowest instrumentalness; avg year ~2015  
- **Cluster 0:** Highest energy + instrumentalness + speechiness; lowest danceability; avg year ~2001  

## How to run
1. Open the notebook in Google Colab
2. Run all cells
3. Upload the dataset when prompted (`rolling_stones_spotify.csv`)

## Tools
Python, Pandas, NumPy, Matplotlib, Seaborn, scikit-learn, statsmodels
