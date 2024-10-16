# Clustering Analysis (SC4020 Data Analytics and Mining Project)

## Overview

This project is part of the SC4020 Data Analytics and Mining module, where we explore three popular clustering algorithms: **K-Means++**, **DBSCAN** (Density-Based Spatial Clustering of Applications with Noise), and **Agglomerative Hierarchical Clustering** (AHC). The goal is to perform clustering analysis on synthetic datasets and compare the results based on performance, robustness, and scalability. This project includes both a report and a Jupyter notebook with code.

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Key Algorithms](#key-algorithms)
- [Datasets](#datasets)
- [Evaluation Metrics](#evaluation-metrics)
- [Results Summary](#results-summary)
- [Contributors](#contributors)

## Project Structure

- `SC4020_*.ipynb`: The Jupyter notebook that contains the code used for clustering analysis.
- `SC4020 Report.pdf`: The full report providing in-depth analysis, results, and conclusions from the project.
- `README.md`: This documentation file explaining the contents of the project.

## Key Algorithms

1. **K-Means++**:
   - An improvement over standard K-Means that speeds up convergence.
   - It is suited for spherical and well-separated clusters.
   - Tunable parameter: `n_clusters` (number of clusters).

2. **DBSCAN**:
   - A density-based algorithm that identifies clusters based on data point proximity.
   - No need to specify the number of clusters in advance.
   - Tunable parameters: `eps` (epsilon distance) and `min_samples` (minimum points to form a dense region).

3. **Agglomerative Hierarchical Clustering (AHC)**:
   - A hierarchical clustering method that builds a tree of clusters by iteratively merging or splitting them.
   - Tunable parameters: `n_clusters` (number of clusters) and linkage type (ward, complete, average).

## Datasets

We generated three synthetic datasets using Scikit-learn:
- **Blobs**: Spherical clusters of points.
- **Moons**: Two crescent-shaped clusters.
- **Circles**: Concentric circles of points.

These datasets were chosen to test the clustering algorithms' performance on different geometric configurations, ranging from well-separated clusters to complex shapes.

## Evaluation Metrics

We used the following metrics to evaluate the clustering results:
- **Silhouette Score**: Measures how similar each point is to its cluster versus other clusters (range: -1 to 1).
- **Davies-Bouldin Score**: A lower value indicates better clustering in terms of separation and compactness.
- **Runtime**: The time taken by each algorithm to complete clustering.

## Results Summary

Here is a summary of the key findings from the project:

- K-Means+ performed well on the Blobs dataset, achieving high Silhouette and low Davies-Bouldin scores. However, it struggled with non-spherical shapes like Moons and Circles.
- DBSCAN was highly effective at identifying clusters in the Moons and Circles datasets, but its performance required careful tuning of the eps and min_samples parameters.
- Agglomerative Hierarchical Clustering showed competitive performance with K-Means++ on the Blobs dataset but required significant computational time as the dataset size increased.

In terms of robustness to noise, DBSCAN outperformed both K-Means++ and AHC, handling noisy datasets better.
For more detailed results and analysis, please refer to the report.

## Contributors

- Wang Shang An Davis (https://www.linkedin.com/in/wang-shang-an-davis/)
- Tomoki Teng Zhi Hui (https://www.linkedin.com/in/tomokiteng/)
- Li Zihan (https://www.linkedin.com/in/zihan-li-a9a601218/)
- Chen Zihang (https://www.linkedin.com/in/chen-zihang-caleb/)


