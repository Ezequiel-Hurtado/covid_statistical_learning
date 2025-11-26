# apprentissage_stat
Repositoire pour le projet d'Apprentissage Statistique

## 🧩 Project Overview
In March 2020, the World Health Organization declared COVID-19 a global pandemic.
Countries in the WHO South-East Asia Region were facing:
First imported cases
Early clusters
Or were attempting to prevent importation through strict control
The months that followed were unprecedented — governments, scientists, health systems, communities and individuals reacted with urgency using measures never seen before.
This project aims to analyze COVID-19 data from South-East Asian countries to identify:
Which countries are performing well in controlling the pandemic
Which require immediate attention
We use machine learning & statistical techniques (preprocessing, PCA, HDBSCAN, KMeans, outlier detection) to provide actionable insights.

## 📂 Repository Structure

```
📦 project/
│
├── 📁 data/
│   └── CovidCases.csv          # Raw dataset from Worldometers
│
├── 📁 scripts/
│   ├── Scripts.ipynb            # Handling missing values, KNN imputation, standardization
│   └── utils.py                 # Helper functions
│
├── Covid19Description.pdf             # List of dependencies
└── README.md                    # Main project description
```

## 🧪 Methods Used
1. Data Cleaning & Preprocessing
Handling missing values
Standardization (RobustScaler / StandardScaler)
Removing duplicated & highly correlated features
Treating populations vs. per-million metrics
2. KPI Engineering
Creation of new meaningful variables:
Case Fatality Rate (CFR)
Test Positivity Rate
Active Case Density
Testing Intensity
3. Outlier Detection using HDBSCAN
Identifies anomalous countries (HDBSCAN label = -1)
These countries are excluded from segmentation analysis
4. Clustering (KMeans)
After removing HDBSCAN outliers, KMeans is applied to the homogeneous cluster to find subtle differences between countries.
5. PCA Visualization
PCA 2D & 3D mapping
Visualizing clusters
Understanding variable influence

## 🎯 Goal of the Project
To answer the question:
“Which countries are doing relatively well and which ones need immediate attention?”
Using:
Data-driven clustering
Scalable ML techniques
Epidemiologically meaningful indicators
The insights produced can help governments, NGOs, and health authorities prioritize interventions.


