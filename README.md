# Machine Learning: Comparative Analysis of Supervised and Unsupervised Learning

[![Python](https://img.shields.io/badge/python-3.9%2B-blue)]()
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-0.23%2B-orange)]()
[![License](https://img.shields.io/badge/license-MIT-green)]()
[![Status](https://img.shields.io/badge/status-complete-success)]()

## Overview

A comprehensive comparative study of supervised and unsupervised learning techniques implemented from scratch and validated against scikit-learn. Evaluates Principal Component Analysis (PCA), K-Means Clustering, and Decision Trees on binary and multi-class classification problems using real-world medical and digit recognition datasets.

**Module:** CM3015 Machine Learning and Neural Networks  
**Datasets:** Breast Cancer Wisconsin (569 samples, 30 features) | Handwritten Digits (1,797 samples, 64 features)  
**Algorithms:** PCA (custom + scikit-learn), K-Means (custom + scikit-learn), Decision Tree (scikit-learn)

## Key Results

| Algorithm | Dataset | Metric | Performance | Notes |
|-----------|---------|--------|-------------|-------|
| **PCA** | Breast Cancer | Variance Retained | 95%+ | 10 components |
| **K-Means** | Breast Cancer | Silhouette Score | 0.58–0.62 | Unsupervised clustering |
| **Decision Tree** | Digits | Accuracy | 95%+ | Multi-class classification |

## What's Inside

**Jupyter Notebook** (`notebooks/CM3015_ML_Analysis.ipynb`):
- 108 cells: 72 markdown sections + 36 code implementations
- **Setup:** Data loading, preprocessing, feature scaling (StandardScaler)
- **Algorithm Implementation:** PCA and K-Means from scratch with mathematical derivations
- **Validation:** Custom implementations verified against scikit-learn equivalents
- **Experiments:** Sanity checks, convergence analysis, hyperparameter tuning, performance comparison
- **Analysis:** Accuracy metrics, confusion matrices, silhouette analysis, visualization
- **Insights:** Algorithm trade-offs, computational complexity, deployment considerations

## Quick Start

```bash
pip install -r requirements.txt
jupyter notebook notebooks/CM3015_ML_Analysis.ipynb
```

## Tech Stack

- **Data Processing:** NumPy, Pandas, Scikit-learn
- **Machine Learning:** PCA, K-Means, Decision Trees
- **Visualization:** Matplotlib, Seaborn
- **Environment:** Python 3.9+, Jupyter

## Methodology Highlights

- **Reproducibility:** Fixed random seed (RANDOM_STATE=42) across all experiments
- **Validation:** Custom algorithms validated pixel-by-pixel against scikit-learn implementations
- **Rigorous Testing:** Sanity checks, convergence verification, edge case handling
- **Fair Comparison:** Identical preprocessing, identical evaluation metrics, consistent random states
- **Comprehensive Analysis:** Per-dataset performance, per-class breakdowns, failure mode analysis

## Algorithms Explained

**Principal Component Analysis (PCA):** Unsupervised dimensionality reduction via eigenvalue decomposition. Captures maximum variance in principal components. Custom implementation demonstrates covariance matrix computation, SVD, and variance explained calculation.

**K-Means Clustering:** Unsupervised partitional clustering via iterative centroid optimization. Custom implementation includes multiple initialization strategies (random, k-means++), convergence checking, and silhouette score evaluation.

**Decision Trees:** Supervised classification via recursive feature-based splitting. Scikit-learn implementation with hyperparameter tuning (max_depth, min_samples_split) and feature importance visualization.

## Key Insights

1. **Custom vs Library:** Custom implementations achieve 99%+ numerical agreement with scikit-learn, validating algorithmic correctness
2. **Dimensionality Reduction:** PCA reduces 30→10 features on Breast Cancer while retaining 95%+ variance; speeds up downstream models
3. **Clustering Quality:** K-Means separates Breast Cancer classes (silhouette ~0.6) but struggles on multi-class Digits (class overlap)
4. **Supervised Dominance:** Decision Trees achieve 95%+ accuracy on Digits; unsupervised methods lag significantly when labels available
5. **Computational Trade-offs:** Custom implementations slower than optimized scikit-learn; educational value justifies deployment cost trade-off

## Experimental Sections

- PCA covariance matrix computation and eigenvalue analysis
- K-Means convergence behavior and initialization impact on final clusters
- Decision Tree pruning and hyperparameter sensitivity
- Cross-algorithm performance comparison (accuracy, runtime, interpretability)
- Visualization of learned representations (PCA projections, cluster assignments, decision boundaries)

## Author

**Dhanarasu Naveen**  
Computer Science | University of London (via SIM Singapore)  
Specialization: Artificial Intelligence & Machine Learning

## License

MIT License
