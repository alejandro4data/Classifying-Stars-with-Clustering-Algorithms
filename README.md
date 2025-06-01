# ✨ Classifying Stars with Clustering Algorithms

> Unsupervised machine learning reveals the hidden structure of our galaxy, just as it does with business data.

---

## 1. Overview

This project applies clustering algorithms to a catalog of stars, aiming to uncover natural groupings and classifications based solely on their intrinsic properties.  
The same unsupervised learning methods that help astronomers understand the cosmos are also at the heart of data science applications in business: segmentation, anomaly detection, and feature discovery.

---

## 2. Data

- **Source:** `stars_data.csv` (simulated or public star catalog)
- **Features:** Luminosity, Absolute Magnitude, Color Index, Temperature, Spectral Class, and others
- **Preprocessing:** normalization, encoding of categorical variables, outlier removal

---

## 3. Methodology

- **Dimensionality Reduction:**  
  - Principal Component Analysis (PCA) to reduce feature space and enhance visualization
- **Clustering Algorithms:**  
  - K-Means: interpretable clusters, solid baseline  
  - DBSCAN: detects outlier and rare types  
  - Agglomerative (Hierarchical): captures nested structure  
- **Model Selection:**  
  - Metrics such as Silhouette Score and Davies-Bouldin Index  
  - Optimal number of clusters determined by data, not by hand
- **Visualization:**  
  - 2D and 3D scatterplots with clusters color-coded  
  - Interactive graphics for deeper exploration

---

## 4. Key Results

| Algorithm      | # Clusters | Silhouette | Highlights                |
|----------------|------------|------------|---------------------------|
| K-Means        | 4          | 0.61       | Most stable clustering    |
| DBSCAN         | 7 (inc. noise) | 0.47   | Detects outlier stars     |
| Agglomerative  | 5          | 0.56       | Finds nested groupings    |

- Stars naturally group by temperature, luminosity, and color index—mirroring how customers, transactions, or products segment in business data.
- Outlier clusters often correspond to rare spectral types or possible data anomalies.

---

## 5. Getting Started

```bash
git clone https://github.com/<your-user>/classifying-stars-clustering.git
cd classifying-stars-clustering

python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

# Open notebook
jupyter notebook notebooks/clustering_analysis.ipynb

# Or run pipeline
python src/cluster_pipeline.py --data data/stars_data.csv --model kmeans --plot
