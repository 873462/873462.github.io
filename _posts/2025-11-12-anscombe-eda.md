---
layout: default
title: "Anscombe’s Quartet – Exploratory Data Analysis (EDA)"
author: Ivan Johnson
date: 2025-10-08
---

[Home](/) | [About](/about)

# Anscombe’s Quartet – Exploratory Data Analysis (EDA)
*By Ivan Johnson — October 9, 2025*

---

## 📘 Introduction

This project explores **Anscombe’s Quartet**, a famous dataset created by statistician *Francis Anscombe* in 1973 to show the importance of **data visualization**.

Although the four datasets (I, II, III, IV) share nearly identical summary statistics — same mean, variance, correlation, and regression line — their scatter plots reveal **dramatically different patterns**.

> “Statistics are not enough — always visualize your data.”

---

## ⚙️ 1. Loading Anscombe’s Quartet

We used Seaborn’s built-in Anscombe dataset:

- 44 total points  
- 4 groups: *I, II, III, IV*  
- Each subset contains 11 (x, y) pairs  

All four datasets have nearly identical statistical properties, which is what makes this dataset so interesting.

---

## 📊 2. Summary Statistics

Below is a summary of each dataset (mean, std, variance, min, and max):

### **Dataset I**
- Mean (x, y): **9.0**, **7.50**
- Std (y): 2.03  
- Max y: 10.84  

### **Dataset II**
- Mean (x, y): **9.0**, **7.50**
- Std (y): 2.03  
- Max y: 9.26  

### **Dataset III**
- Mean (x, y): **9.0**, **7.50**
- Std (y): 2.03  
- Max y: 12.74  

### **Dataset IV**
- Mean (x, y): **9.0**, **7.50**
- Std (y): 2.03  
- Max y: 12.50  

Even though these numbers match across datasets, their graphs do **not**.

---

## 📈 3. Scatter Plots (Matplotlib)

Each dataset was plotted with a regression line:

**I** — nearly perfect linear  
**II** — clear curve  
**III** — strong outlier  
**IV** — vertical line shape  

![Anscombe Scatter](/assets/images/anscombe_scatter.png)

![Combined Plot](/assets/images/anscombe_combined.png)

![Violin Plots](/assets/images/anscombe_violin_xy.png)

<iframe src="../assets/anscombe_plotly.html" width="100%" height="600px"></iframe>

[Home](/)
