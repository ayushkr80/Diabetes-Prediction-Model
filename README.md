# 🩺 Diabetes Prediction Model

This repository contains **two diabetes prediction projects**.

## 📁 Structure

- **`cdc_brfss/`** — Main project. CDC BRFSS dataset (253,680 rows). **86% accuracy, 0.83 ROC-AUC.**
- **`pima/`** — Original Pima Indians project. Smaller dataset (768 rows), used for learning.

## 🎯 Which one should I look at?

Look at **`cdc_brfss/`** for the actual production-quality model. Look at **`pima/`** for the original learning project.

## 🧠 Models used

| Project | Best model | Test accuracy | Test ROC-AUC |
|---|---|---:|---:|
| `pima/` | Linear SVM | 77 % | — |
| `cdc_brfss/` | HistGradientBoosting | **86 %** | **0.83** |

## ⚠️ Why two projects?

The Pima Indians dataset has only 768 rows and ~49% of its `Insulin` values are missing-disguised-as-zero, so the realistic accuracy ceiling there is ~78%. The CDC BRFSS dataset is 330× larger and clean.

## → Quick start (CDC project)

```bash
cd cdc_brfss
pip install pandas numpy scikit-learn matplotlib joblib jupyter
jupyter notebook Diabetes_CDC_BRFSS.ipynb
