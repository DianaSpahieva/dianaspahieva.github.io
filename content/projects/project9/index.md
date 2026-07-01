---
title: Project 9 - Forest Cover ML Pipeline
date: 2026-02-10 # to change
links:
  - type: site
    url: https://github.com/DianaSpahieva/forest-cover-ml-pipeline
tags:
  - Machine Learning
  - Classification
  - Python
---

# 🌲 Forest Cover Classification Pipeline

**End-to-End Machine Learning | Model Comparison | Cross-Validation | Feature Engineering**

---

## 🧭 Overview

This project implements a complete machine learning pipeline to classify forest cover types using cartographic and environmental variables.

Rather than focusing on a single model, the project emphasizes **model benchmarking, cross-validation, and performance comparison** across multiple supervised learning algorithms.

The objective is to evaluate how different classification approaches perform on a high-dimensional, multi-class dataset and identify the most robust model under consistent validation settings.

---

## 🧠 Machine Learning Pipeline

```text
Data Ingestion
      ↓
Exploratory Data Analysis (EDA)
      ↓
Data Preprocessing
  ├── Feature Scaling (Standardization)
  └── Train/Test Split
      ↓
Model Benchmarking
  ├── Logistic Regression
  ├── Linear Discriminant Analysis (LDA)
  ├── K-Nearest Neighbors (KNN)
  └── Decision Tree (CART)
      ↓
5-Fold Cross-Validation
      ↓
Hyperparameter Tuning
  └── Decision Tree (criterion, splitter)
      ↓
Model Evaluation & Comparison
      ↓
Final Insights
```

---

## 📊 Model Performance Comparison

All models were evaluated using **5-fold cross-validation accuracy**.

| Model | Configuration | Mean Accuracy |
|--------|--------------|--------------:|
| Logistic Regression | Original | **0.3866 ± 0.0098** |
| Logistic Regression | Standardized | **0.5864 ± 0.0150** |
| Linear Discriminant Analysis (LDA) | Original | **0.6424 ± 0.0086** |
| Linear Discriminant Analysis (LDA) | Standardized | **0.6424 ± 0.0086** |
| K-Nearest Neighbors (KNN) | Original | **0.8024 ± 0.0063** |
| K-Nearest Neighbors (KNN) | Standardized | **0.3402 ± 0.0060** |
| Decision Tree (CART) | Original | **0.7810 ± 0.0119** |
| Decision Tree (CART) | Tuned | **0.7817 ± 0.0093** |

---

## ⚙️ Hyperparameter Optimization

A **Decision Tree (CART)** classifier was further optimized through grid-level experimentation on key hyperparameters:

### Parameters Evaluated

- **Criterion:** `gini`, `entropy`
- **Splitter:** `best`, `random`

### Best Configuration

```text
criterion = entropy
splitter = random
```

### Result

**Mean Cross-Validation Accuracy:** **0.7819 (~78.2%)**

Although the improvement was modest, it was consistent across validation folds, demonstrating the sensitivity of tree-based models to impurity measures and splitting strategies.

---

## 🧪 Key Methodological Highlights

- Applied **5-Fold Cross-Validation** for robust performance estimation.
- Benchmarked multiple supervised classification algorithms.
- Compared the impact of **feature scaling** across different models.
- Performed controlled **hyperparameter tuning** on the Decision Tree classifier.
- Ensured fair comparison by evaluating all models using identical validation splits.

---

## 🧱 Technical Skills Demonstrated

- Machine Learning Pipeline Design
- Supervised Multi-class Classification
- Model Benchmarking & Selection
- K-Fold Cross-Validation
- Feature Scaling & Data Preprocessing
- Hyperparameter Optimization
- Comparative Model Evaluation
- Statistical Performance Reporting
- Python (Scikit-learn Ecosystem)

---

## 📌 Key Insights

The experiments highlight that model performance depends heavily on algorithm characteristics and preprocessing choices.

Key findings include:

- **K-Nearest Neighbors (KNN)** achieved the highest accuracy on the original feature space but degraded substantially after standardization.
- **Linear Discriminant Analysis (LDA)** produced stable performance regardless of feature scaling.
- **Logistic Regression** benefited significantly from standardization, improving from **38.7%** to **58.6%** accuracy.
- **Decision Trees** delivered consistently strong performance with only modest gains from hyperparameter tuning.

Overall, the project demonstrates the importance of:

- Selecting algorithms appropriate for the underlying data structure.
- Evaluating the effect of preprocessing rather than assuming it always improves performance.
- Using cross-validation to support reliable, data-driven model selection.

---

## 📦 Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook


### Analysis Walkthrough
{{< notebook
    src="Forest_Cover_Type_Prediction.ipynb"
    show_code=false
    show_outputs=true
>}}