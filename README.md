# Functional Cox Regression for Time-to-Event Prediction

This project develops functional survival analysis methods to predict peak performance timing in elite athletes. By treating longitudinal performance trajectories as smooth functions rather than discrete observations, we extend Cox proportional hazards models to incorporate phase-specific effects from entire career curves.

## Repository Contents

**FDA2.qmd**  
Core source code including data processing, functional data analysis, and all survival models (scalar Cox, random survival forest, functional linear Cox model, additive functional Cox model). Contains complete reproducible analysis pipeline.

**Functional_Cox_Regression_for_Time_to_Event_Prediction.pdf**  
First-author manuscript (version 3, under revision). Presents methodology and results from analyzing 67,977 athlete careers across 7 Olympic track-and-field event families.

**FDAOutline.pdf**  
Research design plan outlining the methodological framework and analytical approach.

**fda_data.csv**  
Complete dataset: 347,625 annual season-best observations from Olympic-level athletes (1996-2024). File stored via Git LFS (316 MB).

## Research Workflow

1. **Data Collection**: Compiled longitudinal performance records from World Athletics database covering 28 years of Olympic track-and-field competitions.

2. **Functional Representation**: Converted discrete yearly observations into smooth functional curves using B-spline basis expansion with integrated roughness penalties.

3. **Survival Modeling**: Fit four competing models to predict time-to-peak-performance:
   - Scalar Cox (baseline demographics only)
   - Random Survival Forest (scalar covariates)
   - Functional Linear Cox Model (FLCM with trajectory integrals)
   - Additive Functional Cox Model (AFCM with phase-specific effects)

4. **Model Evaluation**: Assessed discrimination (C-index) and calibrated time prediction accuracy (RMSE, MAE) on held-out test set.

5. **Interpretation**: Extracted phase-specific coefficient functions to identify which career stages most strongly predict timing of peak performance.

## Key Findings

Functional models (FLCM and AFCM) achieve superior predictive performance compared to scalar methods. The additive functional approach reveals that early-career performance patterns typically predict earlier peaks, while sustained late-career improvement predicts later peaks. These phase-specific insights are impossible to capture with traditional scalar covariates.

## Technical Details

Language: R (≥4.0)  
Key Packages: survival, mgcv, refund, randomForestSRC, splines  
Data: 67,977 careers | 347,625 observations  
Models: 4 survival models × 7 event families
