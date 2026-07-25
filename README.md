# Logistic-Regression-Model-Selection
# ML Life Cycle: Evaluation and Deployment — Logistic Regression Model Selection


## Objective
Build, tune, evaluate, and deploy a logistic regression model that predicts `host_is_superhost` (True/False).

## Workflow Summary

### 1. Data Preparation
- Label: `host_is_superhost`
- Features: all other columns
- Train/test split: 90/10

### 2. Logistic Regression (Default)
- `C = 1.0`, `max_iter = 1000`
- Evaluated using confusion matrix, precision‑recall curve, ROC curve, and AUC  
- Default AUC: **0.8229**

### 3. Hyperparameter Tuning (GridSearchCV)
- Searched 10 values of `C` from `1e-05` to `10000`
- Best value: **C = 100**
- Best AUC: **0.8235**

### 4. Feature Selection (SelectKBest)
- Tested different numbers of features
- Best performance achieved with **7 features**
- AUC with 7 features: **0.8112**

### 5. Model Persistence
- Saved optimal model as `model_best.pkl`
- Reloaded and successfully used for predictions

## Key Findings
- Optimal regularization (`C = 100`) slightly improves AUC.
- Selecting 7 features produced the best feature‑subset performance.
- The model is packaged and ready for deployment.

## Files to Upload
- `model_best.pkl`
- `airbnbData_train.csv`
- `notebook.ipynb`
- `README.md`


