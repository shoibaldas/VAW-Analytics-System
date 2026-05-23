# 📊 Violence Against Women (VAW) Analytics System — Bangladesh

![Python](https://img.shields.io/badge/Python-3.11-blue?style=flat-square&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square&logo=jupyter)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Data](https://img.shields.io/badge/Data-DHS%202022-blueviolet?style=flat-square)

An end-to-end machine learning and data analytics project predicting **intimate partner violence (IPV) risk factors** among women in Bangladesh, using the **Bangladesh Demographic and Health Survey (DHS) 2022** microdata. Model predictions are cross-validated against **BBS/UNFPA Violence Against Women Survey 2024** national findings — the largest VAW study ever conducted in Bangladesh (27,476 respondents).

---

## 🎯 Project Objectives

- Predict IPV vulnerability across demographic and geographic segments in Bangladesh
- Identify the strongest socioeconomic risk factors (age, education, division, wealth index, employment)
- Perform decade-long trend analysis by comparing DHS 2022 findings against BBS/UNFPA 2024 published results
- Visualize division-wise risk distribution across Bangladesh's 8 administrative divisions
- Provide interpretable, policy-relevant insights using SHAP explainability

---

## 📁 Project Structure

```
vaw-analytics-bangladesh/
│
├── data/
│   ├── raw/                  # DHS 2022 raw dataset (not included — see Data Access)
│   ├── processed/            # Cleaned and feature-engineered dataset
│   └── external/             # BBS/UNFPA 2024 aggregated statistics
│
├── notebooks/
│   ├── 01_data_exploration.ipynb       # EDA and data understanding
│   ├── 02_preprocessing.ipynb          # Cleaning, encoding, SMOTE
│   ├── 03_model_training.ipynb         # ML model training and evaluation
│   ├── 04_shap_explainability.ipynb    # SHAP analysis and feature importance
│   ├── 05_visualization.ipynb          # Risk maps and trend charts
│   └── 06_validation_2024.ipynb        # Cross-validation with BBS/UNFPA 2024
│
├── src/
│   ├── preprocessing.py      # Data cleaning utilities
│   ├── features.py           # Feature engineering
│   ├── models.py             # Model training pipeline
│   └── visualization.py      # Plotting and mapping utilities
│
├── reports/
│   └── figures/              # Exported charts and maps
│
├── requirements.txt
└── README.md
```

---

## 🗂️ Data Sources

### Primary Dataset
- **Bangladesh Demographic and Health Survey (DHS) 2022**
  - Source: [DHS Program](https://dhsprogram.com)
  - ~20,000+ individual-level respondents
  - Includes domestic violence module, socioeconomic indicators, geographic data
  - ⚠️ Raw data not included in this repository. Access requires free registration at [dhsprogram.com](https://dhsprogram.com/data/new-user-registration.cfm)

### Validation Reference
- **BBS/UNFPA Violence Against Women Survey 2024**
  - Source: [UNFPA Bangladesh](https://bangladesh.unfpa.org/en/2024-violence-against-women-survey)
  - 27,476 respondents across all 8 divisions
  - Used for trend validation and cross-referencing model outputs
  - Aggregated statistics extracted from the published highlights report

---

## 🧠 Methodology

### 1. Exploratory Data Analysis (EDA)
- Distribution of IPV types (physical, sexual, emotional, economic) by age group, division, education
- Urban vs. rural comparison
- Wealth index vs. violence prevalence correlation

### 2. Data Preprocessing
- Handling missing values and encoding categorical variables
- Feature selection based on domain knowledge and correlation analysis
- SMOTE (Synthetic Minority Oversampling Technique) for class imbalance

### 3. Machine Learning Models
| Model | Purpose |
|-------|---------|
| Logistic Regression | Baseline classifier |
| Random Forest | Ensemble model, feature importance |
| XGBoost | Gradient boosting, high performance |
| CatBoost | Handles categorical features natively |

### 4. Model Interpretability
- **SHAP values** to identify top contributing risk factors per prediction
- Feature importance ranking across models
- Division-level risk scoring

### 5. Validation Against 2024 Data
- Compare model-predicted high-risk segments with BBS/UNFPA 2024 findings
- Decade trend analysis: 2011 → 2015 → 2022 → 2024
- Division-wise agreement rate between predictions and national report

---

## 📊 Key Findings

> ⏳ Full results will be updated upon project completion.

Preliminary insights based on BBS/UNFPA 2024 published statistics:
- **76%** of Bangladeshi women have experienced some form of IPV in their lifetime
- Women aged **15–19** face the highest IPV rates (62%+ in the past 12 months)
- **Rural areas** consistently show higher vulnerability than urban zones
- **Education level** is one of the strongest protective factors against IPV
- **Climate-vulnerable and slum areas** show disproportionately higher risk

---

## 🗺️ Division-wise Risk Map

> ⏳ Map visualization will be added upon completion of notebook 05.

The risk map will visualize predicted IPV vulnerability scores across Bangladesh's 8 administrative divisions:
Dhaka · Chittagong · Rajshahi · Khulna · Barisal · Sylhet · Rangpur · Mymensingh

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python 3.11 |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-learn, XGBoost, CatBoost |
| Explainability | SHAP |
| Visualization | Matplotlib, Seaborn, Plotly |
| Geospatial | GeoPandas, Folium |
| Environment | Jupyter Notebook |
| Version Control | Git, GitHub |

---

## ⚙️ Installation & Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/vaw-analytics-bangladesh.git
cd vaw-analytics-bangladesh

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook
```

---

## 📦 Requirements

```
pandas>=2.0.0
numpy>=1.24.0
scikit-learn>=1.3.0
xgboost>=2.0.0
catboost>=1.2.0
shap>=0.44.0
matplotlib>=3.7.0
seaborn>=0.12.0
plotly>=5.15.0
geopandas>=0.14.0
folium>=0.14.0
imbalanced-learn>=0.11.0
jupyter>=1.0.0
```

---

## 📌 Project Status

| Phase | Status |
|-------|--------|
| Dataset access (DHS 2022) | ✅ Requested |
| Data exploration & EDA | ⏳ In Progress |
| Preprocessing pipeline | ⏳ Pending |
| Model training | ⏳ Pending |
| SHAP analysis | ⏳ Pending |
| Risk map visualization | ⏳ Pending |
| 2024 validation layer | ⏳ Pending |

---

## 📜 Data Usage & Ethics

- DHS 2022 data is used strictly for academic and research purposes in accordance with the [DHS Program Data Use Agreement](https://dhsprogram.com/data/terms-of-use.cfm)
- No individual-level raw data is shared or included in this repository
- This project does not attempt to identify or profile individual respondents
- Findings are intended to support evidence-based policy and research — not for commercial use

---

## 🔗 References

- Bangladesh Bureau of Statistics (BBS) & UNFPA. *Violence Against Women Survey 2024*. [Link](https://bangladesh.unfpa.org/en/2024-violence-against-women-survey)
- ICF. *Bangladesh Demographic and Health Survey 2022*. DHS Program. [Link](https://dhsprogram.com)
- WHO. *Violence against women prevalence estimates, 2018*. [Link](https://www.who.int/publications/i/item/9789240022256)
- Lundberg, S. & Lee, S.I. *A Unified Approach to Interpreting Model Predictions (SHAP)*. NeurIPS 2017.

---

---

> *This project is part of a personal research portfolio developed for MSc program applications in Artificial Intelligence and Data Science.*
