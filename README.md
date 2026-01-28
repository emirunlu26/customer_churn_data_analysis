# Customer Churn Analysis
This repository contains a data science project focused on analyzing and predicting customer churn using a comprehensive dataset of customer behaviors and subscription details.

## Project Overview
The goal of this project is to identify patterns and factors that lead to customer churn. By processing and cleaning large-scale customer data, the project prepares the foundation for building machine learning models to predict which customers are likely to cancel their services.

## Dataset
The project utilizes two primary datasets from [this Kaggle Customer Churn Dataset](https://www.kaggle.com/datasets/muhammadshahidazeem/customer-churn-dataset).

* customer_churn_dataset-training-master.csv: The primary training data.

* customer_churn_dataset-testing-master.csv: The testing data used to validate model performance.

The combined dataset consists of 505,207 records across 12 columns:

* CustomerID: Unique identifier for each customer.

* Age: Age of the customer.

* Gender: Customer gender (Male/Female).

* Tenure: Length of time as a customer.

* Usage Frequency: How often the service is used.

* Support Calls: Number of support interactions.

* Payment Delay: History of delayed payments.

* Subscription Type: Level of service (Basic, Standard, Premium).

* Contract Length: Duration of contract (Monthly, Quarterly, Annual).

* Total Spend: Total revenue from the customer.

* Last Interaction: Days since the last customer interaction.

* Churn: Target variable (1.0 = Churned, 0.0 = Retained).

## Workflow
### 1. Data Loading
The notebook begins by importing essential libraries like pandas and loading the training and testing sets into a single unified DataFrame for consistent cleaning.

### 2. Data Cleaning
To ensure data quality, the following steps are performed:

* Duplicate Removal: Checking for and removing any redundant records.

* Handling Missing Values: Identifying and managing NaN values across critical all features.

* Data Type Conversion: Applying type conversion to represent the features better.

### 3. One-Hot Encoding
Encoding categorical features so that prediction model can process these features accurately.

### 4. Training Customer Churn Prediction Model
Decision trees are ideal in this scenario as they work well with huge datasets. In addition, the algorithm is transparent as one can understand the logic behind the class selection clearly thanks to its condition-based structure. I've used GridSearchCV to apply hyperparameter tuning to get the optimal values for the maximum tree depth and criterion.

### 5. Monitoring Feature Importances
In the next step, I have sorted the features by their contribution to the classification in descending order. This way, I was able to see the features from most important to least important.

### 6. Evaluating Model Performance
To evaluate the performance of the model, I have utilized the following structures/metrics:
* Confusion Matrix
* Accuracy
* Precision
* Recall

### 6. Exploratory Data Analysis
