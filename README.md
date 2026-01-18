# Functional Cox Regression for Time-to-Event Prediction

**Undergraduate Research Project**  
*Supervised by Dr. Samuel Wong*  
*Predicting peak performance timing in elite athletes using functional survival analysis*

---

## 📂 Repository Contents

### 🔬 Core Analysis File
- **`FDA2.qmd`**  
  Complete source code including data processing, functional data analysis, and all survival models (Cox, RSF, FLCM, AFCM). Contains ~4,000 lines of reproducible R code with full documentation.

### 📄 Manuscript
- **`Functional_Cox_Regression_for_Time_to_Event_Prediction.pdf`**  
  First-author manuscript (v3, under revision). Presents methodology, results, and phase-specific functional insights from analyzing 67,977 athlete careers.

### 📋 Research Design
- **`FDAOutline.pdf`**  
  Research design plan and methodological framework outlining the project structure and analytical approach.

### 📊 Data
- **`fda_data.csv`**  
  Complete dataset: 347,625 annual season-best observations from Olympic-level track-and-field athletes (1996-2024). Stored via Git LFS (316 MB).

---

## 🎯 Project Summary

**Research Question:** Can we predict when elite athletes will reach peak performance by analyzing their career progression curves?

**Methodology:**
- Functional Data Analysis (FDA) treats performance trajectories as smooth functions
- Cox proportional hazards models extended with functional covariates
- Comparison: Scalar Cox vs. Random Survival Forest vs. Functional Linear Cox Model (FLCM) vs. Additive Functional Cox Model (AFCM)

**Key Findings:**
- Functional models (FLCM/AFCM) achieve best discrimination (C-index) and lowest prediction errors
- Phase-specific coefficient functions reveal which career stages are most predictive
- Early-career performance typically predicts earlier peaks; sustained late-career performance predicts later peaks

**Applications:** Beyond sports analytics, this framework applies to medical biomarkers, equipment reliability, user engagement analytics, and any domain with longitudinal monitoring.

---

## 🔧 Technical Details

- **Language:** R (≥4.0)
- **Key Packages:** `survival`, `mgcv`, `refund`, `randomForestSRC`, `splines`
- **Data Size:** 67,977 athlete-event careers | 347,625 yearly observations
- **Models:** 4 survival models across 7 event families
- **Evaluation:** 80/20 train-test split with C-index, RMSE, MAE metrics

---

## 📈 Impact

This research demonstrates that functional Cox regression provides:
1. ✅ **Better prediction** - Improved discrimination and calibrated time-to-event forecasts
2. ✅ **Interpretable insights** - Phase-specific effects reveal when trajectory shape matters most
3. ✅ **Broad applicability** - Framework generalizes to clinical, engineering, and behavioral domains

---

## 📖 Citation

```
Functional Cox Regression for Time-to-Event Prediction: 
Learning Phase-Specific Effects from Longitudinal Trajectories
Kyle Ye (supervised by Dr. Samuel Wong)
[Under Revision, 2025]
```

---

## 🔗 Keywords

Functional Data Analysis · Survival Analysis · Cox Regression · Longitudinal Data · Sports Analytics · Time-to-Event Prediction · B-Spline Smoothing · Phase-Specific Effects

---

*For questions or collaboration: GitHub @kyk1os*
