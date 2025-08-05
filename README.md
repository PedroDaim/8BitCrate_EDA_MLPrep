# 🛒 Repeat Buyer Prediction - EDA & ML Dataset Prep

## 🔍 Objective
Understand what drives repeat purchases in an online video game store and prepare a machine learning-ready dataset to predict if a new customer will become a repeat buyer.

---

## 🧱 CRISP-DM Approach

### 1. Business Understanding
- Improve retention and campaign targeting by identifying early indicators of repeat purchasing behavior.

### 2. Data Understanding
- 20k+ purchase records
- Fields include user behavior, timestamps, platforms, marketing channels, and more.

### 3. Data Preparation
- Created `IS_REPEAT_BUYER` target (repeat if >1 order)
- Engineered features: shipping delay, platform, marketing source, purchase weekday, etc.
- Final dataset: 1 row per user (first purchase only)

### 4. Modeling Prep
- Class imbalance noted: ~9.5% are repeat buyers
- Dataset is ready for classification tasks with standard models

### 5. Evaluation (EDA Only)
- Detailed comparison of one-time vs. repeat buyers
- Feature distributions, correlations, and trends

---

## 📁 Files

| File | Description |
|------|-------------|
| `notebooks/01_eda.ipynb` | Data profiling, outlier detection, retention trends |
| `notebooks/02_feature_eng.ipynb` | Cleaned dataset, label creation, feature logic |
| `data/processed/final_ml_dataset.csv` | Clean ML-ready data with features + label |
| `scripts/make_dataset.py` | Code to generate the processed dataset |
| `assets/visuals/` | Charts used in EDA |
| `README.md` | Project summary and process |

---

## 📈 Key EDA Insights

-- Coming Soon


---

## 📦 Next Steps (For DS Handoff)

- Model using `final_ml_dataset.csv`
- Recommended metrics: **F1-score**, **AUC**
- Consider resampling (e.g. SMOTE) to balance classes

---

## ✍️ Author

Pedro Daim — Data Analyst  
[🔗 LinkedIn](https://www.linkedin.com/in/data-daim/)


