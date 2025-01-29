# Credit_Card_Default
Predict Credit Card Default and allow to understand feature importance

# Credit Card Default Risk Prediction 📊💳

## Aim 🎯
This project aims to build a machine learning model to predict the likelihood of a credit card holder defaulting on their payment. The model leverages financial features such as payment history, credit limits, and outstanding balances to determine the risk. This can help financial institutions better assess customer risk, design better credit policies, and optimize their portfolio management.

## Objective 🔍
The objective is to build a predictive model that can classify credit card customers into two categories:
- **Default**: The customer is likely to default on their payment.
- **Non-default**: The customer is unlikely to default.

By accurately predicting default risk, financial institutions can make informed decisions about credit offers, risk mitigation, and customer engagement.

## Data 
Data is sourced directly from Kaggle: https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset

## Exploratory Data Analysis (EDA) 🔎

1. **Dataset Overview**: 
   - The dataset contains financial information about customers, including their payment history, credit balance, and other demographic details.
   
2. **Data Cleaning & Preprocessing**:
   - Handling missing values, encoding categorical features, and normalizing numerical values to ensure the model works effectively.

3. **Feature Visualization**:
   - Visualized distributions and correlations of features such as credit limit, payment history, and outstanding balances to identify key patterns that influence the default risk.

4. **Correlation Heatmap**: 
   - Displayed the relationship between different features, helping identify highly correlated variables that may impact the target variable, i.e., the risk of default.

## Model Building 🛠️

### Chosen Model: **RandomForestClassifier** 🌳

- **Why Random Forest?** 
   - Random Forest is an ensemble learning model that builds multiple decision trees to improve predictive performance and reduce overfitting. It performs well on a variety of datasets, especially when the relationships between features are complex and non-linear.
   - **Highest Accuracy**: Among several models tested (e.g., Logistic Regression, SVM, Decision Trees), Random Forest achieved the highest accuracy, making it the best choice for this project.

### Key Steps:
1. **Model Training**:
   - Split the data into training and testing sets (80/20 split).
   - Train the RandomForest model on the training set.

2. **Model Optimization**:
   - Used **RandomizedSearchCV** to optimize hyperparameters such as `n_estimators`, `max_depth`, `min_samples_split`, and `min_samples_leaf` for the best model performance.
   - Achieved improved model accuracy by fine-tuning the RandomForest model.

### Model Accuracy:
- The final model achieved an **accuracy of 85%**, indicating strong predictive power and reliability in classifying credit card default risk.

## Feature Importance 🔑

The RandomForest model provided the following feature importance:

| **Feature**         | **Importance** |
|---------------------|----------------|
| **PAY_SEPT**        | 0.258593       |
| **PAY_AUG**         | 0.127199       |
| **PAY_JUL**         | 0.075031       |
| **PAY_JUN**         | 0.056552       |
| **PAY_MAY**         | 0.044792       |
| **PAY_AMT_SEPT**    | 0.037257       |
| **LIMIT_BAL**       | 0.034023       |
| **BILL_AMT_SEPT**   | 0.032371       |
| **PAY_AMT_JUL**     | 0.027418       |
| **AGE**             | 0.020332       |

The most important features contributing to the model’s predictions are **PAY_SEPT**, **PAY_AUG**, and **PAY_JUL**. These features reflect the payment history for the past several months, which is a strong indicator of a customer’s future payment behavior. 

## Industry Relevance 💼

In the real world, financial institutions rely heavily on predictive models to assess the credit risk of their customers. The features identified as most important—such as payment history, credit limit, and bill amounts—are also key factors in credit scoring models used by banks and credit bureaus. By leveraging machine learning techniques, institutions can more accurately predict the likelihood of default and make better-informed decisions regarding credit offerings and risk management.

### Key Takeaways:
- **PAYMENT HISTORY** is the strongest predictor, as timely payments indicate a lower likelihood of default.
- **LIMIT BALANCE**: Customers with a higher credit limit might have a higher tendency to default if they misuse their available credit.
- **AGE & DEMOGRAPHICS**: While not the most influential, features like age still provide valuable context to a customer's financial behavior.

## Conclusion 🎉

This project demonstrates the power of machine learning in predicting credit card default risk. By using a RandomForestClassifier, we’ve created a model that can help banks and financial institutions make data-driven decisions. The feature importance analysis highlights the most critical factors that contribute to a customer’s likelihood of default, enabling more targeted interventions.

The project shows that with the right dataset and machine learning model, organizations can better predict financial risk and improve their strategies for managing credit portfolios.

## 🚀 Future Work:
- Explore other machine learning algorithms (e.g., XGBoost, Neural Networks) for potentially better performance.
- Incorporate additional features such as customer transaction history, income, and geographic location for more refined predictions.
- Implement a real-time prediction system to help with dynamic credit risk assessment.

---

Thanks for checking out this project! Feel free to explore the code and contribute with improvements! ✨

🔗 [[GitHub Repo Link] ](https://github.com/29nasa/Credit_Card_Default/blob/main/Credit_Card_Default_Risk_Classification_Prediction.ipynb) 
📧 Contact: nasa.khatri@gmail.com
