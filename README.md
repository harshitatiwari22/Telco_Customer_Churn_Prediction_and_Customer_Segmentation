# Telco Customer Churn Prediction and Customer Segmentation

## Project Overview

Customer churn is one of the major challenges faced by telecom companies because losing customers can significantly affect business growth and revenue. This project focuses on predicting customer churn using Machine Learning techniques and grouping customers into different segments based on their characteristics. The objective is to help businesses understand customer behavior and improve retention strategies.

The project utilizes **Random Forest Classification** for churn prediction and **K-Means Clustering** for customer segmentation.

---

## Dataset

**Dataset:** Telco Customer Churn Dataset

The dataset includes customer-related information such as:

* Customer Tenure
* Monthly Charges
* Total Charges
* Contract Type
* Internet Service
* Payment Method
* Technical Support
* Customer Lifetime Value (CLTV)
* Churn Status

---

## Objectives

* Explore customer behavior through data analysis.
* Build a Machine Learning model to predict customer churn.
* Determine the major factors influencing customer churn.
* Evaluate the model using different performance metrics.
* Group customers into meaningful clusters.
* Provide insights that can support customer retention decisions.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* OpenPyXL

---

## Exploratory Data Analysis (EDA)

Exploratory Data Analysis was carried out to better understand customer behavior and identify important trends within the dataset.

### Numerical Features

* Tenure Months
* Monthly Charges
* Total Charges

### Categorical Features

* Contract Type
* Internet Service
* Payment Method
* Technical Support

### Visualizations

* Histograms
* Boxplots
* Countplots
* Correlation Analysis

The analysis helped identify noticeable differences between customers who churned and those who remained with the company.

---

## Data Preprocessing

The dataset was prepared for model training using the following preprocessing steps:

* Converted **Total Charges** into numeric values.
* Treated missing values appropriately.
* Removed unnecessary columns.
* Applied One-Hot Encoding to categorical variables.
* Created feature and target datasets.
* Split the data into training and testing sets.

---

## Machine Learning Model

### Random Forest Classifier

A Random Forest Classification model was trained to classify customers based on their likelihood of churn.

The model training process included:

* Train-Test Split
* Random Forest Classification
* Class imbalance handling using **class_weight='balanced'**

---

## Model Evaluation

Model performance was assessed using the following evaluation metrics:

* Accuracy Score
* Precision Score
* Recall Score
* F1 Score
* Confusion Matrix
* Classification Report

---

## Hyperparameter Tuning

Several combinations of model parameters were tested to improve prediction performance.

The parameters included:

* Number of Trees (**n_estimators**)
* Maximum Tree Depth (**max_depth**)

The final optimized model was configured with:

* **n_estimators = 300**
* **max_depth = 10**
* **class_weight = balanced**

---

## Feature Importance Analysis

Feature importance scores were extracted from the trained Random Forest model to identify the variables that contribute the most to customer churn prediction.

Low-impact features were removed and the model was retrained to improve overall efficiency.

---

## Cross Validation

To verify the model's consistency and reliability:

* 5-Fold Cross Validation was performed.
* Accuracy and Recall scores were compared across all folds.

---

## ROC-AUC Analysis

The model was further evaluated using:

* ROC Curve
* AUC Score

These metrics helped measure the model's ability to distinguish between churned and non-churned customers.

---

## Customer Segmentation

After predicting churn, customer segmentation was performed using the **K-Means Clustering** algorithm.

### Features Used

* Tenure Months
* Monthly Charges
* Total Charges
* Churn Probability

### Steps Performed

* Data Standardization using StandardScaler
* Elbow Method for selecting the optimal number of clusters
* K-Means Clustering

---

## Customer Segments Identified

### Budget Loyal Customers

* Low spending customers
* Long-term subscribers
* Low risk of churn

### High Risk New Customers

* Customers with shorter tenure
* Higher probability of churn
* Require retention strategies

### Loyal Premium Customers

* High-value customers
* Long-term relationship with the company
* Significant contribution to business revenue

---

## Business Insights

* Customers with month-to-month contracts tend to have a higher churn rate.
* Customers paying higher monthly charges are more likely to leave the service.
* Technical support services positively influence customer retention.
* Customers with longer tenure generally show greater loyalty.
* Customer segmentation enables businesses to design more targeted retention campaigns.

---

## Future Improvements

* Implement advanced boosting models such as XGBoost and LightGBM.
* Deploy the project using Streamlit.
* Develop an interactive dashboard for business users.
* Build a real-time customer churn prediction system.
