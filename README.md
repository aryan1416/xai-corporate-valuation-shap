# Explainable AI in Corporate Valuation  
## A SHAP-Based Approach to Enhancing Transparency

This repository contains the code used for the empirical analysis in the paper:

**"Explainable AI in Corporate Finance: A SHAP-Based Approach to Enhancing Transparency"**

---

## 📌 Overview

The objective of this project is to investigate whether explainable machine learning methods—specifically the combination of **XGBoost** and **SHAP (Shapley Additive Explanations)**—enable a transparent and economically interpretable valuation of firms.

The analysis compares a non-linear machine learning model (XGBoost) with a classical linear regression (OLS) and evaluates how SHAP enhances interpretability.

---

## ⚙️ Methodological Workflow

The notebook follows a structured pipeline:

### 1. Data Loading
- Financial dataset of publicly listed U.S. firms
- Source: Kaggle (financial statements & market data)

### 2. Data Preprocessing
- Conversion to numeric format
- Handling missing values (median imputation)
- Winsorization (1st–99th percentile)
- Log-transformation of Market Cap
- Removal of leakage variables (e.g., Enterprise Value)

### 3. Feature Selection
- XGBoost feature importance
- Mutual Information (MI)
- Correlation filtering (ρ-threshold)
- Economic plausibility validation

### 4. Model Training
- Linear Regression (OLS) as baseline model
- XGBoost Regressor for non-linear modeling
- Train-test split (80/20)
- Cross-validation (10-fold)

### 5. Model Evaluation
- R²
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)

### 6. Explainability (SHAP)
- Global feature importance (mean |SHAP|)
- SHAP summary plots
- Local explanations (waterfall plots)
- Comparison with OLS coefficients

---

## 📊 Key Features of the Analysis

- Combination of **predictive performance and interpretability**
- Identification of **non-linear effects and interaction mechanisms**
- Comparison of **statistical vs. explainable importance**
- Application in a **financial valuation context**

---

## 📁 Repository Structure

- `Methodik and Results.ipynb` → main analysis notebook
- `requirements.txt` → package dependencies

---

## 📂 Data

The dataset used in this study is publicly available via Kaggle: 
**https://www.kaggle.com/datasets/cnic92/200-financial-indicators-of-us-stocks-20142018**
Due to licensing restrictions, it is not included in this repository.

Please download the dataset manually and update the file path in the notebook:

```python
file = "Financial_data.xlsx"
