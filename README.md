# Predicting Diabetic Retinopathy 

## Overview
This repository contains a machine learning project aimed at predicting Diabetic Retinopathy based on various patient health metrics. The project involves data preprocessing, exploratory data analysis (EDA), and training classification models to assist in early detection.

**Author:** Yazeed Almazyad

## Dataset
The dataset consists of 20,000 patient records obtained from Kaggle. It includes 10 clinical and demographic features:
* `age`, `sugar_percentage`, `glucose_percentage`, `cholesterol_percentage`, `obesity_percentage`, `heart_rate`
* `blood_pressure` (split into `high_bp` and `low_bp` during preprocessing)
* Boolean flags: `has_eye_disease` and `has_diabetic_retinopathy` (Target Variable)

## Tech Stack
* **Language:** Python 3
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn
* **Environment:** Google Colab

## Methodology
1. **Data Preprocessing:** Handled missing values, encoded boolean categorical data using `LabelEncoder`, and engineered blood pressure features.
2. **Feature Scaling:** Applied `StandardScaler` to normalize the data for the Logistic Regression model.
3. **Modeling:** 
   * Logistic Regression
   * Decision Tree Classifier
4. **Hyperparameter Tuning:** Optimized the Decision Tree's `max_depth` to prevent overfitting.

## Key Results & Insights
* **Model Performance:** The optimized Decision Tree (with `max_depth=10`) achieved an accuracy of **75.6%**.
* **Feature Importance:** Based on the Decision Tree analysis, the most influential factors in predicting Diabetic Retinopathy are:
  1. `has_eye_disease` (Most significant indicator)
  2. `cholesterol_percentage`
  3. `glucose_percentage`

## How to Run
1. Clone this repository.
2. Ensure you have the required libraries installed.
3. Keep the `patient_data.csv` in the same directory as the Jupyter Notebook.
4. Open and run the `Predicting_Diabetic_Retinopathy.ipynb` notebook.
