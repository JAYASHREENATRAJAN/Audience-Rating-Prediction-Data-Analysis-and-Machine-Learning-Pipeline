# Audience-Rating-Prediction-Data-Analysis-and-Machine-Learning-Pipeline
This script demonstrates a complete workflow for predicting **audience ratings** using **data analysis**, **visualization**, and  machine learning  techniques. The goal is to extract insights, preprocess data, and build a predictive model to determine audience ratings based on various features.
# Comprehensive Model Evaluation and Performance Overview

## **Project Overview:**
In this project, multiple machine learning models were tested and evaluated for predicting audience ratings. The goal was to find the best model that could provide the most accurate predictions. Throughout the process, various techniques were applied, such as hyperparameter tuning, cross-validation, and data transformations. Below is the step-by-step demonstration of the process, detailing the models used, methods applied, and the final performance achieved.

---

## **Step 1: Data Loading and Preprocessing**
- **Data Source:** The dataset used for this project contains audience ratings along with features that can influence those ratings.
- **Initial Data Exploration:** The data was explored for missing values, outliers, and skewness.
- **Log Transformation:** Applied a log transformation to handle positive skewness, improving data distribution for model fitting.

---

## **Step 2: Model Selection**
We tested several popular machine learning models and evaluated their performance. The models used include:

1. **Linear Regression**
2. **Random Forest**
3. **XGBoost**
4. **SVM (Support Vector Machine)**
5. **Gradient Boosting**
6. **Neural Network**
7. **Stacked Ensembling**

Each model was tested with default hyperparameters initially, followed by tuning and optimization techniques.

---

## **Step 3: Model Tuning and Cross-Validation**
To ensure the best performance, each model underwent hyperparameter tuning using various methods:

1. **Randomized Search** and **Grid Search** were applied for models like Random Forest and XGBoost.
2. **Optuna** was used to tune hyperparameters, especially for Random Forest, XGBoost, and SVM.
3. **Cross-Validation:** Performed 5-fold cross-validation for model evaluation to ensure robustness of performance.

---

## **Step 4: Model Evaluation Metrics**
The models were evaluated using the following metrics:
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **R² Score**
- **Mean Absolute Error (MAE)**
- **RMSLE (Root Mean Squared Logarithmic Error)**

---

## **Step 5: Results and Insights**

### **Key Model Results:**

- **Random Forest (after Hyperparameter Tuning):**
  - **MSE:** 185.82
  - **R² Score:** 0.5445
  - **Best Hyperparameters:** 
    - `n_estimators: 500`
    - `max_depth: 48`
    - `min_samples_leaf: 5`
    - `bootstrap: True`

- **XGBoost (after Hyperparameter Tuning):**
  - **MSE:** 181.30
  - **R² Score:** 0.5556
  - **Best Hyperparameters:** 
    - `n_estimators: 1000`
    - `max_depth: 6`
    - `learning_rate: 0.199`
    - `subsample: 0.511`

- **Support Vector Machine (SVM):**
  - **MSE:** 391.73
  - **R² Score:** 0.0397 (Very low performance)

- **Gradient Boosting:**
  - **MSE:** 184.97
  - **R² Score:** 0.5466

- **Neural Network:**
  - **MSE:** 323.33
  - **R² Score:** 0.2074

---

### **Best Model Performance:**
The **XGBoost model** emerged as the top performer with the highest **R² Score** of **0.5556**, followed closely by **Gradient Boosting** with a score of **0.5466**. 

- **Best R² Score Achieved:** **0.5556** (XGBoost after hyperparameter tuning).
- **Best MSE Achieved:** **181.30** (XGBoost after hyperparameter tuning).

These results show that **XGBoost** is the best-performing model for this dataset, making it the most suitable choice for predicting audience ratings.

---

## **Step 6: Stacked Ensemble Performance**
After testing individual models, a **Stacked Ensemble** of the best-performing models was created:

- **Stacked Model Accuracy:** 
  - **MSE:** 175.53
  - **R² Score:** 0.588
  - **Best Model in Ensemble:** XGBoost

---

## **Conclusion:**
- **Best Model:** **XGBoost** after hyperparameter tuning.
- **Achieved Best R² Score:** **0.5556**, which is the highest among all models tested.
- The stacked ensemble model further improved the performance, achieving the lowest **MSE** of **175.53**.

This detailed analysis and performance evaluation process involved various techniques and models, culminating in the best-performing **XGBoost** model, demonstrating strong predictive power for audience ratings.

---

## **Technical Insights:**
- **Hyperparameter Optimization:** Successfully used **Optuna** and **Randomized Search** for tuning, leading to improved model performance.
- **Ensemble Techniques:** Implemented **stacking** of models, improving overall accuracy.
- **Advanced Evaluation:** Used cross-validation, log transformations, and various performance metrics for in-depth model evaluation.
- **Strong Statistical Understanding:** Demonstrated knowledge of regression metrics, overfitting/underfitting analysis, and proper model validation.


