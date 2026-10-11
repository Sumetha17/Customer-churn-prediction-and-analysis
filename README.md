# Customer Churn Prediction and Analysis Using Machine Learning

## Project Overview

This project analyzes customer churn using the Telco Customer Churn dataset. The objective is to understand customer churn patterns and build machine learning classification models that predict whether a customer is likely to leave the company.

The project uses Python for data cleaning, exploratory data analysis (EDA), visualization, model training, and evaluation. Different classification approaches are compared to understand how well they identify customers who churn.

## Objectives

* Clean and prepare customer data for analysis.
* Explore customer characteristics and churn patterns.
* Visualize churn distribution and relationships between customer attributes and churn.
* Build and evaluate machine learning classification models.
* Compare baseline models with class-balanced and tuned Logistic Regression models.
* Examine different classification thresholds to improve churn detection.

## Tools and Technologies

* Python
* Google Colab / Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* GitHub

## Dataset

The project uses the Telco Customer Churn dataset.

Important features used in the modeling section include:

* `tenure` — the number of months a customer has stayed with the company.
* `MonthlyCharges` — the customer's monthly charges.
* `TotalCharges` — the customer's total charges.
* `Contract` — the customer's contract type.
* `PaymentMethod` — the customer's payment method.
* `Churn` — whether the customer left the company.

The target variable `Churn` is converted into numeric labels: `No = 0` and `Yes = 1`.

## Project Workflow

### 1. Data Cleaning

* Inspected the dataset and data types.
* Checked missing values and duplicate records.
* Converted `TotalCharges` into a numeric column.
* Handled missing `TotalCharges` values using median imputation.

### 2. Exploratory Data Analysis

* Examined numerical summaries and categorical distributions.
* Calculated the overall churn rate.
* Compared churn across contract types, internet services, and payment methods.
* Created visualizations to explore churn distribution, tenure, monthly charges, and payment methods.

### 3. Feature Engineering and Preparation

* Selected features for machine learning.
* Converted the target variable into numeric values.
* Applied one-hot encoding to categorical predictors.
* Split the dataset into training and testing sets using an 80:20 split.

### 4. Machine Learning Models

The notebook explores:

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier
* Class-balanced Logistic Regression
* Class-balanced Random Forest
* Hyperparameter tuning for Logistic Regression
* Classification threshold tuning

### 5. Model Evaluation

Models are evaluated using accuracy, precision, recall, F1-score, classification reports, and a confusion matrix.

For churn prediction, recall and F1-score for the churn class are important because identifying customers at risk of leaving can help a company plan customer-retention activities.

## Key Findings and Model Comparison

The current notebook records the following Logistic Regression results:

| Model configuration                              | Accuracy | Churn recall | Churn F1-score |
| ------------------------------------------------ | -------: | -----------: | -------------: |
| Original Logistic Regression                     |      78% |          48% |            54% |
| Class-balanced Logistic Regression               |      73% |          79% |            61% |
| Tuned Logistic Regression                        |      73% |          79% |            61% |
| Balanced Logistic Regression with threshold 0.55 |      75% |          76% |            62% |

These results illustrate the trade-off between overall accuracy and identifying customers who churn. The threshold 0.55 configuration is the current preferred configuration recorded in the notebook, based on its churn recall and F1-score. The final model choice should be validated carefully before deployment.

## Skills Demonstrated

* Data cleaning and preprocessing
* Exploratory data analysis
* Data visualization
* Feature encoding
* Train-test splitting
* Classification model development
* Model evaluation
* Class imbalance handling
* Hyperparameter tuning
* Classification threshold analysis

## Conclusion

This project demonstrates an end-to-end customer churn analysis workflow using Python and machine learning. It compares multiple classification approaches and explores techniques to improve churn detection. The analysis provides a foundation for identifying customers who may be at risk of leaving and supporting data-driven retention strategies.
