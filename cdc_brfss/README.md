# CDC Diabetes Health Indicators — Prediction Model

Main model for this repository. Uses the CDC BRFSS dataset (253,680 rows, 21 features, no missing values).

## Highlights

| Property | Value |
|---|---:|
| Rows | 253,680 |
| Best test accuracy | **86%** |
| Best test ROC-AUC | **0.83** |
| Best model | HistGradientBoostingClassifier |

## How to run

1. Make sure `diabetes_cdc.csv` is in this folder.
2. Open `Diabetes_CDC_BRFSS.ipynb` in Jupyter and run all cells.

## Important: this dataset is class-imbalanced

86% of patients are non-diabetic, so a model that always says "not diabetic" already gets 86% accuracy. Always report **ROC-AUC alongside accuracy**.

## Top features the model relies on

1. General Health (GenHlth)
2. BMI
3. High Blood Pressure
4. Age
5. High Cholesterol

These are exactly the standard clinical risk factors — confirming the model is learning real medical signal.
