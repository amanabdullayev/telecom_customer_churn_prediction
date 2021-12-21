# Project Description: Customer Churn prediction
test
The telecom operator Interconnect would like to be able to forecast their churn of clients. If it's discovered that a user is planning to leave, they will be offered promotional codes and special plan options. Interconnect's marketing team has collected some of their clientele's personal data, including information about their plans and contracts.
- **Objective: We need to predict next most likely customers who would leave soon.**

<p align="center">
<img src="data/Churn.png" width="500px">
</p>



## Interconnect's services
Interconnect mainly provides two types of services:

1. Landline communication. The telephone can be connected to several lines simultaneously.
2. Internet. The network can be set up via a telephone line (DSL, *digital subscriber line*) or through a fiber optic cable.

Some other services the company provides include:

- Internet security: antivirus software (*DeviceProtection*) and a malicious website blocker (*OnlineSecurity*)
- A dedicated technical support line (*TechSupport*)
- Cloud file storage and data backup (*OnlineBackup*)
- TV streaming (*StreamingTV*) and a movie directory (*StreamingMovies*)

The clients can choose either a monthly payment or sign a 1- or 2-year contract. They can use various payment methods and receive an electronic invoice after a transaction.

## Data Description

The data consists of files obtained from different sources:

- `contract.csv` — contract information
- `personal.csv` — the client's personal data
- `internet.csv` — information about Internet services
- `phone.csv` — information about telephone services

In each file, the column `customerID` contains a unique code assigned to each client.

The contract information is valid as of February 1, 2020.

## Overall steps:

- Loading and exploring data:
    - get familiar with tables
    - check missing values
    - data types of columns (info)
- Preprocessing (deal with the issues observed in the previous section) :
    - Column names
    - Data types of columns
    - From "Yes-No" pair to 1-0 pair
    - Feature engineering
    - Merging all tables into one

- EDA:
    - Monthyl and total charge distribution of churned and still using customers. As well as distribution of lifetime (since how many monthes a customer is using/used the operator) of churned and still-using customers.
    - Customers by different contract type and with/without internet;
    - Correlation of numerical columns
    - Counts of churned and still-using customers

- Necessary functions:
    - Model evaluation function with plots and main metrics

- Preparing data for ML:
    - Feature and target separation
    - one-hot encoded version of the data
    - label eoncoded version of the data
    - training and testing dataset preparation

- Model training and testing:
    - DummyClassifier
    - Logistic regression
    - RandomForest with hyperparameter tuning
    - LightGBM with hyperparameter tuning

- Feature importances, since each algorithm has its own way of treating features, each might have different feature importances:
    - logistic regression feature importance
    - randomforest feature importance
    - lgbm feature importance

- Summary