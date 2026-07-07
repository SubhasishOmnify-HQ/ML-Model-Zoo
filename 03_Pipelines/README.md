# Scikit-learn Pipeline and ColumnTransformer

## What is a Pipeline?

A **Pipeline** is a Scikit-learn utility that chains multiple machine learning steps into a single workflow. It applies each step in sequence and ensures that preprocessing and model training are performed consistently.

### Why Use a Pipeline?

* Organizes preprocessing and model training in one object.
* Prevents data leakage by fitting preprocessing only on training data.
* Simplifies training, prediction, and deployment.
* Works seamlessly with Cross Validation and GridSearchCV.
* Produces cleaner, reusable, and maintainable code.

### Common Pipeline Steps

* Missing Value Imputation
* Feature Scaling
* Feature Selection
* Dimensionality Reduction (PCA)
* Machine Learning Model

### Example Workflow

```text
Dataset
   │
   ▼
StandardScaler
   │
   ▼
Feature Selection
   │
   ▼
Logistic Regression
```

### Basic Syntax

```python
from sklearn.pipeline import Pipeline

pipeline = Pipeline([
    ("scaler", StandardScaler()),
    ("model", LogisticRegression())
])

pipeline.fit(X_train, y_train)
```

---

# What is a ColumnTransformer?

A **ColumnTransformer** applies different preprocessing techniques to different columns of the dataset. It is useful when numerical and categorical features require different transformations.

### Why Use a ColumnTransformer?

* Applies different preprocessing to different feature types.
* Handles mixed datasets efficiently.
* Keeps preprocessing organized and reusable.
* Integrates directly with a Pipeline.

### Common Transformations

**Numeric Columns**

* SimpleImputer
* StandardScaler
* MinMaxScaler
* RobustScaler

**Categorical Columns**

* SimpleImputer
* OneHotEncoder
* OrdinalEncoder

### Example Workflow

```text
Dataset
      │
      ├───────────────┐
      ▼               ▼
Numeric         Categorical
Columns            Columns
      │               │
StandardScaler  OneHotEncoder
      └───────┬───────┘
              ▼
      Combined Features
```

### Basic Syntax

```python
from sklearn.compose import ColumnTransformer
from sklearn.preprocessing import StandardScaler, OneHotEncoder

preprocessor = ColumnTransformer([
    ("num", StandardScaler(), numeric_columns),
    ("cat", OneHotEncoder(), categorical_columns)
])
```

---

# Pipeline vs ColumnTransformer

| Feature                        | Pipeline                    | ColumnTransformer                                     |
| ------------------------------ | --------------------------- | ----------------------------------------------------- |
| Purpose                        | Executes steps sequentially | Applies different transformations to selected columns |
| Works On                       | Entire dataset              | Specific columns                                      |
| Contains Model                 | Yes                         | No                                                    |
| Used for Preprocessing         | Yes                         | Yes                                                   |
| Used for Training              | Yes                         | No                                                    |
| Supports Multiple Transformers | No (one sequence)           | Yes                                                   |

---

# Using Pipeline and ColumnTransformer Together

In real-world machine learning projects, **ColumnTransformer** is commonly used inside a **Pipeline**.

### Workflow

```text
Dataset
   │
   ▼
ColumnTransformer
   │
   ├── Numeric Pipeline
   │      ├── SimpleImputer
   │      └── StandardScaler
   │
   └── Categorical Pipeline
          ├── SimpleImputer
          └── OneHotEncoder
   │
   ▼
Machine Learning Model
   │
   ▼
Prediction
```

### Example

```python
pipeline = Pipeline([
    ("preprocessor", preprocessor),
    ("model", LogisticRegression())
])
```

---

# When to Use Pipeline

Use a **Pipeline** when:

* All features require the same preprocessing.
* The dataset contains only numerical features.
* Building a clean and reusable machine learning workflow.

Examples:

* Iris Dataset
* Wine Dataset
* Breast Cancer Dataset

---

# When to Use ColumnTransformer

Use a **ColumnTransformer** when:

* The dataset contains both numerical and categorical features.
* Different columns require different preprocessing methods.

Examples:

* Titanic Dataset
* House Price Prediction
* Customer Churn Prediction
* Loan Prediction

---

# Best Practices

* Perform `train_test_split()` **before** fitting the pipeline.
* Include preprocessing inside the pipeline to avoid data leakage.
* Use `ColumnTransformer` for mixed data types.
* Use `GridSearchCV` or `RandomizedSearchCV` with the complete pipeline.
* Save the entire pipeline using `joblib` or `pickle` for deployment.

---

# Summary

* **Pipeline** executes preprocessing and model training in sequence.
* **ColumnTransformer** applies different preprocessing to different feature groups.
* **ColumnTransformer** is often the preprocessing step inside a **Pipeline**.
* Together, they create clean, reusable, and production-ready machine learning workflows.
