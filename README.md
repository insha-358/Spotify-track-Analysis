# Spotify-track-Analysis
Spotify Streaming Data Analysis: Conducted data analysis on 8,000 Spotify tracks using Python, Spotify API, and Power BI to identify patterns in music popularity. Found that songs with moderate-to-high energy and danceability, especially in R&amp;B and Alternative genres, are most popular. 

## Project Overview

An in-depth exploratory data analysis of Spotify track data combining API integration, statistical analysis, and interactive Power BI dashboards to uncover patterns in music popularity, genre preferences, and audio characteristics.

**Prepared by:** Insha Javaid  
**Date:** October 12, 2025

---

## Executive Summary

This project analyzes **8,213 tracks** with **36 features** to understand what makes music popular on Spotify. Through data enrichment via Spotify APIs, feature engineering, and comprehensive visualizations, the analysis reveals that:

- **Popular tracks balance moderate-to-high energy and danceability**
- **R&B and Alternative genres dominate popularity metrics**
- **Artist popularity and followers strongly predict track success**
- **Acoustic and relaxing tracks appeal to niche audiences**
- **No single feature determines success—it's the combination that matters**

---

## Table of Contents

- [Business Objectives](#business-objectives)
- [Dataset Description](#dataset-description)
- [Key Features](#key-features)
- [Installation](#installation)
- [Analysis Workflow](#analysis-workflow)
- [Key Findings](#key-findings)
- [Visualizations](#visualizations)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Future Enhancements](#future-enhancements)
- [License](#license)

---

## Business Objectives

### Primary Goals

1. **Trend Identification**: Discover patterns across genres, artists, and labels to inform playlist curation and marketing strategies
2. **Feature Analysis**: Determine which audio characteristics correlate most with hit songs
3. **Data Engineering**: Create derived metrics to capture nuanced listener preferences
4. **Actionable Insights**: Provide data-driven recommendations for content creation, curation, and promotion

### Target Audience

- Music streaming platforms and curators
- Artists and record labels
- Marketing and A&R professionals
- Data analysts and music researchers

---

## Dataset Description

### Source
- **Base Dataset**: Spotify tracks from Kaggle
- **Enrichment**: Spotify Web API for additional metadata
- **Final Dataset**: `spotifyfinalclean.csv`

### Statistics
- **Total Tracks**: 8,213
- **Features**: 36 (17 original + 19 engineered)
- **Genres**: Alternative, R&B, Country, Movie, A Capella
- **Data Quality**: No missing values in critical fields, minimal outliers retained for analysis

### Feature Categories

**Audio Features (Original)**
- Energy, Danceability, Acousticness, Instrumentalness
- Loudness, Tempo, Valence, Liveness
- Duration, Key, Mode, Time Signature

**Metadata (API-Enriched)**
- Artist followers and popularity
- Album type and label
- Track and artist names

**Engineered Features**
- Mood Zone (e.g., "Happy Energetic", "Sad Calm")
- Popularity Potential (composite score)
- Production Intensity (complexity measure)
- Relaxation Score (calmness indicator)
- Energy-to-Acoustic Ratio
- Tempo Category (Slow/Medium/Fast)
- Duration Category (Short/Standard/Long/Very Long)

---

## Key Features

### Data Processing
- **API Integration**: Automated data enrichment using Spotify Web API
- **Feature Engineering**: 19 custom metrics capturing listener preferences
- **Data Cleaning**: Handled missing values, duplicates, and outliers
- **Categorical Encoding**: Structured categorical variables for analysis

### Analysis Capabilities
- **Comprehensive EDA**: Statistical summaries, distributions, and correlations
- **Rich Visualizations**: Bar charts, scatter plots, heatmaps, and genre comparisons
- **Power BI Dashboard**: Interactive exploration of trends and patterns
- **Multi-Dimensional Analysis**: Genre, mood, tempo, and popularity intersections

---

## Installation

### Prerequisites
```bash
Python 3.8+
Spotify Developer Account (for API access)
Power BI Desktop (for dashboard)
```

### Python Libraries
```bash
pip install pandas numpy matplotlib seaborn
pip install spotipy requests
pip install scikit-learn
```

### Spotify API Setup
1. Create an app at [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Obtain Client ID and Client Secret
3. Configure authentication in your script:



## Analysis Workflow

### 1. Data Collection
- Collected Data using Spotify API

### 2. Data Cleaning
- Remove duplicates and handle missing values
- Validate data types and ranges
- Standardize categorical variables

### 3. Feature Engineering
- Popularity Bucket
- Relaxation Score
- Populalarity potential
- popularity intensity
- Mood zone etc


### 4. Exploratory Analysis
- Summary statistics
- Distribution analysis
- Genre-specific patterns
- Correlation studies

### 5. Visualization
- Generate static plots (Matplotlib/Seaborn)
- Build interactive Power BI dashboard

---

## Key Findings

### Genre Insights

| Genre | Avg Popularity | Characteristics | Best For |
|-------|---------------|-----------------|----------|
| **R&B** | 63.6-64.4 | High danceability, energetic, polished production | Dance playlists, mainstream appeal |
| **Alternative** | ~55.5 | Highest energy, versatile mood, complex production | Energetic playlists, active listening |
| **Country** | 40-41 | Balanced energy, moderate tempo, storytelling | Background music, emotional connection |
| **Movie** | ~1 | High instrumentalness, moderate energy, cinematic | Focus/study, film scores |
| **A Capella** | <10 | Most acoustic, lowest energy, relaxing | Relaxation, vocal appreciation |

### Audio Feature Patterns

**What Makes Songs Popular?**
- Moderate-to-high **danceability** (0.5-0.7)
- Moderate-to-high **energy** (0.6-0.8)
- Lower **acousticness** (<0.3)
- Standard **duration** (3-4 minutes)
- Higher **artist followers** and popularity

**What Doesn't Impact Popularity?**
- Mode (Major vs. Minor key)
- Time signature
- Exact tempo value
- Track duration category

### Correlation Highlights

```
Strong Positive Correlations:
- Popularity ↔ Danceability (0.34)
- Popularity ↔ Energy (0.34)
- Popularity ↔ Artist Popularity (0.47)

Strong Negative Correlations:
- Popularity ↔ Acousticness (-0.39)
- Popularity ↔ Relaxation Score (-0.38)
```

### Mood Zone Distribution

Top mood zones by track count:
1. **Happy Energetic** (Alternative, R&B dominant)
2. **Sad Energetic** (Pop/Rock influence)
3. **Happy Calm** (Country, acoustic tracks)
4. **Sad Calm** (Movie scores, introspective)

---

## Visualizations

### Included Charts

1. **Genre Distribution** - Bar chart of track counts per genre
2. **Key Distribution** - Frequency of musical keys
3. **Time Signature** - Distribution of rhythmic patterns
4. **Mood Zone Analysis** - Popularity across emotional categories
5. **Feature-by-Genre Comparisons** - Multi-panel bar charts for:
   - Acousticness
   - Danceability
   - Energy
   - Instrumentalness
   - Liveness
   - Loudness
   - Valence
   - Relaxation Score
   - Production Intensity
6. **Feature-by-Popularity Scatterplots** - Relationships between:
   - Danceability × Popularity
   - Energy × Popularity
   - Energy-to-Acoustic Ratio × Popularity
   - Popularity Potential × Actual Popularity
7. **Duration Category Analysis** - Popularity across song lengths
8. **Energy-Danceability-Popularity** - 3D relationship scatter
9. **Correlation Heatmap** - Audio and engineered features

### Power BI Dashboard

Interactive dashboard includes:
- Genre performance metrics
- Artist leaderboards
- Temporal trend analysis
- Audio feature filters
- Mood zone explorer

---

## Technologies Used

### Data Processing
- **Python 3.8+** - Core programming language
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations

### Data Collection
- **Spotipy** - Spotify Web API wrapper
- **Requests** - HTTP library for API calls

### Visualization
- **Matplotlib** - Static plot generation
- **Seaborn** - Statistical visualizations
- **Power BI** - Interactive dashboards

### Analysis
- **Scikit-learn** - Feature engineering and scaling
- **SciPy** - Statistical tests

---

## Project Structure

```
spotify-streaming-analysis/
├── data/
│   ├── raw/
│   │   └── spotify_tracks_raw.csv
│   └── processed/
│       └── spotifyfinalclean.csv
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_exploratory_analysis.ipynb
│   └── 05_visualization.ipynb
├── scripts/
│   ├── spotify_api.py
│   ├── feature_engineering.py
│   └── visualization_utils.py
├── dashboards/
│   └── spotify_analysis.pbix
├── outputs/
│   ├── figures/
│   └── reports/
├── requirements.txt
├── config.py
└── README.md
```

---

## Usage

### Basic Analysis


### Generate Visualizations


## Key Insights for Stakeholders

### For Artists & Producers

- **Target the sweet spot**: Aim for moderate-high energy (0.6-0.8) and danceability (0.5-0.7)
- **Production quality matters**: R&B and Alternative's polished production correlates with popularity
- **Don't ignore relaxation**: While less mainstream, acoustic/calm tracks fill important niche markets
- **Genre strategy**: Consider R&B or Alternative influences for mainstream appeal

### For Playlist Curators

- **Mood-based curation**: Use engineered mood zones for targeted playlists
- **Energy pacing**: Balance high-energy tracks with moderate ones for engagement
- **Genre mixing**: Country and Alternative work well together (similar energy profiles)
- **Context matters**: Movie scores and A Capella excel in focus/relaxation contexts

### For Marketing Teams

- **Artist popularity is key**: Promote tracks from artists with existing followings
- **Genre positioning**: R&B has broadest appeal across major/minor modes
- **Feature bundling**: Market tracks highlighting energy + danceability together
- **Duration optimization**: Standard length (3-4 min) remains safest for radio/playlists

---

## Future Enhancements

### Planned Features

1. **Time-Series Analysis**
   - Track popularity trends over release periods
   - Seasonal listening pattern identification

2. **Machine Learning Models**
   - Predict track popularity using Random Forest/XGBoost
   - Clustering analysis for genre sub-categorization

3. **Lyrical Analysis**
   - Integrate Genius API for lyric sentiment analysis
   - Identify themes in popular vs. unpopular tracks

4. **Real-Time Dashboard**
   - Live API integration for trending tracks
   - Automated weekly insights generation

5. **Expanded Dataset**
   - Include more genres and international markets
   - Add user demographic data for personalized insights

---

## Limitations

- **Dataset Scope**: Limited to 5 primary genres (not representative of all Spotify content)
- **Temporal Coverage**: Snapshot analysis (no longitudinal trends)
- **Causation**: Correlations identified, but causation not established
- **API Constraints**: Rate limits may affect large-scale data collection
- **Cultural Bias**: Results may reflect Western/English-speaking market preferences

---

## License

This project is created for educational and research purposes. 

**Dataset**: Spotify track data subject to Spotify's Terms of Service  
**Code**: Available for academic and non-commercial use

---

## Acknowledgments

- **Spotify**: For providing comprehensive Web API and data access
- **Kaggle Community**: For base dataset and inspiration
- **Data Visualization Community**: For visualization best practices

---

## Contact

**Insha Javaid**  
Data Analyst | Music Industry Researcher

Email: [inshajavaid881@gmail.com]  
LinkedIn: [https://www.linkedin.com/in/insha-javaid-71a01423a/]  


---

## Citation

If you use this analysis in your research or work, please cite:


Javaid, I. (2025). Spotify Streaming Data Analysis: Exploring Music Popularity 
Through Audio Features and Genre Patterns. 




## Appendix

### Glossary of Terms

- **Acousticness**: Measure of acoustic (non-electronic) sound (0-1 scale)
- **Danceability**: How suitable a track is for dancing (0-1 scale)
- **Energy**: Intensity and activity level (0-1 scale)
- **Instrumentalness**: Likelihood of containing no vocals (0-1 scale)
- **Liveness**: Presence of audience in recording (0-1 scale)
- **Loudness**: Overall volume in decibels (typically -60 to 0 dB)
- **Speechiness**: Presence of spoken words (0-1 scale)
- **Tempo**: Speed in beats per minute (BPM)
- **Valence**: Musical positiveness/cheerfulness (0-1 scale)

### Additional Resources

- [Spotify Web API Documentation](https://developer.spotify.com/documentation/web-api/)
- [Spotipy Library Documentation](https://spotipy.readthedocs.io/)
- [Power BI Documentation](https://docs.microsoft.com/en-us/power-bi/)

---

**Last Updated:** October 21, 2025
