## Predicting ERP Implementation Duration using Machine Learning

This project investigates the use of various machine learning models to predict the **duration of ERP (Enterprise Resource Planning) system implementations**, measured in weeks. The dataset contains features such as project size, team characteristics, client attributes, and industry type.

We compare and evaluate models including **Random Forest Regressor**, **XGBoost**, and **LightGBM**, with the goal of identifying the most accurate and generalizable model for real-world prediction scenarios.

---

## 🧠 Problem Statement

ERP implementations are complex and often vary significantly in duration based on organizational and project factors. Accurately estimating project duration helps:

- Manage client expectations
- Plan team resources
- Reduce project overruns

This project aims to use **supervised regression models** to predict the `Duration_Weeks` of an ERP project based on known input features.

---

## 🧾 Dataset Overview

**Target variable:**
- `Duration_Weeks` (numeric)

**Feature examples:**
- `Num_Modules`
- `Customization_Level`
- `Team_Size`
- `Team_Experience_Years`
- `Client_Size`
- `Contract_Complexity`
- `Industry` (categorical)

---

## 📊 Models Evaluated

| Model                  | CV R² Score | Test MAE ↓ | Test R² ↑ |
|------------------------|-------------|------------|-----------|
| RandomForest (default) | N/A         | 1.93       | 0.53      |
| **RandomForest (tuned)**   | 0.472       | **1.90**    | **0.59**  |
| XGBoost (tuned)        | 0.474       | N/A        | N/A       |
| LightGBM (tuned)       | 0.430       | N/A        | N/A       |

---

## ✅ Final Conclusion

The **tuned RandomForestRegressor** achieved the best performance:

- ✔️ **Highest R² on test data (0.59)**
- ✔️ **Lowest MAE (1.90 weeks)**
- ✔️ Simple, robust, and interpretable

While XGBoost and LightGBM performed competitively in cross-validation, they **underperformed or showed instability** in this use case. Further preprocessing or feature engineering may improve their results in future iterations.

---

## 🧪 Tech Stack & Tools

- Python 3.8+
- pandas, NumPy
- scikit-learn
- XGBoost
- LightGBM
- Jupyter Notebooks
- matplotlib / seaborn (optional)

---
