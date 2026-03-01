# ❤️ Heart Failure Prediction — Machine Learning Project [Medical-ML]
## 📌 Project Overview
Cardiovascular diseases (CVDs) remain the leading cause of death worldwide, accounting for approximately 32% of global deaths (WHO, 2019). Early detection plays a crucial role in prevention and risk mitigation.

This project aims to:
* Perform Exploratory Data Analysis (EDA) on a heart disease dataset
* Develop and compare multiple machine learning classification models
* Address class imbalance
* Optimize decision thresholds using Diagnostic Odds Ratio (DOR)
* Interpret the best-performing model using modern explainability techniques

The ultimate goal is to identify a model capable of accurately predicting whether a patient has heart disease based on demographic and clinical indicators.

## 📊 Dataset Description
The dataset (originally sourced from Kaggle, Heart Failure Prediction) contains:
* 918 observations
* 11 predictors
* 1 binary outcome variable (HeartDisease)

The dataset was retrieved from [here](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction?select=heart.csv). The dataset was slightly modified for didactic purposes — the positive class was randomly undersampled, introducing imbalance (~22% positives).

## 🧠 Models Evaluated
Four classification models were implemented and tuned:
* Logistic Regression
* Random Forest
* ADA Boost (Decision Tree Boosting)
* Support Vector Machine (SVM)

Each model was evaluated under four strategies:
* Regular (no imbalance correction)
* Weighted
* Undersampled (NearMiss variants)
* Oversampled (SMOTENC)

Threshold tuning was performed using Diagnostic Odds Ratio (DOR) scoring with cross-validation.

## 📏 Evaluation Metric
Primary Metric: Diagnostic Odds Ratio (DOR). DOR combines:
* Sensitivity (TPR)
* Specificity (TNR)

It is especially useful for imbalanced datasets because it is not biased by class prevalence and reflects overall discriminatory power.

## 🔍 Model Interpretation
Since most models lack direct interpretability, multiple explainability techniques were used:
* Feature Importance
* Ceteris Paribus Profiles
* Partial Dependence
* Break-down Plots
* Shapley Values

The analysis was done using **Python 3.12.8**.
