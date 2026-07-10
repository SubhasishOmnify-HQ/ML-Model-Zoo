# Unsupervised Machine Learning

## Overview
Unsupervised Learning finds hidden patterns in **unlabeled data**. It is mainly used for clustering and dimensionality reduction.

---

## Models

| Model | Purpose |
|--------|---------|
| K-Means | Clustering |
| Hierarchical Clustering | Hierarchical clusters |
| DBSCAN | Density-based clustering |
| Gaussian Mixture (GMM) | Probabilistic clustering |
| PCA | Dimensionality reduction |
| t-SNE | Data visualization |
| ICA | Feature extraction |

---

## Imports

```python
from sklearn.cluster import KMeans, AgglomerativeClustering, DBSCAN
from sklearn.mixture import GaussianMixture
from sklearn.decomposition import PCA, FastICA
from sklearn.manifold import TSNE
```

---

## Evaluation

```python
from sklearn.metrics import (
    silhouette_score,
    davies_bouldin_score,
    calinski_harabasz_score
)

kmeans.inertia_
```

---

## Workflow

1. Load data
2. Handle missing values
3. Scale features
4. Train model
5. Predict clusters / Transform data
6. Evaluate
7. Visualize
8. Interpret results

---

## Applications

- Customer Segmentation
- Fraud Detection
- Recommendation Systems
- Image Segmentation
- Document Clustering
- Feature Extraction
- Data Visualization

---

## Types

### Clustering
- K-Means
- Hierarchical
- DBSCAN
- GMM

### Dimensionality Reduction
- PCA
- t-SNE
- ICA