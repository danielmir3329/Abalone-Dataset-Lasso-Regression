# Abalone Dataset Lasso Regression (L1)

## Overview

This project uses Lasso Regression (L1 Regularization) to predict abalone age using measurements from the Kaggle Abalone Dataset.

Lasso Regression was selected because it performs both regularization and feature selection, helping identify the most important variables while reducing model complexity.

---

## Dataset

Source: Kaggle Regression with Abalone Dataset Competition

Features:

- Sex
- Length
- Diameter
- Height
- Whole Weight
- Shucked Weight
- Viscera Weight
- Shell Weight

Target:

- Rings

---

## What is Lasso Regression?

Lasso Regression extends linear regression by adding an L1 penalty term to the objective function.

Mathematically:

RSS + λΣ|β|

Unlike Ridge Regression, Lasso can shrink coefficients completely to zero, effectively removing less important features from the model.

---

## Project Objectives

- Build a regularized regression model
- Perform automatic feature selection
- Improve interpretability
- Compare performance with Ridge and Multiple Linear Regression
- Generate Kaggle predictions

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Data Preparation

### Feature Engineering

Additional features were created:

- Volume
- Density
- Shell Ratio
- Length-Diameter Ratio

### Scaling

Lasso Regression requires standardized data:

```python
StandardScaler()
```

---

## Model Development

```python
from sklearn.linear_model import Lasso

lasso_model = Lasso(alpha=0.001)
```

Cross-validation was used to identify the optimal regularization parameter.

---

## Evaluation Metrics

The model was evaluated using:

- RMSLE
- MAE
- MSE
- R² Score

### Final Performance

**RMSLE: 0.1672**

The model achieved performance nearly identical to Ridge Regression while producing a simpler and more interpretable model.

---

## Feature Selection Results

Lasso automatically identified the most important predictors.

Top predictors included:

- Shell Weight
- Shell Ratio
- Whole Weight
- Shucked Weight
- Density

Several less important variables were shrunk toward zero, reducing model complexity.

---

## Advantages of Lasso Regression

- Performs feature selection automatically
- Produces simpler models
- Improves interpretability
- Reduces overfitting
- Identifies the most influential predictors

---

## Model Comparison

| Model | RMSLE |
|---------|---------|
| Multiple Linear Regression | Baseline |
| Ridge Regression (L2) | 0.1666 |
| Lasso Regression (L1) | 0.1672 |

Ridge Regression achieved the lowest prediction error, while Lasso Regression produced the most interpretable model.

---


Southern New Hampshire University

Master of Science in Human Resource Management
