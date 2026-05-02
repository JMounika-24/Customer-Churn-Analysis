# Customer-Churn-Analysis

Project/ Title 

  📉 Telecom Customer Churn Analysis
 End-to-End Exploratory Data Analysis in Python

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-EDA-lightblue)
![NumPy](https://img.shields.io/badge/NumPy-Stats-orange)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Viz-green)
![Seaborn](https://img.shields.io/badge/Seaborn-Viz-teal)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

> A complete data analysis project on 7,043 telecom customer records — covering data loading, preprocessing, statistical modeling, and 11 inline visualizations — to uncover the root causes of customer churn.

---

 📌 Business Problem

> "How can a telecom company identify which customers are at risk of leaving — before they leave?"

Customer churn is one of the most expensive problems in telecom. This project analyses the full customer dataset to surface patterns, segment risk groups, and deliver actionable retention insights — using EDA

Target: `Churn` — whether the customer cancelled their service (Yes / No)

---

 🗂️ Project Structure

```
customer-churn-Analysis/
│
├── 📓 Customer Churn Analysis.py   # Main analysis script (run top to bottom)
├── 📁 Customer Churn.csv           # Raw dataset — 7,043 rows × 21 columns
└── 📄 README.md                    # Project documentation
```

---

 🛠️ Tech Stack

| Layer | Tool | Purpose |
|---|---|---|
| Data Manipulation | `pandas` | Loading, cleaning, groupby, pivot tables |
| Numerical Computing | `numpy` | Descriptive stats, encoding, histogram bins |
| Visualization | `matplotlib` | Histograms, bar charts, scatter, dual-axis |
| Visualization | `seaborn` | Count plots, heatmaps, themes |

> ⚠️ No machine learning used — this is a pure EDA & visualization project.

---

 📊 Dataset Overview
| Attribute | Details |
|---|---|
| Source | IBM Watson Telco Customer Churn |
| Records | 7,043 customers |
| Features | 21 columns |
| Target | Churn (Yes / No) |
| Churn Rate | 26.5% (1,869 churned / 5,174 retained) |

---

 🔬 Project Workflow — 4 Sections

 Section 1 — Data Loading
- Read CSV with `pd.read_csv()`
- Printed shape, dtypes, and first 5 rows
- Identified `TotalCharges` stored as string — flagged for fixing

 Section 2 — Data Pre-Processing
- ✅ Converted `TotalCharges` to numeric (fixed 11 null values)
- ✅ Encoded `Churn` → `Churn_Flag` (Yes=1 / No=0) using `np.where()`
- ✅ Engineered `TenureGroup` feature using `pd.cut()` → 5 bands (0–6, 7–12, 13–24, 25–48, 49–72 months)
- ✅ Computed descriptive statistics (mean, median, std) with NumPy

 Section 3 — Statistical Modeling (NumPy)
Computed group-level stats for churned vs retained customers:

| Feature | Churned (mean) | Not Churned (mean) |
|---|---|---|
| Tenure | 18.0 months | 37.6 months |
| Monthly Charges | $74.4 | $61.3 |
| Total Charges | $1,531 | $2,555 |

 Section 4 — 11 Inline Visualizations

| # | Chart | Key Finding |
|---|---|---|
| 1 | 🥧 Pie — Churn Distribution | 26.5% overall churn rate |
| 2 | 📊 Count — Churn by Contract Type | Month-to-month = 42.7% churn |
| 3 | 📊 Count — Churn by Internet Service | Fiber optic = 41.9% churn |
| 4 | 📈 Histogram — Monthly Charges | Churners pay $74 avg vs $61 |
| 5 | 📈 Histogram — Tenure | Churners cluster in first 6 months |
| 6 | 📉 Barh — Churn by Payment Method | Electronic check = 45.3% churn |
| 7 | 📊 Bar — Churn by Senior Citizen | Seniors churn at 41.7% |
| 8 | 🔥 Heatmap — Add-On Services | No security/support = highest churn |
| 9 | 🔵 Scatter — Tenure vs Charges | Churners: low tenure + high charges |
| 10 | 🔗 Heatmap — Correlation Matrix | Tenure −0.35 correlation with churn |
| 11 | 📉 Dual-Axis — Tenure Segments | ≤6 months tenure = 52.9% churn |

---

 💡 Key Business Insights

| Priority | Finding | Recommended Action |
|---|---|---|
| 🔴 Critical | Tenure ≤6 months → 52.9% churn | Early onboarding calls & check-ins |
| 🔴 Critical | Month-to-month → 42.7% churn | Offer discounts to switch to annual |
| 🟠 High | Electronic check → 45.3% churn | Incentivise auto-pay enrollment |
| 🟠 High | Fiber optic → 41.9% churn | Investigate pricing & quality issues |
| 🟡 Medium | Senior citizens → 41.7% churn | Simplified billing & senior support |
| 🟡 Medium | No Online Security → 41.8% churn | Bundle security with base plan |
---

 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn

python Customer Churn Analysis.py
```

> Place `Customer Churn.csv` in the same folder. Charts appear inline one by one — no files saved.

---

 🙋 About

Mounika Jarugumalli — Aspiring Data Analyst
Building end-to-end projects in Python, SQL, and Power BI.

⭐ If this project helped you, give it a star!
