# Data Clustering and Predictive Modeling Project

This project focuses on clustering data into 3 or 4 groups based on covariates and building a predictive model \( \hat{y} \) to better approximate the outcome variable \( y \), which is poorly described. The project utilizes dimensionality reduction, clustering techniques, and machine learning to derive meaningful insights and improve predictions.

---

## Table of Contents
- [Dataset Overview](#dataset-overview)
- [Project Workflow](#project-workflow)
---

## Dataset Overview
- **Outcome Variable (y):** The target variable. Rows with \( y = 0 \) are filtered out.
- **Covariates:**
  - \( X1, X2, X3 \): Measure similar attributes.
  - \( Z1, Z2 \): Measure another related aspect.
  - \( A \): Represents a distinct attribute.
  - \( B \): Represents a different distinct attribute.

---

## Project Workflow
1. **Data Preprocessing:**
   - Rows where \( y = 0 \) are excluded.
   - Covariates are normalized to ensure meaningful clustering.

2. **Dimensionality Reduction:**
   - **PCA (Principal Component Analysis):**
     - \( X1, X2, X3 \) are combined into `X_combined`.
     - \( Z1, Z2 \) are combined into `Z_combined`.

3. **Clustering:**
   - **K-means clustering** groups data into 3 or 4 clusters.
   - Cluster labels are added to the dataset for analysis.

4. **Predictive Modeling:**
   - A **Random Forest Regressor** is trained to predict \( \hat{y} \), using:
     - Features: Cluster labels, `X_combined`, `Z_combined`, \( A \), \( B \).
     - Target: \( y \).

5. **Evaluation:**
   - Performance is evaluated using metrics like R² and Mean Squared Error (MSE).

---
