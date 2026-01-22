# Experiment 1: Working with Python Packages

## Overview

This experiment focuses on exploring Python libraries (Numpy, Scipy, Scikit-Learn, Matplotlib) through practical data analysis tasks.

## Objectives

1. Load and explore various datasets
2. Perform Exploratory Data Analysis (EDA)
3. Create visualizations
4. Identify ML task types for each dataset
5. Determine suitable algorithms

## Datasets

1. **Iris Dataset** - Classic classification dataset
2. **Loan Amount Prediction** - Regression task
3. **Predicting Diabetes** - Binary classification
4. **Classification of Email Spam** - Text classification
5. **Handwritten Character Recognition (MNIST)** - Multi-class image classification

## Folder Structure

```
EXP1/
├── report.tex              # LaTeX report
├── Experiment_!.pdf        # Original experiment specification
├── plots/
│   ├── png/               # PNG plots at 600 DPI
│   └── eps/               # EPS plots at 600 DPI
├── dataset/               # All datasets
└── notebooks/             # Jupyter notebooks
    └── experiment1.ipynb  # Main analysis notebook
```

## Tasks Completed

- [x] Download/load all 5 datasets
- [x] Perform EDA for each dataset
- [x] Generate visualizations (save as PNG and EPS at 600 DPI)
- [/] Fill the ML task analysis table (in report.tex)
- [/] Complete the LaTeX report
- [ ] Compile report to PDF (Requires LaTeX environment)

## Visualization Requirements

All plots have been saved in **both PNG and EPS formats at 600 DPI**:

- **Histograms**: Feature distributions
- **Box Plots**: Outlier detection
- **Correlation Heatmaps**: Feature relationships
- **Pair Plots**: Class separation analysis

## ML Task Analysis Table

The table in `report.tex` has been pre-filled with:

- Type of ML task (Classification/Regression, Binary/Multi-class)
- Feature selection techniques used
- Suitable ML algorithms

## Notes

- Use matplotlib for plotting with `dpi=600` parameter
- Save plots with descriptive names
- Keep notebook well-documented with markdown cells
- Update the LaTeX report with your findings
