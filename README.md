# Telecom Customer Churn Prediction

## Overview

Customer churn is a critical problem for the telecom industry, especially in a competitive market. This project, developed for No-Churn Telecom, aims to address the challenge of retaining customers by leveraging machine learning. The project focuses on understanding churn-driving factors, creating risk scores, predicting churn, and providing actionable insights to improve customer retention.

## Business Case

No-Churn Telecom is facing a churn rate exceeding 10% despite initiatives like reduced tariffs and promotional offers. The goal of this project is to assist No-Churn Telecom by:

1. Understanding variables influencing customer churn.


2. Creating churn risk scores for targeted retention campaigns.


3. Introducing a predictive "CHURN-FLAG" variable for personalized customer offers.


4. Identifying high-risk customers for focused customer care efforts.




---

## Dataset

Rows: 4,617

Columns: 21

Target Variable: Churn (Yes/No)


## Key Features

Customer Service Calls: Number of calls to customer service.

International Plan: Subscription status for an international calling plan.

Day Charge, Eve Charge, Night Charge, Intl Charge: Call charges during different times.

Account Length: Number of days a customer has been with the company.



---

## Data Preprocessing

**1. Dropped Irrelevant Column: Phone (unique identifier).**


**2. Handled Categorical Variables:**

Used Label Encoding for Churn.

Applied Label Encoder for other categorical columns.



**3. Feature Selection:**

Removed highly correlated features (VMail Message, Day Mins, Eve Mins, Night Mins, Intl Mins) based on a heatmap analysis.



**4. Scaling: Applied scaling separately to train and test datasets to avoid data leakage.**


**5. Data Balancing: Used SMOTE to address class imbalance in the target variable.**




---

## Machine Learning Models

The following models were implemented and evaluated:

1. Logistic Regression


2. Support Vector Machine (SVM)


3. Decision Tree (DT)


4. Random Forest (RF)


5. XGBoost


6. K-Nearest Neighbors (KNN)


7. Naive Bayes


8. Artificial Neural Networks (ANN)


9. LightGBM




---

## Results

Best Model for Accuracy: ANN with an accuracy of 89.1%.

Best Model for Recall: LightGBM with a recall of 93.6%.

Best Model for Balance (Precision/Recall): SVM with:

Accuracy: 89.0%

Precision: 58.2%

Recall: 70.0%

ROC-AUC: 89.8%




---

## Project Goals

### Goal 1: Understanding Variables Influencing Customer Churn

Used Logistic Regression and permutation importance to identify key features like:

Customer Service Calls

International Plan

Day Charge


Insights enable targeted efforts to address high-churn factors.


### Goal 2: Creating Churn Risk Scores

Used SVM (highest ROC-AUC of 89.8%) to create risk scores, enabling data-driven retention campaigns.


### Goal 3: Introducing CHURN-FLAG Variable

Applied LightGBM for high recall, flagging churners with 93.6% recall.

Correctly identified 147 out of 157 churners, minimizing missed cases.


### Goal 4: Identifying CHURN-FLAG Customers for Attention

**1. Prediction: LightGBM flagged high-risk customers.**


**2. Customer Segmentation:**

High Priority: Multiple unresolved tickets or frequent complaints.

Medium Priority: Moderate engagement issues.

Low Priority: Minor concerns.



**3. Automating Ticket Categorization: Designed a system to categorize customer tickets as high, normal, or low priority.**


**4. Actionable Insights: Dashboard visualization showed:**

Low Priority: 651 customers

High Priority: 105 customers

Medium Priority: 86 customers




---

## Conclusion

This project successfully utilized machine learning to address No-Churn Telecom's business challenges. By providing actionable insights, risk scores, and predictive churn flags, the solutions empower the company to enhance customer retention strategies and maintain a competitive edge.
