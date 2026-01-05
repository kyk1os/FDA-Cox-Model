# Functional Cox Regression for Time-to-Event Prediction

This repository contains the code and data for applying functional Cox regression to predict time-to-peak performance in elite track-and-field athletes.

## Overview

We analyze longitudinal performance trajectories from 67,977 athlete-event careers to predict when athletes will reach their peak performance. The project demonstrates how functional data analysis (FDA) combined with Cox regression models can extract phase-specific insights from irregular time series data.

## Key Features

- **Functional Cox Models**: Treats full performance trajectories as functional covariates rather than scalar summaries
- **Large-Scale Analysis**: 347,625 yearly observations from Olympic-level athletes (1996-2024)
- **Phase-Specific Insights**: Reveals which career phases are most predictive of peak timing
- **Model Comparison**: Evaluates scalar Cox, random survival forest, functional linear Cox (FLCM), and additive functional Cox (AFCM) models

## Repository Contents

- `FDA2.qmd`: Main analysis notebook with all models and visualizations
- `fda_data.csv`: Source dataset (Olympic athlete performance data via Git LFS)
- `olympic_results.csv`: Processed Olympic results
- `paper_draft.tex`: LaTeX manuscript draft
- `output/`: Generated figures and tables for publication
- `Functional_Cox_Regression_for_Time_to_Event_Prediction.pdf`: Current paper draft

## Methods

The project implements:
- Time normalization and B-spline smoothing of irregular trajectories
- Cox proportional hazards models with functional covariates
- Calibration for absolute time-to-event prediction
- Phase-specific effect estimation (early, mid, late career)

## Applications

Beyond sports analytics, this framework applies to:
- Medical biomarker trajectories predicting disease onset
- Equipment sensor data predicting failure times
- User engagement patterns predicting churn
- Any domain with longitudinal monitoring and time-to-event outcomes

## Citation

If you use this code or methodology, please cite:
```
Functional Cox Regression for Time-to-Event Prediction: 
Learning Phase-Specific Effects from Longitudinal Trajectories
[Author information to be added]
```

## Requirements

- R (≥4.0)
- Key packages: `survival`, `mgcv`, `refund`, `randomForestSRC`
- See analysis file for complete dependencies

## Contact

For questions or collaboration inquiries, please open an issue or contact the repository owner.

---

**Keywords**: Functional Data Analysis, Survival Analysis, Sports Analytics, Longitudinal Data, Cox Regression, Explainable AI

