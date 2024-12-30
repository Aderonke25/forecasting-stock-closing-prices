# Predicting Loan Default with Machine Learning

## Introduction

Lending money is a critical decision for financial institutions, as loan defaults can lead to significant financial losses, potentially resulting in liquidation. To mitigate this risk, it is essential to evaluate customer behavior and loan purposes comprehensively before approving loans. This project leverages the power of Machine Learning to simplify and enhance the decision-making process, helping financial institutions determine the likelihood of a customer defaulting on a loan.

### Objectives
1. Build a classification model to predict the likelihood of loan defaults.
2. Provide actionable insights to financial institutions about key features influencing loan decisions.
3. Deploy the final model as an API and a user-friendly web application using Streamlit.

---

## Data Dictionary

The dataset contains 14 input features and a target variable, with over 200 observations. Key features include:

- **LoanID**: Unique identifier for each observation.
- **Age**: Applicant’s age, correlating with financial stability and earning potential.
- **Income**: Annual income, indicating repayment capability.
- **LoanAmount**: Total requested loan amount, impacting repayment difficulty.
- **CreditScore**: Numeric representation of creditworthiness.
- **MonthsEmployed**: Employment duration, reflecting job stability.
- **NumCreditLines**: Number of active credit lines, indicating credit utilization and management.
- **InterestRate**: Loan interest rate, influencing repayment burden.
- **LoanTerm**: Loan duration, affecting repayment schedule and total interest.
- **DTIRatio**: Debt-to-income ratio, representing the applicant's debt burden.
- **Education**: Educational level, associated with earning potential.
- **EmploymentType**: Type of employment (e.g., full-time, part-time).
- **MaritalStatus**: Applicant’s marital status, affecting financial responsibilities.
- **HasMortgage**: Indicates whether the applicant has an existing mortgage.
- **HasDependents**: Indicates if the applicant has dependents.
- **LoanPurpose**: Reason for the loan, influencing associated risk.
- **HasCoSigner**: Presence of a co-signer, reducing default risk.
- **Default**: Target variable (0: no default, 1: default).

---

## Tools and Technologies

- **Python**
- **Flask API**
- **Heroku**
- **Render**
- **Git**
- **Streamlit**

---

## Data Exploration

Thorough data exploration was conducted to uncover patterns and relationships:
1. Visualized target variable distribution to check for class imbalance and implemented oversampling/undersampling or class weighting as needed.
2. Used pair plots and bar plots to examine numeric and categorical features, exploring relationships with the target.
3. Created correlation matrices and heatmaps to identify feature relationships.

---

## Data Preprocessing

Steps performed:
1. Identified missing values using `isna().sum()`.
2. Verified data types with `info()`.
3. Checked for duplicates using `duplicated().sum()`.
4. Detected outliers using box plots and statistical summaries.
5. Split the dataset into training and testing sets.
6. Encoded categorical features using one-hot encoding (`get_dummies`).
7. Applied MinMax scaling on numeric features, fitting the scaler only on training data.

---

## Model Development

Multiple machine learning models were evaluated for performance, complexity, and generalization:
- **Voting Classifier**
- **Bagging Classifier**
- **Adaboost Classifier**
- **Random Forest**
- **Gradient Boosting**
- **XGBoost**
- **GaussianNB**
- **BernoulliNB**
- **MultinomialNB**
- **MLP Classifier**
- **Logistic Regression**
- **TensorFlow Sequential**
- **DecisionTreeClassifier**

**Logistic Regression** was chosen for deployment due to its high interpretability, strong generalization, and recall performance.


---

## Web Development

### Flask API
A loan default prediction API was built using Flask and deployed on Render. The API accepts input data and predicts the likelihood of loan default. 

**API URL**: [Loan Default Prediction API](https://loan-default-prediction-9fvx.onrender.com/)

**Testing**: The API was tested using Postman.

### Streamlit Application
A user-friendly interface for loan default prediction was developed with Streamlit and deployed using Streamlit's deployment services.

**Screenshot of Streamlit Interface**:
