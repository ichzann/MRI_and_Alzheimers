# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

MRI-based Alzheimer's disease classification project using the OASIS Longitudinal MRI dataset from Kaggle. The entire workflow lives in a single Jupyter notebook (`data_prep.ipynb`).

## Data

- Source: `kagglehub.load_dataset("kaggle/oasis-longitudinal-mri", "oasis_longitudinal.csv")` via kagglehub
- Dataset: OASIS Longitudinal MRI — demographic and clinical features (not raw images)

## Pipeline (in `data_prep.ipynb`)

1. **Data loading & prep** — fetch via kagglehub, clean, encode, scale with `StandardScaler` (saved as `alz_scaler.save` via joblib)
2. **PCA & visualization** — dimensionality reduction, matplotlib/seaborn plots
3. **Random Forest** — classification with `RandomizedSearchCV`, confusion matrix, feature importance, graphviz tree export
4. **Logistic Regression** — baseline comparison
5. **LSTM (Keras)** — sequential model (`pca_trajectory_model.keras`) using TensorFlow/Keras

## Key Artifacts

- `alz_scaler.save` — fitted StandardScaler (joblib)
- `pca_trajectory_model.keras` — trained LSTM model

## Dependencies

Key packages: kagglehub, pandas, numpy, scikit-learn, matplotlib, seaborn, graphviz, tensorflow, joblib
