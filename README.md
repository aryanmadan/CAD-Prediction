# A Comparative Study of Different Machine Learning Algorithms for the Prediction of Coronary Artery Disease: A Classification Approach

## Overview
This project evaluates the performance of various machine learning algorithms to predict the presence of Coronary Artery Disease (CAD) based on clinical and demographic features. The study focuses on model selection, training, cross-validation, and comparative analysis to identify the best-performing model for CAD prediction.

---

## Table of Contents
1. [Introduction](#introduction)
    - [Goals](#goals)
    - [Background Research](#background-research)
    - [Features & Predictor](#features--predictor)
2. [Data Wrangling](#data-wrangling)
3. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
4. [Model Training & Testing](#model-training--testing)
5. [Results](#results)
    - [Model Comparison Table](#model-comparison-table)
6. [Conclusion & Further Research](#conclusion--further-research)

---

## 1. Introduction

### 1.1 Goals
1. Can machine learning algorithms accurately predict the presence of CAD in patients?
2. Which machine learning algorithm performs the best for CAD prediction?
3. Can ensemble models improve prediction performance by combining diverse algorithms?

### 1.2 Background Research
Coronary Artery Disease is a leading cause of death worldwide, making its early detection critical. Machine learning provides an opportunity to improve diagnostic accuracy through efficient and non-invasive predictions. This study leverages a dataset from Kaggle containing clinical and diagnostic data from 297 patients.

### 1.3 Features & Predictor
The target variable (CAD presence) is predicted using 13 features:
- **Age**
- **Sex**: Binary (1 = Male, 0 = Female)
- **Chest Pain Type** (cp): Categorical (0–3)
- **Resting Blood Pressure** (trestbps): Numerical
- **Serum Cholesterol** (chol): Numerical
- **Fasting Blood Sugar** (fbs): Binary
- **Resting ECG Results** (restecg): Ordinal
- **Max Heart Rate Achieved** (thalach): Numerical
- **Exercise-Induced Angina** (exang): Binary
- **ST Depression** (oldpeak): Numerical
- **Slope of Peak Exercise ST Segment** (slope): Ordinal
- **Number of Major Vessels Colored by Fluoroscopy** (ca): Ordinal
- **Thalassemia** (thal): Ordinal

---

## 2. Data Wrangling
- The dataset was cleaned to handle missing and duplicate values.
- All rows and columns were found complete, with no missing or duplicated data.
- A balanced distribution of the target variable was observed.

---

## 3. Exploratory Data Analysis (EDA)
EDA focused on identifying correlations between features and the target variable:
1. **Correlation Matrix**: Examined feature relationships.
2. **Heatmap**: Visualized the strength of feature correlations.
3. **Histograms**: Analyzed the distribution of key features stratified by CAD presence.

---

## 4. Model Training & Testing
Six machine learning models were trained and tested:
1. Logistic Regression (LR)
2. K-Nearest Neighbors Classifier (KNC)
3. Decision Tree Classifier (DTC)
4. Random Forest Classifier (RFC)
5. Support Vector Machine (SVM)
6. Neural Network (NN)

### Training Strategy
- **Train-Test Split**: 80% training, 20% testing.
- **Cross-Validation**: 5-fold CV to evaluate model generalizability.
- Metrics used: Accuracy, Precision, Recall, F1-score, and AUC (Area Under the Curve).

---

## 5. Results

### 5.1 Model Comparison Table
| Model Name                       | Cross Validation AUC Score | Test Set AUC Score |
|----------------------------------|----------------------------|---------------------|
| Logistic Regression (LR)         | 0.923                      | 0.734               |
| K Neighbors Classifier (KNC)     | 0.715                      | 0.562               |
| Neural Network (NN)              | 0.928                      | 0.818               |
| Random Forest Classifier (RFC)   | 0.926                      | 0.734               |
| Decision Tree Classifier (DTC)   | 0.741                      | 0.721               |
| Support Vector Machine (SVM)     | 0.923                      | 0.752               |
| Ensemble Model (LR + NN + RFC)   | N/A                        | 0.828               |

The **Neural Network** performed best in cross-validation, achieving an AUC of 0.928. The **Ensemble Model** outperformed others on the test set, with an AUC of 0.828.

---

## 6. Conclusion & Further Research
- **Summary**: Machine learning algorithms demonstrate significant potential in accurately predicting CAD. Neural networks and ensemble methods yielded the best results.
- **Future Work**:
  1. Hyperparameter tuning of individual models to improve performance.
  2. Incorporating external datasets to enhance model generalizability.
  3. Developing a software tool to assist healthcare professionals with CAD risk prediction and prevention strategies.

---

## Installation & Usage
1. Clone the repository:
   ```bash
   git clone <repository-url>
