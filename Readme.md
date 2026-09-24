# GMM: Breast Cancer Clustering

Gaussian Mixture Model clustering on the Breast Cancer Wisconsin Diagnostic dataset, with soft cluster assignments, probability-based anomaly detection, and a comparison against K-Means.

## Files

- `CG_C08_M06.ipynb`: analysis notebook (the dataset loads directly from scikit-learn, so no CSV is needed)

## Approach

1. Standardize the 30 features with `StandardScaler`
2. Select the number of components using BIC and AIC
3. Fit a GMM with 2 components and score it with the silhouette coefficient
4. Flag anomalies as points in the bottom 5% of cluster probability
5. Compare GMM and K-Means assignments, and visualize both in 2D with PCA

## Results

- Silhouette score: 0.3145
- Anomalies detected: 29 of 569 samples
- GMM and K-Means agree on all but 30 samples
