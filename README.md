# Credit Card Fraud Detection

## Overview
This project implements a **binary classification** model to detect fraudulent credit card transactions. Using a highly imbalanced dataset from a Kaggle, I evaluate multiple gradient boosting models to identify fraudulent activities with high precision and recall.

### Features
| Feature Group | Description |
|---------------|-------------|
| V1 - V28 | Anonymized PCA-transformed features |
| Time | Seconds elapsed from first transaction |
| Amount | Transaction amount |
| Class | Target variable |

### Class Distribution
| Class | Count | Percentage |
|-------|-------|------------|
| 0 (Legitimate) | 218,754 | 99.79% |
| 1 (Fraudulent) | 375 | 0.21% |

> **Key Challenge**: Extreme class imbalance (0.21% fraud cases) requires specialized handling.

## Models Evaluated
Three gradient boosting models were selected for their effectiveness with imbalanced tabular data:

| Model | Key Advantages |
|-------|----------------|
| **LightGBM** | Fast training, leaf-wise growth, efficient with large datasets |
| **XGBoost** | Excellent performance, built-in handling of imbalanced data |
| **CatBoost** | Robust to overfitting, handles categorical features well |

> **Note**: Baseline results were achieved without hyperparameter tuning, indicating room for significant improvement.

### Feature Importance
Feature importance analysis was performed using CatBoost to identify the most influential predictors.
