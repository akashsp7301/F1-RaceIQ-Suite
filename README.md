# F1-RaceIQ-Suite

Machine learning pipeline predicting whether a Formula 1 driver finishes in the points (Top 10), built on 75 years of race data (1950–2024).

## Overview

- **Data source:** [Jolpica API](https://api.jolpi.ca/ergast/f1/), the community successor to Ergast - race  7000 results across 19 features
- **Task:** Binary classification - Points finish (Top 10) vs No Points
- **Best model:** Decision Tree (Entropy, Max Depth 6) - 88.76% accuracy
- **21 model configurations** across five algorithm families, plus PCA for unsupervised validation

## Methods

**Supervised Learning**
- Decision Tree (3 configurations)
- Random Forest & XGBoost
- Naive Bayes (5 variants)
- Logistic Regression (2 configurations)
- SVM (9 configurations, 3 kernels)

**Unsupervised Learning**
- Principal Component Analysis (PCA)

All models evaluated on the same 80/20 train/test split (random_state=42) using Accuracy, Precision, Recall and F1-Score.

## Key Findings

- Grid Position, Laps Completed and Status are the strongest predictors across every model
- Tree-based models substantially outperform linear and probability-based models
- PCA independently confirms the supervised feature importance rankings

## Repository Structure
 Supervised Learning/ # Decision Tree, Ensemble, Naive Bayes, Regression, SVM notebooks
Unsupervised Learning/ # PCA notebook
data/ # Raw and cleaned datasets
 README.md


## Deliverables

A full write-up - methodology, results, discussion and an interactive Power BI dashboard - is available in the accompanying MSc dissertation report.

**Author:** Akash Sakharayapattana Prakash - MSc Data Analytics, Dublin Business School
