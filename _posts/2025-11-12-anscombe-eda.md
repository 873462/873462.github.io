---
layout: default
title: "Anscombe’s Quartet – Exploratory Data Analysis (EDA)"
author: Ivan Johnson
date: 2025-10-08
---

[Home](/)

# Anscombe’s Quartet – Exploratory Data Analysis (EDA)
*By Ivan Johnson — October 9, 2025*

---

[Download CSV data](../assets/anscombe.csv){: .button }
[Download full PDF report](../assets/anscombe_eda.pdf){: .button }

---

# Abstract

This report presents a full exploratory data analysis (EDA) of **Anscombe’s Quartet**, a classic example demonstrating why data visualization is essential in statistical analysis. While the four datasets share nearly identical summary statistics—mean, variance, correlation, and regression coefficients—their visual structures differ dramatically.

Using Python libraries including **Pandas**, **NumPy**, **Seaborn**, **Matplotlib**, and **Plotly**, this analysis includes:
- summary statistics  
- regression analysis  
- residual diagnostics  
- box plots  
- violin plots  
- scatterplots  
- interactive visualizations

This study emphasizes how relying solely on numerical summaries can lead to misinterpretation, while combining statistical metrics with visual inspection reveals patterns, anomalies, and structures otherwise hidden.

---

# Introduction

Anscombe’s Quartet, introduced by Francis Anscombe in 1973, is one of the most famous demonstrations in statistics. It highlights a major problem analysts face today: **summary statistics alone do not accurately describe data**.

Each of the four datasets (I, II, III, IV) have:
- identical x-mean (9.0)  
- identical y-mean (~7.5)  
- identical x-variance and y-variance  
- nearly identical correlation coefficients  
- nearly identical linear regression lines  

Yet, the datasets behave **completely differently** when visualized.

This is the foundation of **Exploratory Data Analysis (EDA)**, which combines:
- summary statistics  
- visualizations  
- structure detection  
- outlier identification  
- pattern recognition  

EDA is used across science, engineering, finance, and data science to improve accuracy, reduce risk, and avoid decision-making errors. Anscombe’s Quartet shows why visualization is mandatory in any serious analysis.

---

# Data Source & Loading

The dataset used here is Seaborn’s built-in `anscombe` dataset. To reproduce the figures and files, run the provided Python script `scripts/generate_anscombe_assets.py` (instructions below). That script will create the following files in `/assets/`:

- `anscombe.csv`  
- `anscombe_scatter.png` (individual dataset scatter plots with regression lines)  
- `anscombe_combined.png` (all datasets combined)  
- `anscombe_box.png`  
- `anscombe_violin_xy.png`  
- `residual_1.png`, `residual_2.png`, `residual_3.png`, `residual_4.png`  
- `anscombe_plotly.html` (interactive)  
- `anscombe_eda.pdf` (single PDF with figures and summary)

---

# Methods

This analysis uses common statistical measures and diagnostic tools.

### 1. Summary Statistics
- **Mean** – central value  
- **Variance** – spread of data  
- **Standard Deviation** – average distance from the mean  
- **Covariance** – direction of relationship  
- **Correlation (r)** – strength of linear relationship  
- **Regression Coefficients** – slope and intercept of best-fit line  
- **R² (Coefficient of Determination)** – how well the regression line explains the data

### 2. Visualization Techniques
- **Scatter Plots** — reveal relationships and structures  
- **Regression Lines** — show linear tendencies  
- **Residual Plots** — evaluate model accuracy and outliers  
- **Box Plots** — show distribution, median, and outliers  
- **Violin Plots** — visualize full data density  
- **Interactive Plots** — allow detailed exploration

### 3. Python Libraries Used
- **Pandas** — data manipulation  
- **NumPy** — numerical operations  
- **Matplotlib & Seaborn** — plotting  
- **Plotly** — interactive visualization  
- **Statsmodels** — regression diagnostics (optional, used in script)

---

# Summary Statistics

All datasets share nearly identical numerical summaries:

- **Mean of x:** 9.0  
- **Mean of y:** ~7.50  
- **Standard deviation (y):** ~2.03  
- **Variance (y):** ~4.12  
- **Correlation (r):** ~0.816  
- **Linear regression (approx):** similar slope/intercept across datasets

Despite these similarities, the datasets reveal drastically different shapes when plotted.

---

# Visualizations

## Scatter Plots (Individual Datasets)
These reveal the true differences in patterns — each dataset plotted with a regression line.

![Scatter Plots (I–IV)](../assets/anscombe_scatter.png)

*Figure: Scatter plots for datasets I, II, III, IV (with regression lines).*

---

## Combined Scatter Plot
All datasets shown together to emphasize that summary statistics overlap while shapes do not.

![Combined Plot](../assets/anscombe_combined.png)

*Figure: Combined view of all four datasets colored by dataset.*

---

## Box Plots
Box plots show median, IQR, and potential outliers for X and Y across datasets.

![Box Plots](../assets/anscombe_box.png)

*Figure: Box plots for X (and/or Y) across datasets.*

---

## Violin Plots
Violin plots show the distribution/density of X and Y values for each dataset.

![Violin Plots](../assets/anscombe_violin_xy.png)

*Figure: Violin plots visualizing distributions of X and Y.*

---

## Residual Plots
Residual plots show patterns that indicate poor linear fit or the presence of outliers.

![Residual Plot - Dataset I](../assets/residual_1.png)
![Residual Plot - Dataset II](../assets/residual_2.png)
![Residual Plot - Dataset III](../assets/residual_3.png)
![Residual Plot - Dataset IV](../assets/residual_4.png)

*Figure: Residual diagnostics for each dataset.*

---

## Interactive Plot (Plotly)
Use this interactive Plotly visualization to hover, zoom, and inspect individual points.

<iframe src="../assets/anscombe_plotly.html" width="100%" height="600px"></iframe>

---

# Interpretation & Analysis

## Dataset I — Linear Relationship
- Points form a near-perfect straight line.  
- Small residuals; linear regression is appropriate.  
- R² will be high and residuals roughly random.

## Dataset II — Nonlinear Curve
- Clear curved pattern; a linear model is misleading.  
- Residuals show a pattern (systematic structure), indicating a poor linear fit.  
- Summary statistics hide this curvature.

## Dataset III — Outlier Distortion
- Mostly linear except for an extreme outlier at (13, 12.74).  
- A single outlier drastically changes the regression line and metrics.  
- Demonstrates how one observation can bias estimates.

## Dataset IV — Vertical / Repeated X Values
- Many points share the same or near-same x-value, producing vertical structure.  
- Linear regression is not informative for this dataset.  
- Summary statistics cannot reveal the stacked/clustered structure.

---

# Real-World Applications

### 1. Economics & Income Inequality
Countries with a few high-income outliers may appear richer on average, hiding inequality. Visualization reveals distributional problems.

### 2. Engineering & Safety
Improper visualization or ignoring data structure can lead to catastrophic decisions (historical reference: Challenger Disaster).

### 3. Medicine & Pharmacology
Outliers may mask adverse effects of treatments. Visualization can reveal subgroups or dosage responses.

### 4. Machine Learning
Models trained without proper EDA often fail due to outliers, nonlinearity, or hidden clusters — visualization helps avoid such pitfalls.

---

# Discussion

This project demonstrates that:
- Numerical summaries alone **cannot** describe dataset structure.  
- Visualization reveals patterns and anomalies that are invisible to aggregate metrics.  
- Outliers can distort regression and correlation estimates.  
- Linear models can be misleading even when statistics look “perfect.”  
- EDA is a required step before modeling or drawing conclusions.

---

# Conclusion

Anscombe’s Quartet powerfully illustrates the need for visualization in data analysis. Summary statistics can mislead; graphs reveal the true structure.  
To extend this analysis, consider:
- polynomial regression for nonlinear patterns  
- robust regression to reduce outlier influence  
- clustering and anomaly detection  
- automated EDA pipelines for larger datasets

This assignment strengthened my understanding of both statistical summaries and visual diagnostics, and reinforced the critical role of EDA in data-driven decision-making.

---

# Tools Used

- **Python** (Pandas, NumPy)  
- **Matplotlib** & **Seaborn** (visualization)  
- **Plotly** (interactive visualization)  
- **Statsmodels** (diagnostics)  
- **Jekyll** & **GitHub Pages** (deployment)

---

# References & Further Reading

- Anscombe, F. J. (1973). Graphs in statistical analysis. *The American Statistician*.  
- Tukey, J. W. (1977). *Exploratory Data Analysis*.  
- Seaborn documentation: https://seaborn.pydata.org/  
- Plotly documentation: https://plotly.com/python/  
- Pandas documentation: https://pandas.pydata.org/

[Home](/)

---
