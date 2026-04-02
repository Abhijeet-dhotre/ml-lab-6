# ML Assignment 6 — Clustering Techniques

**Aim:** To perform clustering using K-Means, Spectral Clustering, and DBSCAN, and compare their performance across three datasets.

## Datasets
| Dataset | Samples | Features | Classes |
|---------|---------|----------|---------|
| Iris | 150 | 4 | 3 (setosa, versicolor, virginica) |
| Wine | 178 | 13 | 3 (class_0, class_1, class_2) |
| Breast Cancer | 569 | 30 | 2 (malignant, benign) |

## Algorithms Implemented
- **K-Means Clustering** — Partitioning method using centroid-based clustering
- **Spectral Clustering** — Graph-based clustering using nearest neighbors
- **DBSCAN** — Density-based spatial clustering with noise detection

## Evaluation Metrics
- **Silhouette Score** — Measures cluster cohesion and separation (-1 to 1, higher is better)
- **Adjusted Rand Index (ARI)** — Measures similarity with ground truth labels (-1 to 1, higher is better)

## Methodology
1. Data preprocessing with StandardScaler for z-score normalization
2. PCA (2 components) for visualization
3. Optimal K selection using Elbow Method and Silhouette Analysis
4. Hyperparameter tuning for DBSCAN (eps parameter)
5. Performance comparison across all algorithms and datasets

## Key Results

### K-Means
| Dataset | Silhouette | ARI |
|---------|------------|-----|
| Iris | 0.4599 | 0.6201 |
| Wine | 0.2849 | 0.8975 |
| Breast Cancer | 0.3144 | 0.5107 |

### Spectral Clustering
| Dataset | Silhouette | ARI |
|---------|------------|-----|
| Iris | 0.4593 | 0.6465 |
| Wine | 0.2828 | 0.8804 |
| Breast Cancer | 0.2862 | 0.5236 |

### DBSCAN
| Dataset | eps | Clusters | Noise | Silhouette | ARI |
|---------|-----|----------|-------|------------|-----|
| Iris | 1.40 | 2 | 0 | 0.5818 | 0.5681 |
| Wine | 2.40 | 2 | 36 | 0.1959 | 0.4205 |
| Breast Cancer | 2.50 | 2 | 224 | -0.0168 | 0.2078 |

## Conclusion

- **K-Means** was the most consistently reliable algorithm, achieving highest ARI on Wine (0.8975)
- **Spectral Clustering** produced similar results to K-Means, with slightly higher ARI on Iris
- **DBSCAN** struggled with high-dimensional data (negative silhouette on Breast Cancer)
- **Overall Winner: K-Means** — best balance of simplicity, speed, and accuracy

## Requirements
- Python 3.x
- numpy, pandas, matplotlib, seaborn
- scikit-learn

## License
This is an academic assignment for ML Lab.