---
title: "Applied Linear Regression — Auto Dataset"
layout: default
---

# Applied Linear Regression on the Auto Data Set

**Author:** Ivan Johnson  
**Date:** 2025-11-24  

## Overview
This post walks through the applied linear regression tasks (simple and multiple) using the *Auto* dataset from the ISLR/ISLP collection. I performed model fitting with `statsmodels`, created diagnostic plots, investigated interactions, and tested a few transformations.

[Link to the notebook (GitHub) — `auto_regression.ipynb`](/assets/images/auto_regression.ipynb)

## Task A — Simple Linear Regression (mpg ~ horsepower)

### Model and results
I fit the simple OLS model `mpg ~ horsepower` using statsmodels. The regression summary shows a statistically significant relationship between horsepower and mpg (p-value << 0.05). The coefficient for horsepower is negative, which indicates that as horsepower increases, mpg decreases — consistent with intuition.

**Predicted mpg at horsepower = 98**: `X` mpg (include the exact number from your notebook run).  
**95% CI for mean prediction**: `(lower, upper)`  
**95% Prediction interval for a single car**: `(lower_obs, upper_obs)`

### Plots
- Scatterplot of mpg vs horsepower with the fitted least-squares line.  
- Diagnostic plots: Residuals vs Fitted, Normal Q-Q, Scale-Location, Influence plot.

**Commentary:** (copy your interpretation from the notebook). Mention whether residuals show heteroscedasticity, whether Q-Q suggests non-normality, and whether influential points exist.

## Task B — Multiple Linear Regression (mpg ~ all other predictors)

### Exploratory analysis
- Pairwise scatterplot matrix (pairplot) to visualize relationships.  
- Correlation matrix between variables (table inserted here).

### Full model results
I fit `mpg` on all predictors (cylinders, displacement, horsepower, weight, acceleration, year, origin). The ANOVA shows the predictors as a group are (significant / not significant — put actual result).  

**Significant predictors:** list predictors with p < 0.05 from the multiple regression.  
**Year coefficient interpretation:** (e.g., each additional year corresponds to an estimated X mpg increase, holding other predictors constant.)

### Diagnostics
- Residuals vs Fitted: (any pattern?)  
- Q-Q: (normality?)  
- Influence & Leverage: (list any high-leverage rows and their row numbers or names).

### Interactions & Transformations
- Interaction example: horsepower * weight — (did interaction have significant p-value?)  
- Transformations tried: log(horsepower), sqrt(weight), horsepower^2 — summarize which transformation improved model fit (e.g., lower AIC, increased adj. R^2)

## Reflective Summary
- Key findings (2–3 bullet points)  
- Limitations (data quality, model assumptions, omitted variables)  
- Ethical considerations: avoid over-generalizing; models are correlational, not causal.  

## Appendix
- Notebook link  
- All code and saved models
