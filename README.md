# PREDICTING CUSTOMER CHURN IN TELECOMMUNICATIONS USING LOGISTIC REGRESSION AND XGBOOST 

This project applies machine learning techniques to predict customer churn in the telecommunications industry using behavioral, service-related, and demographic data. The goal is to evaluate the effectiveness of a baseline Logistic Regression model and a more advanced XGBoost classifier, and to interpret model predictions using SHAP in order to identify the key drivers of churn.

This work was completed as the final project for MIE1628: Cloud-Based Data Analytics at the University of Toronto. The project was completed individually and includes exploratory data analysis, model development, performance evaluation, interpretability analysis, and a final report documenting the methodology, results, and insights.

## 📌 Project Overview

This project focuses on predicting customer churn using a real-world dataset from an Iranian telecommunications company. The analysis includes exploratory data analysis (EDA), machine learning model development, hyperparameter tuning, and interpretability using SHAP. The goal is to identify key drivers of churn and provide actionable insights that telecom providers can use to improve customer retention.

The project was developed using Microsoft Azure Machine Learning, Python, XGBoost, and scikit-learn.

## 📖 Blog Post

For a detailed walkthrough of the analysis, modeling decisions, and interpretability results, see the accompanying Medium article:

[![Medium](https://img.shields.io/badge/Medium-Read%20Article-black?logo=medium)](https://medium.com/@bskky001/telecom-customer-churn-prediction-with-xgboost-and-shap-099bcd568e38)

## 📁 Dataset Description

Dataset: https://archive.ics.uci.edu/dataset/563/iranian+churn+dataset 

The dataset contains 3150 customers and 13 features, including:

* Call Failure

* Complains

* Subscription Length

* Charge Amount

* Seconds of Use

* Frequency of Use

* Frequency of SMS

* Distinct Called Numbers

* Age Group

* Tariff Plan

* Status

* Age

* Customer Value

* Churn (target variable: 1 = churn, 0 = non-churn)

The features represent customer demographics, usage patterns, and service experience—ideal for churn prediction modeling.

## 🔍 Exploratory Data Analysis (EDA)

### Key insights from the EDA:

* Churned customers tend to have lower usage, fewer distinct contacts, shorter subscription lengths, and lower customer value.

* Customers who filed complaints show significantly higher churn rates.

* Age groups show different churn patterns, with younger and older segments behaving differently.

* Boxplots and bar charts highlighted clear behavioral differences between churned and non-churned customers.

* Outliers were examined but retained, as they represent genuine real-world behavior.

### EDA visuals include:

* Churn distribution

<img width="471" height="393" alt="image" src="https://github.com/user-attachments/assets/c39488ba-a8b9-40aa-ba2f-d0cb56ee95e7" />

* Complaints

<img width="549" height="393" alt="image" src="https://github.com/user-attachments/assets/d3c22abf-28fc-46b3-87ca-61b4246be5ab" />

* Age group behavior

* Subscription length patterns

* Customer value boxplots

* Usage comparisons

## 🤖 Machine Learning Models

Two models were implemented and compared:

### 1️⃣ Logistic Regression (Baseline Model)

* Simple, interpretable binary classifier

* Scaling applied to numerical features

* Achieved strong recall but lower accuracy than XGBoost

* Useful for benchmarking performance

### 2️⃣ XGBoost Classifier (Final Model)

* Handles nonlinear relationships and outliers effectively

* Does not require scaling

* Delivered the best overall performance

* Used as the final model for predictions and SHAP interpretability

## 📈 Model Performance
	
<img width="602" height="80" alt="image" src="https://github.com/user-attachments/assets/31e351c6-0395-4e5d-b046-26af8bdf326f" />

👉 XGBoost significantly outperformed Logistic Regression, making it the chosen model for final predictions.

<img width="391" height="329" alt="image" src="https://github.com/user-attachments/assets/ef6e45ce-2c43-4701-bb98-be53974b9dc1" />

👉 The confusion matrix confirms that XGBoost accurately classifies both churned and non-churned customers, achieving a strong balance between precision and recall.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🧠 Model Interpretability with SHAP

To understand why the model predicts churn, SHAP (SHapley Additive exPlanations) was used.

<img width="777" height="660" alt="image" src="https://github.com/user-attachments/assets/1832009e-dc25-41d5-bb36-358c8c117c27" />

### Key findings:

* Customer complaints, subscription length, frequency of use, and seconds of use were among the strongest predictors of churn.

* SHAP summary plots revealed global feature importance.

* Individual force plots showed why specific customers are predicted to churn—for example, low usage + complaints + low value = high churn probability.

SHAP ensures the model is explainable and trustworthy.

## 🔮 Predicting Churn for New Customers

The project includes a prediction function that allows users to input new customer data and receive:

* Predicted churn class (0 = stay, 1 = churn)

* Probability of churn

### Example output:

Predicted class: 1  
Churn probability: 0.999  

## 🛠️ Technologies Used

* Python

* Microsoft Azure ML

* Jupyter Notebooks

* scikit-learn

* XGBoost

* SHAP

* Matplotlib

## 📚 Project Structure

telecom-churn-xgboost-shap/

├── Churn Project Presentation.pptx

├── Churn Project.pdf

├── README.md

├── churn_project.ipynb

## 📝 Conclusion

The project demonstrates that machine learning can effectively predict customer churn and identify key behavioral drivers such as low usage, short subscription length, complaints, and low customer value. XGBoost delivered the strongest performance, while SHAP provided valuable interpretability for understanding model decisions. These insights can support telecom providers in designing targeted retention strategies.

Future work may include adding temporal features, cost-sensitive learning, or deploying the model as an API.

## 👤 Author

Basak Kaya

MEng – Mechanical & Industrial Engineering

University of Toronto

Specialization: Data Analytics & Machine Learning
