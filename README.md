# Week 4 Lab: Simple Linear Regression (OLS)

**QM 2023 -- Statistics II / Data Analytics | Spring 2026**

## Overview

This lab introduces **simple linear regression** (OLS) using REIT master data. You will estimate how individual REIT returns relate to market capitalization (size) and learn to interpret the regression output like a professional analyst.

## Quick Start

```bash
# 1. Install dependencies (if not already in your course venv)
pip install -r requirements.txt

# 2. Launch the notebook
jupyter notebook week4_simple_regression_lab.ipynb
```

Or open `week4_simple_regression_lab.ipynb` directly in VS Code.

## What's Inside

| File | Purpose |
|:-----|:--------|
| `week4_simple_regression_lab.ipynb` | Main lab notebook -- work through this in class |
| `data/reit_master_sample.csv` | Individual REIT observations (returns, market cap, sector) |
| `requirements.txt` | Python dependencies |

## Lab Structure

The notebook has 11 parts:

1. **Setup & Data Loading** -- import libraries, load the dataset
2. **Look at the Data First** -- scatter plot before modeling
3. **Fit Your First OLS Regression** -- `statsmodels` formula API
4. **Read the Regression Output** -- what each column means
5. **Extract Key Results** -- pull out coefficients, p-values, R-squared
6. **Write a Proper Interpretation** -- wrong way vs. right way
7. **Visualize the Regression** -- scatter plot with fitted line
8. **Understand Residuals** -- what OLS minimizes
9. **Confidence Interval Visualization** -- does the CI contain zero?
10. **Omitted Variables** -- what are we missing?
11. **Practice Exercises** -- try log(mcap), by sector, etc.

## Dataset

REIT master panel (individual REIT-month observations):

- `permno` -- Unique REIT identifier
- `ym` -- Year-month (e.g., 202101)
- `ret` -- Monthly return (decimal, e.g., 0.05 = 5%)
- `mcap` -- Market capitalization in millions of dollars
- `sector` -- Property sector (Retail, Office, Industrial, etc.)
- `price` -- Stock price

All returns are in decimal form (0.01 = 1 percentage point).

## Connection to Assignment 04

This lab prepares you for **Assignment 04** (due Friday at 11:59 PM). The assignment asks you to:

1. Estimate `ret ~ mcap` in a Python script
2. Create a scatter plot with the regression line
3. Write an interpretation memo
4. Complete the AI Audit Appendix

Everything you learn in this lab applies directly to the assignment.
