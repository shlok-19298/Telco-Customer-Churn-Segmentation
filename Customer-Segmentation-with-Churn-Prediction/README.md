# Customer Segmentation with Churn Prediction

## Overview

This project combines **Customer Churn Prediction** and **Customer Segmentation** using the IBM Telco Customer Churn dataset. The objective is to identify customers who are likely to leave the company and simultaneously group customers into meaningful segments for targeted business strategies.

The project covers the complete machine learning workflow including:

* Exploratory Data Analysis (EDA)
* Data Cleaning and Preprocessing
* Feature Engineering
* Handling Class Imbalance using SMOTE
* Random Forest Classification
* XGBoost Classification with Hyperparameter Tuning
* Threshold Optimization
* Feature Importance Analysis
* Customer Segmentation using K-Means Clustering

---

## Dataset

Dataset: IBM Telco Customer Churn Dataset

The dataset contains customer information such as:

* Demographics
* Subscription details
* Contract information
* Monthly charges
* Total charges
* Customer tenure
* Churn status

Target Variable:

* `Churn Value`

  * 1 = Customer Churned
  * 0 = Customer Retained

---

## Project Workflow

### 1. Exploratory Data Analysis

Performed:

* Dataset structure analysis
* Missing value inspection
* Churn distribution visualization
* Monthly Charges distribution analysis
* Churn vs Monthly Charges comparison

Visualizations:

* Count Plot
* Histogram
* Box Plot

---

### 2. Data Preprocessing

Steps performed:

* Converted `Total Charges` to numeric format
* Handled missing values
* Removed irrelevant columns
* Applied One-Hot Encoding to categorical features
* Created feature matrix and target variable

---

### 3. Feature Scaling

Applied:

* StandardScaler

Purpose:

* Normalize feature values
* Improve model performance
* Prepare data for clustering algorithms

---

### 4. Handling Class Imbalance

Applied:

* SMOTE (Synthetic Minority Oversampling Technique)

Benefits:

* Balanced class distribution
* Improved churn prediction performance
* Better recall for minority class

---

### 5. Random Forest Classifier

Configuration:

* 500 Trees
* Max Depth = 8
* Balanced Class Weights

Evaluation Metrics:

* Accuracy
* Precision
* Recall
* F1 Score
* Classification Report

---

### 6. Feature Importance Analysis

Random Forest feature importance was used to identify the most influential variables affecting customer churn.

Outputs:

* Ranked feature importance table
* Top 15 feature importance visualization

---

### 7. Hyperparameter Tuning

Used:

* GridSearchCV
* 3-Fold Cross Validation

Optimized:

* Number of estimators
* Learning rate
* Tree depth

Scoring Metric:

* F1 Score

---

### 8. XGBoost Classifier

Trained using the best parameters obtained from Grid Search.

Additional Parameters:

* Subsample = 0.9
* Colsample_bytree = 0.9

Evaluation:

* Accuracy
* Precision
* Recall
* F1 Score

---

### 9. Threshold Tuning

Tested multiple classification thresholds:

* 0.35
* 0.40
* 0.45
* 0.50

Purpose:

* Improve recall and churn detection
* Balance precision and recall according to business requirements

---

### 10. Model Comparison

Compared:

| Model         | Evaluation     |
| ------------- | -------------- |
| Random Forest | Baseline Model |
| XGBoost       | Tuned Model    |

Comparison based on:

* Accuracy
* Classification Performance

---

## Customer Segmentation

### Elbow Method

Used the Elbow Method to determine the optimal number of customer clusters.

Features used:

* Tenure Months
* Monthly Charges
* Total Charges

---

### K-Means Clustering

Final Configuration:

* Number of Clusters = 3

Generated Segments:

* Premium Customers
* Stable Customers
* High-Risk Customers

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* Imbalanced-Learn

---

## Results

### Churn Prediction

Successfully built multiple machine learning models capable of predicting customer churn using customer behavioral and subscription data.

### Customer Segmentation

Identified distinct customer groups that can be used for:

* Retention Campaigns
* Personalized Marketing
* Revenue Optimization
* Customer Lifetime Value Strategies

---

## Kaggle Notebook

View the complete implementation:

https://www.kaggle.com/code/shlok192980707/customer-segmentation-with-churn-prediction

---

## Future Improvements

* Deploy model using Flask or FastAPI
* Build interactive dashboard using Streamlit
* Experiment with LightGBM and CatBoost
* Perform advanced feature engineering
* Create automated churn monitoring pipeline

---

## Author

Shlok Kumar

Machine Learning | Data Analytics | AI Enthusiast