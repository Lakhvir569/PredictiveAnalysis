# Student Dropout Prediction Model

**Type:** Solo Project

## Overview
Built a logistic regression model using generalized linear modeling (GLM) to predict whether university students would graduate or drop out, achieving 84.98% accuracy. Applied iterative variable selection to identify the most significant predictors of student dropout risk.

## Problem
University dropout rates represent a significant challenge for institutions and students alike. The goal was to build a predictive model that identifies students most at risk of dropping out, enabling targeted early intervention.

## Dataset
- **2,904 observations** across 14 variables
- Variables included: mother's qualification, admission grade, scholarship status, tuition fees paid, second semester grades, gender, and more
- Source: Student Dropout dataset

## Approach
1. Fit a full multivariate GLM (logistic) with all 14 variables as a baseline
2. Identified and removed non-significant variables (p > 0.05)
3. Dropped course enrollment variable (not predictive by design — students can change courses)
4. Built a reduced parsimonious model retaining only statistically significant predictors
5. Evaluated on held-out test set of 726 observations

## Results
| Model | Accuracy |
|---|---|
| Full model (all variables) | 84.98% |
| Reduced model (significant only) | 84.02% |
| Test set predictions correct | 610 / 726 |

Models performed nearly identically, favouring the parsimonious reduced model.

## Top Predictors
| Variable | Direction | Interpretation |
|---|---|---|
| Tuition fees paid to date | Positive | Strongest predictor of graduation |
| Scholarship holder | Positive | Significantly reduces dropout risk |
| Second semester grade | Positive | Academic momentum matters |
| Outstanding debt | Negative | Highest risk indicator for dropout |

## Tech Stack
`Python` `pandas` `numpy` `sklearn` `statsmodels` `GLM` `Logistic Regression`

## Files
- `PredictiveAnalysisReport.pdf` — Full project report with model output and analysis
- `PredictiveAnalysis.ipynb` — Full Python Jupyter Notebook with code and output
