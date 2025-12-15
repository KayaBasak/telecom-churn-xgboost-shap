# PREDICTING CUSTOMER CHURN IN TELECOMMUNICATIONS USING LOGISTIC REGRESSION AND XGBOOST 

Predicting customer churn using machine learning, interpretability, and real-world telecom behavioral data.

📌 Project Overview

This project focuses on predicting customer churn using a real-world dataset from an Iranian telecommunications company. The analysis includes exploratory data analysis (EDA), machine learning model development, hyperparameter tuning, and interpretability using SHAP. The goal is to identify key drivers of churn and provide actionable insights that telecom providers can use to improve customer retention.

The project was developed using Microsoft Azure Machine Learning, Python, XGBoost, and scikit-learn.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📁 Dataset Description

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

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🔍 Exploratory Data Analysis (EDA)

Key insights from the EDA:

* Churned customers tend to have lower usage, fewer distinct contacts, shorter subscription lengths, and lower customer value.

* Customers who filed complaints show significantly higher churn rates.

* Age groups show different churn patterns, with younger and older segments behaving differently.

* Boxplots and bar charts highlighted clear behavioral differences between churned and non-churned customers.

* Outliers were examined but retained, as they represent genuine real-world behavior.

EDA visuals include:

* Churn distribution

* Age group behavior

* Subscription length patterns

* Customer value boxplots

* Usage comparisons

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🤖 Machine Learning Models

Two models were implemented and compared:

1️⃣ Logistic Regression (Baseline Model)

* Simple, interpretable binary classifier

* Scaling applied to numerical features

* Achieved strong recall but lower accuracy than XGBoost

* Useful for benchmarking performance

2️⃣ XGBoost Classifier (Final Model)

* Handles nonlinear relationships and outliers effectively

* Does not require scaling

* Delivered the best overall performance

* Used as the final model for predictions and SHAP interpretability

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📈 Model Performance
	
<img width="602" height="80" alt="image" src="https://github.com/user-attachments/assets/31e351c6-0395-4e5d-b046-26af8bdf326f" />

👉 XGBoost significantly outperformed Logistic Regression, making it the chosen model for final predictions.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🧠 Model Interpretability with SHAP

To understand why the model predicts churn, SHAP (SHapley Additive exPlanations) was used.

Key findings:

* Customer complaints, subscription length, frequency of use, and seconds of use were among the strongest predictors of churn.

* SHAP summary plots revealed global feature importance.

* Individual force plots showed why specific customers are predicted to churn—for example, low usage + complaints + low value = high churn probability.

SHAP ensures the model is explainable and trustworthy.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🔮 Predicting Churn for New Customers

The project includes a prediction function that allows users to input new customer data and receive:

* Predicted churn class (0 = stay, 1 = churn)

* Probability of churn

Example output:

Predicted class: 1  
Churn probability: 0.999  

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🛠️ Technologies Used

* Python

* Microsoft Azure ML

* Jupyter Notebooks

* scikit-learn

* XGBoost

* SHAP

* Matplotlib

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📚 Project Structure
telecom-churn-xgboost-shap/

├── Churn Project Presentation.pptx

├── Churn Project.pdf

├── README.md

├── churn_project.ipynb


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📝 Conclusion

The project demonstrates that machine learning can effectively predict customer churn and identify key behavioral drivers such as low usage, short subscription length, complaints, and low customer value. XGBoost delivered the strongest performance, while SHAP provided valuable interpretability for understanding model decisions. These insights can support telecom providers in designing targeted retention strategies.

Future work may include adding temporal features, cost-sensitive learning, or deploying the model as an API.
