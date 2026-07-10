# Unsupervised Machine Learning Models

## Overview

Unsupervised Learning is a type of machine learning where the model learns patterns from **unlabeled data**. It is commonly used for clustering, dimensionality reduction, anomaly detection, and association rule learning.

---

# Common Unsupervised Learning Models

| Model | Purpose | Scikit-learn Class |
|---|---|---|
| K-Means Clustering | Groups similar data points into K clusters | `KMeans()` |
| Hierarchical Clustering | Creates a hierarchy of clusters | `AgglomerativeClustering()` |
| DBSCAN | Density-based clustering algorithm | `DBSCAN()` |
| Mean Shift | Cluster detection based on density peaks | `MeanShift()` |
| Gaussian Mixture Model (GMM) | Probabilistic clustering | `GaussianMixture()` |
| Spectral Clustering | Graph-based clustering | `SpectralClustering()` |
| Birch | Efficient clustering for large datasets | `Birch()` |
| Principal Component Analysis (PCA) | Dimensionality reduction | `PCA()` |
| t-SNE | Visualization of high-dimensional data | `TSNE()` |
| Independent Component Analysis (ICA) | Feature extraction | `FastICA()` |

---

# Import Statements

```python
from sklearn.cluster import (
    KMeans,
    AgglomerativeClustering,
    DBSCAN,
    MeanShift,
    SpectralClustering,
    Birch
)

from sklearn.mixture import GaussianMixture

from sklearn.decomposition import (
    PCA,
    FastICA
)

from sklearn.manifold import TSNE
```

---

# Evaluation Metrics

### Silhouette Score

```python
from sklearn.metrics import silhouette_score
```

### Davies-Bouldin Index

```python
from sklearn.metrics import davies_bouldin_score
```

### Calinski-Harabasz Score

```python
from sklearn.metrics import calinski_harabasz_score
```

### Inertia (K-Means)

```python
kmeans.inertia_
```

---

# Beginner-Friendly Algorithms

- K-Means Clustering
- Hierarchical Clustering
- DBSCAN
- Gaussian Mixture Model (GMM)
- Principal Component Analysis (PCA)

---

# Typical Workflow

1. Load dataset
2. Handle missing values
3. Scale the features
4. Train an unsupervised learning model
5. Predict cluster labels or transform features
6. Evaluate using Silhouette Score or other clustering metrics
7. Visualize clusters using PCA or t-SNE
8. Interpret the results

---

# Applications

- Customer Segmentation
- Market Basket Analysis
- Document Clustering
- Image Segmentation
- Topic Modeling
- Recommendation Systems
- Fraud Detection
- Anomaly Detection
- Feature Extraction
- Data Visualization

---

# Types of Unsupervised Learning

## 1. Clustering

- K-Means
- Hierarchical Clustering
- DBSCAN
- Mean Shift
- Gaussian Mixture Model
- Spectral Clustering
- Birch

## 2. Dimensionality Reduction

- PCA
- t-SNE
- ICA

---

# Author

This repository provides beginner-friendly notes and code references for popular Unsupervised Machine Learning algorithms.
