# Regression Models in Machine Learning

## Overview

Regression algorithms are used to predict **continuous numerical values** such as house prices, salaries, temperatures, or sales.

---

## Common Regression Models

| Model | Purpose | Scikit-learn Class |
|---|---|---|
| Linear Regression | Predicts continuous values using a linear relationship | `LinearRegression()` |
| Polynomial Regression | Models non-linear relationships | `PolynomialFeatures` + `LinearRegression()` |
| Ridge Regression | Linear regression with L2 regularization | `Ridge()` |
| Lasso Regression | Linear regression with L1 regularization; performs feature selection | `Lasso()` |
| Elastic Net Regression | Combines L1 and L2 regularization | `ElasticNet()` |
| Support Vector Regression | Handles linear and non-linear regression | `SVR()` |
| Decision Tree Regression | Tree-based regression model | `DecisionTreeRegressor()` |
| Random Forest Regression | Ensemble of decision trees | `RandomForestRegressor()` |
| Gradient Boosting Regression | Boosting-based regression | `GradientBoostingRegressor()` |
| XGBoost Regression | Optimized boosting algorithm (XGBoost library) | `XGBRegressor()` |

---

## Import Statements

```python
from sklearn.linear_model import (
    LinearRegression,
    Ridge,
    Lasso,
    ElasticNet
)

from sklearn.svm import SVR
from sklearn.tree import DecisionTreeRegressor
from sklearn.ensemble import (
    RandomForestRegressor,
    GradientBoostingRegressor
)

from xgboost import XGBRegressor
```

---

## Regression Evaluation Metrics

### R² Score

```python
from sklearn.metrics import r2_score
```

### Mean Absolute Error (MAE)

```python
from sklearn.metrics import mean_absolute_error
```

### Mean Squared Error (MSE)

```python
from sklearn.metrics import mean_squared_error
```

### Root Mean Squared Error (RMSE)

```python
import numpy as np
from sklearn.metrics import mean_squared_error

rmse = np.sqrt(mean_squared_error(y_test, y_pred))
```

---

## Beginner-Friendly Regression Models

- Linear Regression
- Ridge Regression
- Lasso Regression
- Elastic Net Regression
- Decision Tree Regression
- Random Forest Regression
- Support Vector Regression (SVR)

---

## Typical Workflow

1. Import dataset
2. Split into training and testing sets
3. Preprocess data (if needed)
4. Train a regression model
5. Make predictions
6. Evaluate using MAE, MSE, RMSE, and R² Score
7. Compare multiple models
8. Select the best-performing model

---

## Applications

- House Price Prediction
- Salary Prediction
- Sales Forecasting
- Stock Price Analysis
- Weather Forecasting
- Energy Consumption Prediction
- Medical Cost Prediction

---

## Author

This repository provides beginner-friendly notes and code references for popular machine learning regression algorithms.
