# Car Price Regression Analysis

A concise, reproducible project to **model and explain used-car prices**. We explore features (age, mileage, brand, engine, fuel, transmission, etc.), run baseline and regularized **regression models**, and compare performance (RMSE/MAE/R²). The repository includes a short report summarizing findings.

---

## Goals
- **EDA**: understand distributions, outliers, and correlations.
- **Feature engineering**: encode categorical variables, create age/mileage transforms, handle missing values.
- **Modeling**: compare linear and **regularized** baselines (e.g., Ridge/Lasso) and optionally **tree-based** regressors.
- **Evaluation**: RMSE/MAE/R² on hold-out or cross-validation; simple error plots and feature importance.

---

## Repository structure
.
├─ Data/ # raw or prepared datasets (place files here; see Data/README if added) /
├─ Report/ # project report (PDF/Docx) and any exported figures/tables /
└─ README.md /


**Data policy.** If the dataset is from a public source (e.g., Kaggle), do not commit large/raw files; instead, link instructions to download in `Data/README.md`. If small, anonymized samples are allowed, you can include a 100–1,000 row sample for quick testing.

---

## Quick start

> This project can be run in **Python** or **R** depending on your scripts/notebooks. Keep one path and delete the other once you finalize.

### Run in ** R **
1. Install packages:
```
  pkgs <- c("tidyverse","janitor","skimr","GGally","caret","glmnet","rpart","ranger","ggplot2")
  to_install <- setdiff(pkgs, rownames(installed.packages()))
  if(length(to_install)) install.packages(to_install)
```

2. Put data in Data/.

3. Knit the analysis Rmd or run the R script(s).

## Reproducibility checklist
  
  Random seeds fixed during CV/splits.
  
  Data versions documented (source URL, download date).
  
  Environment pinned (Python requirements.txt or R renv.lock).
  
  Outputs: keep a few key plots/tables inside Report/ so visitors see results without running code.

## Results (short preview)

  Top predictors typically include age and mileage, with brand/segment fixed effects improving fit.
  
  Regularization (Ridge/Lasso) often improves generalization vs. plain OLS; tree-based models can capture non-linearities (check SHAP or permutation importance for interpretability).
  
  Replace this section with your actual metrics table (RMSE/MAE/R²) and 1–2 plots exported to Report/.

## How to cite

If you use this repo:
```
Jinmin Li. Sicheng Huang. Zixiang Xiao. Yifan Wang (2024). Car Price Regression Analysis. Repository: https://github.com/Lexie000/Car_price_regression_analysis
```
