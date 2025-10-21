
# 🎗️ Cancer-Data-Analysis

A concise, fully reproducible exploratory data analysis (EDA) and initial modeling project built on a 50,000‑record synthetic cancer patient dataset (global_cancer_patients_2015_2024). The repository contains an interactive notebook and a Python script that fetch, profile, visualize, and run initial predictive models examining cancer severity, survival, and economic burden.

> ⚠️ Note: The dataset used in the analysis is a synthetic Kaggle dataset (zahidmughal2343/global-cancer-patients-2015-2024). Results are illustrative and intended for method demonstration and exploration.

---

## 📁 Contents
- `🎗️Cancer_Data_Analysis (1).ipynb` — Jupyter/Colab notebook with full EDA, profiling, visualizations, tests, and modeling.
- `🎗️cancer_data_analysis.py` — Script auto-exported from the notebook (same steps in script form).
- `Cancer Data Anlysis.pdf` — Exported static report.
- `README.md` — This file.

---

## 🔍 Quick summary — important findings
- 🧾 Data: 50,000 synthetic patients (2015–2024), 8 cancer types, 10 countries.
- 👥 Demographics:
  - Age range ≈ 20–89 (mean ~54.4).
  - Gender categories: Male, Female, Others (Male most frequent).
  - Patients from 10 countries with roughly even distribution.
- 🦠 Cancer types & stages:
  - 8 cancer types, stages from Stage 0 → Stage IV.
  - Early-stage (Stage 0/I) diagnoses across cancers ~38–41% (varies; lung lower).
- ⚖️ Risk factors vs Severity:
  - Factors: Genetic_Risk, Air_Pollution, Alcohol_Use, Smoking, Obesity_Level.
  - Positive slopes vs severity but weak linear relationships:
    - Genetic_Risk ≈ R² 0.23
    - Smoking ≈ R² 0.23
    - Air_Pollution ≈ R² 0.13
    - Alcohol_Use ≈ R² 0.13
    - Obesity_Level ≈ R² 0.06
  - ⇒ These single features explain only a small portion of severity variance — consider interactions or more features.
- 🧠 Modeling (Target_Severity_Score):
  - Model: RandomForestRegressor + GridSearchCV.
  - Top features: Smoking, Genetic_Risk, Treatment_Cost_USD, Alcohol_Use, Air_Pollution.
  - Model provides relative importance but limited predictive power.
- 📊 Tests & stats:
  - Treatment cost vs Survival_Years: no meaningful correlation (Pearson/Spearman).
  - Treatment cost & Survival_Years across Cancer_Stage: Kruskal–Wallis → no significant differences.
  - Genetic_Risk × Smoking interaction on severity: not significant (p > 0.05).

---



---

## ✅ Recommended next steps
- 🚀 Improve modeling:
  - Add interaction features, try gradient boosting (XGBoost/LightGBM), regularized models, and SHAP for explainability.
- 🔬 External validation:
  - Validate on real-world datasets when possible (synthetic limits generalizability).
- ⏳ Survival analysis:
  - Use time-to-event modeling (Cox proportional hazards) for survival outcomes if follow-up data available.
- 🧩 Reproducibility:
  - Add `requirements.txt`, a small `run.sh`, or a Colab/Binder badge for one-click reproducibility.

---

## ⚙️ Notes & caveats
- This repository uses synthetic data — treat effect sizes as illustrative.
- `ydata-profiling` creates large HTML reports best viewed in notebooks.
- Many interpretation notes are inline in the notebook for transparency.

---

## 📬 Contact
- Author: kshirod46 (GitHub)
- If you'd like this README adapted (short executive version, portfolio landing, or `requirements.txt` + run script), I can add it.

```
