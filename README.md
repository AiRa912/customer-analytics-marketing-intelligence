# Customer Analytics & Marketing Intelligence

End-to-end customer analytics project covering segmentation, campaign 
response prediction, spend behaviour, and LTV modelling — built on a 
real-world marketing dataset.

![Python](https://img.shields.io/badge/Python-3.10+-blue)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange)

---

## Overview

This project applies a full analytics workflow to a real-world marketing 
dataset — from raw data cleaning through to customer segmentation, 
predictive modelling, and an interactive Looker Studio dashboard.

Three core business questions drive the analysis:

1. **Who are our customers, and how do they differ?**
2. **Which customers are most likely to respond to a campaign?**
3. **Where should we focus retention and spend to maximise LTV?**

These are questions that matter across any growth-focused, data-driven 
business — from digital health to e-commerce to fintech.

---

## Project Structure
customer-analytics-marketing-intelligence/
│
├── data/
│   ├── raw/                        # Original dataset (gitignored)
│   └── processed/                  # Cleaned outputs from notebooks
│
├── notebooks/
│   ├── 01_eda_and_cleaning.ipynb
│   ├── 02_customer_segmentation.ipynb
│   ├── 03_campaign_response_prediction.ipynb
│   └── 04_ltv_and_spend_behaviour.ipynb
│
├── src/
│   ├── preprocessing.py            # Reusable cleaning functions
│   ├── segmentation.py             # Clustering logic
│   └── visualisation.py            # Reusable plot functions
│
├── reports/
│   └── figures/                    # Saved charts and plots
│
├── dashboard/
│   └── README.md                   # Looker Studio link + screenshots
│
├── .gitignore
├── requirements.txt
└── README.md


## Notebooks

### 01 — EDA & Data Cleaning
- Age derivation from `Year_Birth`, income outlier handling
- Missing value treatment and feature type validation
- Feature engineering: total spend across categories, customer tenure 
  (days since joining), campaign acceptance rate, household composition
- Distribution analysis across demographic and behavioural features

### 02 — Customer Segmentation
- K-Means and hierarchical clustering on spend + behavioural features
- Elbow method and silhouette scoring for optimal k selection
- Dimensionality reduction (PCA) for cluster visualisation
- Segment profiling: spend patterns, demographics, channel preferences

### 03 — Campaign Response Prediction
- Binary classification to predict likelihood of campaign response
- Models: Logistic Regression, Random Forest, XGBoost
- Evaluation: ROC-AUC, precision-recall curves, confusion matrix
- SHAP feature importance to explain model decisions

### 04 — LTV & Spend Behaviour
- Total and category-level spend analysis
- RFM (Recency, Frequency, Monetary) scoring
- LTV proxies by customer segment
- Channel preference breakdown (web vs store vs catalogue)

---

## Tech Stack

| Area | Tools |
|------|-------|
| Data processing | Python, Pandas, NumPy |
| Visualisation | Matplotlib, Seaborn |
| Machine learning | Scikit-learn, XGBoost, SHAP |
| Dashboard | Looker Studio |
| Environment | Jupyter Notebooks |

---

## Dashboard

Live Looker Studio dashboard → **[Link coming]**

Screenshots available in `dashboard/`

---

## Dataset

**Customer Personality Analysis** — available on 
[Kaggle](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)

2,240 customers · 29 features · Demographics, purchase behaviour, 
and campaign response history across 5 marketing campaigns.

---

## Key Features Engineered

| Feature | Description |
|---------|-------------|
| `Age` | Derived from `Year_Birth` |
| `Total_Spend` | Sum across all `Mnt` columns |
| `Customer_Tenure_Days` | Days since `Dt_Customer` |
| `Total_Campaigns_Accepted` | Sum of `AcceptedCmp1–5` |
| `Total_Children` | `Kidhome` + `Teenhome` |
| `Avg_Purchase_Value` | `Total_Spend` / total purchases |

---

## Getting Started

```bash
git clone https://github.com/yourusername/customer-analytics-marketing-intelligence
cd customer-analytics-marketing-intelligence
pip install -r requirements.txt
```

Download the dataset from Kaggle and place the CSV in `data/raw/`.

Then run notebooks in order starting with `01_eda_and_cleaning.ipynb`.

---

## License

Apache 2.0 — free to use, adapt, and build on but with added patent protection

---

## Author

Aishwarya Raman · [LinkedIn](https://www.linkedin.com/in/aishraman9/) 
