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

  ## 📊 Key Project KPIs

This section tracks the most important metrics derived from the exploratory and data preparation phases. These KPIs help quantify user behavior, data quality, and dataset readiness for downstream machine learning tasks.

| KPI | Value | Notes |
|-----|-------|-------|
| **Repeat Buyer Rate** | 9.5% | % of users (USER_IDs) with more than one purchase |
| **Total Users Analyzed** | 19,851 | Unique USER_IDs in the dataset |
| **Repeat Buyers** | 1,889 | Users with more than one ORDER_ID |
| **One-Time Buyers** | 17,962 | Users with exactly one ORDER_ID |
| **Final Dataset Rows** | 19,851 | 1 row per user (first purchase only, for modeling prep) |
| **Engineered Features** | _To be defined_ | Will include: shipping delay, platform, weekday, etc. |
| **Target Variable** | `IS_REPEAT_BUYER` | Binary target: 1 = repeat, 0 = one-time |
| **Target Class Balance** | 9.5% positive / 90.5% negative | Indicates imbalance for classification models |
| **% Missing (Post-Cleaning)** | _To be calculated_ | Will track after data cleaning is complete |
| **Average Order Value (AOV)** | _To be calculated_ | Mean price per order (can segment by buyer type) |
| **Average Time to Repeat Purchase** | _To be calculated_ | Days between 1st and 2nd order for repeat buyers |

### ➕ Additional EDA Metrics (Planned)

The following KPIs will be calculated and analyzed during EDA:
- **Repeat rate by platform:** Desktop vs. Mobile behavior patterns
- **Repeat rate by marketing channel:** Effectiveness of each acquisition source
- **Impact of shipping delay:** How shipping speed affects repeat likelihood
- **Repeat rate by country:** Retention trends across different markets

These KPIs will support strategic recommendations and feature engineering for machine learning readiness.


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



