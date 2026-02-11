# Week 4 Lab: Simple Linear Regression (OLS)

**QM 2023 -- Statistics II / Data Analytics | Spring 2026**

## Overview

This lab introduces **simple linear regression** (OLS) using REIT data. You will estimate how individual REIT annual returns relate to **dividend yield** and learn to interpret the regression output like a professional analyst. A secondary analysis explores **market cap** (size) as an alternative predictor.

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
| `data/REIT_sample_annual_2004_2024.csv` | Individual REIT observations (annual returns, dividend yield, market cap) |
| `requirements.txt` | Python dependencies |

## Lab Structure

The notebook is organized as follows:

1. **Setup & Data Loading** -- import libraries, load the dataset
2. **Look at the Data First** -- scatter plot of returns vs. dividend yield
3. **Winsorization** -- cap extreme dividend yields at 1st and 99th percentiles (address outliers before regression)
4. **Fit Your First OLS Regression** -- `ret ~ div_yield` using `statsmodels`
5. **Read the Regression Output** -- what each column means
6. **Extract Key Results** -- pull out coefficients, p-values, R-squared
7. **Write a Proper Interpretation** -- wrong way vs. right way
8. **Visualize the Regression** -- scatter plot with fitted line
9. **Understand Residuals** -- what OLS minimizes, residual diagnostics
10. **Confidence Interval Visualization** -- does the CI contain zero?
11. **Thinking About What We're Missing** -- omitted variables  
12. **Part 10a: Secondary Analysis** -- compare with `ret ~ mcap`
13. **Practice Exercises** -- try log(mcap), by year, interpretation

## Dataset

REIT sample, annual observations (2004--2024):

- `permno` -- Unique REIT identifier
- `year` -- Calendar year
- `ticker` -- Stock ticker symbol
- `ret` -- Annual (12-month) return (decimal, e.g., 0.05 = 5%)
- `div_yield` -- Dividend yield (12-month dividends / market equity, e.g., 0.05 = 5%)
- `mcap` -- Market capitalization in millions of dollars

All returns and yields are in decimal form (0.01 = 1 percentage point). Dividend yield is winsorized at the 1st and 99th percentiles before the main regression.

## Connection to Assignment 04

This lab prepares you for **Assignment 04** (due Friday at 11:59 PM). The assignment asks you to:

1. Estimate `ret ~ div_yield` in a Python script
2. Create a scatter plot with the regression line
3. Write an interpretation memo
4. Complete the AI Audit Appendix

Everything you learn in this lab applies directly to the assignment.
