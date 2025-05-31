# ❤️ Heart Disease Prediction Using Machine Learning

This project develops a machine learning model to **predict the presence of heart disease** using clinical and demographic patient data. The goal is to support early screening and assist physicians in making better decisions during routine checkups.

---

## 🎯 Objective

To build and evaluate a predictive model that classifies whether a patient is at risk of heart disease based on their health records, helping detect high-risk cases early.

---

## 🗃️ Dataset Overview

- Source: Public health dataset used in clinical prediction tasks
- Total records: ~5,000+
- Target variable: Binary (`1 = Disease`, `0 = No Disease`)
- Features: Age, Blood Pressure, Cholesterol, Weight, etc.

---

## 🧹 Data Preprocessing

- Removed extreme outliers (e.g., abnormal BP and weight)
- Converted `age` from days → years
- Encoded categorical variables
- Scaled numerical variables
- Handled nulls and inconsistencies

---

## 📊 Exploratory Data Analysis (EDA)

- **Boxplots** identified BP outliers
- **Correlation heatmap** highlighted strong links (age, BP)
- **Partial Dependence Plots (PDPs)** revealed risk increases with age and weight

---

## 🤖 Models Used

| Model | Description |
|-------|-------------|
| **XGBoost** | Best performance with high recall and F1 score |
| **Random Forest** | Strong accuracy, interpretable |
| **Logistic Regression** | Baseline model |

---

## 🧪 Model Evaluation

| Metric         | XGBoost  | Random Forest | Logistic Regression |
|----------------|----------|----------------|---------------------|
| F1 Score       | 0.723    | ~0.68          | Lower               |
| ROC-AUC        | 0.801    | ~0.75          | ~0.71               |
| Recall (Disease)| High     | Medium         | Low                 |

> ⚠️ **Imbalanced classes** handled through feature scaling and tuning, but future work may use SMOTE or ensemble boosting.

---

## 📌 Feature Importance

Top predictors across models:
- **Age** 
- **Systolic BP (ap_hi)** 
- **Cholesterol** 
- **Weight** 

Interpretation verified through:
- Permutation importance
- Partial Dependence Plots

---

## 💡 Real-World Applications

- Assist clinicians in early detection of at-risk patients
- Flag high-risk individuals for further testing
- Integrate into EHR dashboards for real-time screening

---

## 🔬 Limitations & Future Work

- No lab/ECG data (just clinical metrics)
- Cross-sectional data only (no patient history)
- Binary target – lacks condition severity or timing

✅ Future Work:
- Add lab values and ECG readings
- Test on new hospital datasets
- Deploy pilot model with clinician feedback

---

## 🧰 Tech Stack

- Python, Pandas, Scikit-learn, XGBoost
- Matplotlib, Seaborn, Jupyter Notebook

---

## 📫 Contact

**Ibrahim Fahd Bindawod**  
 
📧 ibrahim.bindawod@gmail.com

---

> “The best treatment starts with early detection — let data help save lives.”
