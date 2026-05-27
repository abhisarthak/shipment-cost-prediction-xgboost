# 🚚 Shipment Cost Prediction using XGBoost & SHAP

Explainable shipment cost prediction using XGBoost, SHAP, and real-world supply chain data.

---

# 📌 Overview

This project focuses on predicting total shipment cost using machine learning on real-world logistics and supply chain data.

The objective is to move from:

> Reactive cost reporting → Proactive cost forecasting

The project combines:
- XGBoost Regression
- Feature Engineering
- SHAP Explainability
- End-to-End ML Pipelines

to build an interpretable shipment cost prediction system.

---

# 🎯 Problem Statement

Manual shipment cost estimation in logistics operations often leads to:
- budgeting variance
- delayed decision-making
- reduced profitability
- inefficient vendor planning

This project addresses these challenges using predictive analytics and explainable AI.

---

# 📊 Dataset

Dataset Used:
- SCMS Delivery History Dataset (Open Source Logistics Dataset)

Dataset Characteristics:
- Numerical Features
- Categorical Features
- Temporal Features
- High-cardinality variables
- Missing values
- Real-world noisy logistics data

---

# ⚠️ Data Challenges

The dataset contains:
- mixed currency/unit strings
- sparse categorical features
- inconsistent formatting
- missing values

Example:
```python
"$1,250.75 kg" → 1250.75
```

These values were cleaned using RegEx-based preprocessing.

---

# 🧹 Data Preprocessing

Key preprocessing steps:
- RegEx cleaning
- Missing value imputation
- Feature scaling
- OneHotEncoding
- Log transformation of target variable

---

# ⚙️ Feature Engineering

Derived Feature:
```python
Planning_Lead_Time_Days =
PO Sent to Vendor Date -
PQ First Sent to Client Date
```

This captures procurement planning efficiency.

---

# 🤖 Model Used

## XGBoost Regressor

Why XGBoost?
- High performance on structured data
- Handles sparse features efficiently
- Strong predictive capability
- Supports SHAP explainability

Key Hyperparameters:
```python
n_estimators = 500
learning_rate = 0.05
max_depth = 5
```

---

# 📈 Evaluation Metrics

Train-Test Split:
- 80% Training
- 20% Testing

Metrics Used:
- RMSE
- MAPE

Performance:
```python
RMSE = 56540.37
MAPE = 20.95%
```

---

# 🧠 SHAP Explainability

SHAP (SHapley Additive exPlanations) was used to interpret feature contributions toward shipment cost prediction.

Major cost-driving features:
- Line Item Quantity
- Pack Price
- Unit Price
- Weight (Kilograms)
- Vendor
- Manufacturing Site

---

# 🚀 Future Scope

Planned improvements:
- Geospatial distance modeling
- Bayesian hyperparameter optimization
- Time-series shipment forecasting
- Dashboard deployment
- Real-time prediction system

---

# 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib

---

# 🚧 Project Status

Currently:
- Understanding model behavior deeply
- Improving preprocessing pipeline
- Enhancing feature engineering
- Exploring SHAP interpretability

Code implementation and deployment will be uploaded progressively.

---

# 📚 References

1. Chen & Guestrin (2016) — XGBoost
2. Lundberg & Lee (2017) — SHAP
3. SCMS Delivery History Dataset

---

# 🎯 Key Takeaway

This project demonstrates how explainable machine learning can support data-driven logistics optimization and proactive shipment cost forecasting in supply chain systems.
