# Experiment 2: Binary Classification (Naive Bayes & KNN)

## Overview

Implementation of Naive Bayes (Gaussian, Multinomial, Bernoulli) and K-Nearest Neighbors (KNN) for binary classification on the Spambase dataset. Includes hyperparameter tuning and performance analysis.

**Dataset Note:** Using the provided local `dataset/spambase/spambase_csv.csv`.

## Objectives

- Implement Naive Bayes variants and KNN.
- Tune KNN hyperparameters ($k$, search algorithm).
- Analyze Bias-Variance tradeoff.
- Evaluate using Accuracy, Precision, Recall, F1, ROC-AUC.

## Dataset

- **Name**: Spambase Dataset (from OpenML/UCI)
- **Task**: Binary Classification (Spam vs Non-Spam)
- **Features**: 57 continuous attributes.

## Key Visualizations (`plots/png/`)

| Plot                   | Description                    |
| :--------------------- | :----------------------------- |
| `class_distribution`   | Balance of the target variable |
| `feature_distribution` | Histograms of select features  |
| `confusion_matrices`   | Performance of all 4 models    |
| `roc_curves`           | ROC Comparison (AUC scores)    |
| `knn_accuracy_vs_k`    | Effect of $k$ on CV accuracy   |
| `learning_curve_nb`    | Bias-Variance analysis for NB  |
| `learning_curve_knn`   | Bias-Variance analysis for KNN |

## How to Run

1.  **Activate Environment**: `..\venv\Scripts\Activate.ps1`
2.  **Run Notebook**: `jupyter notebook notebooks/experiment2.ipynb`
3.  **Compile Report**: Update `report.tex` with your details and run `pdflatex report.tex`.

## Results Summary

- **Naive Bayes**: Fast training, good baseline. Gaussian NB suitable for continuous features.
- **KNN**: Sensitive to $k$. Tuning required. Slower inference time than NB.
- **Tuning**: Grid Search identified optimal $k$. KDTree/BallTree optimized search speed.
