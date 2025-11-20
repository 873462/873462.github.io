---
layout: default
title: "Linear Regression"
excerpt: "A blog about understanding linear regression"
---
# Linear Regression Tutorial — Blog Post

This post is based on the Jupyter notebook **`linear-regression-tutorial.ipynb`** from the following GitHub commit:

**Notebook Link:**  
[Notebook Link](/assets/images/TER_improved.ipynb)

All cells in the notebook were run successfully, and this post summarizes what the notebook does and answers the questions included in it.

---

## Introduction

This tutorial explores **simple linear regression** using datasets from **Anscombe’s Quartet**. The goal is to:

- Import and inspect multiple datasets  
- Compute regression statistics  
- Visualize the fits  
- Understand why visualization is essential, even when summary statistics look identical  

Anscombe’s Quartet is a perfect demonstration of why you should never rely only on summary statistics in data analysis.

---

## Section Overview

### 1. **Importing Data**

The notebook loads four CSV files:

- `anscombe_I.csv`
- `anscombe_II.csv`
- `anscombe_III.csv`
- `anscombe_IV.csv`

Each dataset contains paired x–y values intended to show very different patterns despite appearing statistically identical.

### 2. **Summary Statistics and Regression**

For each dataset, the notebook computes:

- Mean of x  
- Mean of y  
- Variance of x  
- Variance of y  
- Correlation  
- Linear regression slope  
- Linear regression intercept  

The surprising part:  
**All four datasets share nearly identical values for every one of these statistics.**

### 3. **Visualization**

Scatter plots + fitted regression lines are produced for each dataset.

Even though the regression line is almost the same, the scatter plots are **completely different**:

- One looks perfectly linear  
- One contains a single extreme outlier  
- One is clearly non-linear  
- One has nearly constant x-values except for a single outlier  

---

# Answers to the Notebook Questions

Below are the full answers to the questions included in the notebook.

---

## **Q1. Compare the summary statistics across all four datasets. What do you notice?**

All four datasets have:

- Very similar **mean of x**
- Very similar **mean of y**
- Very similar **variance of x**
- Very similar **variance of y**
- Nearly identical **regression slopes**
- Nearly identical **regression intercepts**

**Observation:**  
Even though the datasets look completely different when plotted, the summary numbers are almost exactly the same.  
This is the whole point of Anscombe’s Quartet:  
> *Summary statistics alone can be misleading.*

---

## **Q2. What differences appear in the plots that do not show up in the summary statistics?**

Once visualized:

- **Dataset I**: A clean linear relationship  
- **Dataset II**: A slight curve — not actually linear  
- **Dataset III**: A single outlier forces the regression line  
- **Dataset IV**: Almost all points stack vertically except one outlier that completely dictates the slope  

These differences are **invisible** in the summary statistics, but **obvious** in the plots.

---

## **Q3. What lessons can we learn about linear regression and summary statistics?**

### Main Lessons:

- **Always visualize your data.**  
  Summary statistics cannot reveal shape, outliers, subgroups, or non-linearity.

- **Regression coefficients do not guarantee a good model.**  
  A dataset may appear to fit a line numerically but be inappropriate visually.

- **Outliers matter.**  
  One single point can drastically change a regression line.

- **Data context is essential.**  
  Numbers alone do not tell the whole story.

### Final takeaway:
> *Statistics summarize; visualizations reveal.*

---

## Final Thoughts

Working through this notebook reinforced why linear regression requires more than just looking at slope and intercept values. Anscombe’s Quartet is a brilliant reminder that:

- Data can look the same numerically,  
- But behave completely differently visually.

Understanding this is critical for anyone working with real-world data.

---

### 📎 Notebook Link (again)

https://github.com/mrandrewandrade/TER/blob/f33c0606f1b182e7d84554032ba7f8e46d3ba845/linear-regression-tutorial.ipynb
