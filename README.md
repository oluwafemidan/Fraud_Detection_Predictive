<div align="center">

[1]: https://github.com/oluwafemidan
[2]: https://www.linkedin.com/in/oluwafemidanielajala/
[3]: https://public.tableau.com/app/profile/oluwafemi.daniel/vizzes
[4]: https://twitter.com/ajala14055

[![GitHub](https://github.com/oluwafemidan/Fraud_Detection_Predictive/assets/146761013/2c70a08b-a628-4800-8a8d-1f738b00e865)][1]
[![LinkedIn](https://github.com/oluwafemidan/Fraud_Detection_Predictive/assets/146761013/82b1f60f-5244-4081-bc5b-ad72ef2daa7e)][2]
[![tableau](https://github.com/oluwafemidan/Fraud_Detection_Predictive/assets/146761013/d3d07da2-a8d4-4e36-8777-00231254610e)][3]
[![X](https://github.com/oluwafemidan/Fraud_Detection_Predictive/assets/146761013/4d790bae-2842-4d0f-af0a-1f48d59b704e)][4]

</div>

# <div align="center">Fraud Detection Predictive</div>
<div align="center"><img src ="https://github.com/oluwafemidan/Fraud_Detection_Predictive/assets/146761013/cb842497-14d1-48e0-9ea7-db69ae8e4fe2"></div>

## Overview
In the ever-evolving landscape of financial services, the detection and prevention of fraudulent activities are paramount for maintaining trust, security, and regulatory compliance. Financial institutions grapple with the challenges of identifying unauthorized transactions and thwarting identity theft, necessitating innovative solutions for effective fraud detection. This project aims to address these challenges through the strategic application of data analytics.

## Objectives
Implement rigorous data cleaning and preprocessing strategies to guarantee the reliability and accuracy of the dataset, bolstering the effectiveness of fraud detection analyses.

Leverage advanced analytics to identify abnormal patterns within transaction data, providing actionable insights for proactive fraud prevention.

Develop models to continuously monitor user behavior, detecting anomalies indicative of potential fraudulent activities and fortifying the institution's security measures.

## Fraud Detection Data
- **TransactionID:** Unique identifier for each financial transaction.
- **TransactionAmount:** The monetary value associated with each transaction, reflecting the amount of money transferred.
- **MerchantID:** Identification number assigned to the merchant involved in the transaction.
- **UserID:** Unique identifier for each user/customer conducting the transaction.
- **TransactionTime:** Timestamp indicating the date and time when the transaction occurred.
- **TransactionType:** Categorization of the transaction as either "Online" or "In-store", denoting the method through which the transaction was initiated.
- **Region:** Location or region where the transaction took place, providing geographical context.
- **TransactionFrequency:** Number of transactions associated with the user, indicating the user's transaction activity level.
- **MerchantFrequency:** Frequency of transactions with the specific merchant, indicating the merchant's popularity or regularity of transactions.
- **TransactionHour:** Hour of the day when the transaction occurred, providing temporal context.
- **FraudIndicator:** Binary indicator (0 or 1) representing whether the transaction is fraudulent (1) or not (0), facilitating fraud detection and prevention efforts.

## Mapping
![Mapping](https://github.com/oluwafemidan/Heart-disease-prediction/assets/146761013/bf71ba31-2669-4e9d-b7df-829e35baefa2)

## Implementation:

**Libraries:**  `NumPy` `pandas` `matplotlib` `sklearn` `seaborn` 

## Data Exploration
The dataset has 169 (2%) fraudulent transactions and 8394 (98%) non-fraudulent transactions. That means the data is highly unbalanced with respect with target variable Class.

### Feature Engineering
`TransactionFreqRatio` refers to a calculated metric that represents the normalized transaction frequency for each entry in the dataset. It is obtained by dividing the transaction frequency of each entry (the number of transactions associated with that entry) by the average transaction frequency across the entire dataset. This ratio provides a measure of how many times more or less frequent a particular entry's transactions are compared to the average transaction frequency. It allows for the comparison of transaction frequencies across different entries while accounting for variations in the overall dataset.

`MerchantFreqRatio` refers to a calculated metric that represents the normalized merchant frequency for each entry in the dataset. It is obtained by dividing the merchant frequency of each entry (the number of transactions associated with a particular merchant) by the average merchant frequency across the entire dataset. This ratio provides a measure of how many times more or less frequent a particular entry's transactions with a specific merchant are compared to the average merchant frequency. It allows for the comparison of merchant frequencies across different entries while accounting for variations in the overall dataset.

### Machine Learning
Each classifier is represented as a list containing an instance of a classifier model from scikit-learn and a string indicating the name of the classifier. This setup allows for easy iteration and identification of different classifiers within a machine learning pipeline.
```
classifiers = [[XGBClassifier(),'XGB Classifier'],
              [RandomForestClassifier(),'Random Forest'],
              [LogisticRegression(),'Logistic Regression'],
              [KNeighborsClassifier(), 'K-Nearest Neighbours'],
              [SGDClassifier(),'SGD Classifier']]
```
This code snippet trains multiple classifier models on training data and evaluates their performance metrics on test data. It iterates over a list of classifiers, fits each model, computes metrics such as accuracy score, cross-validation score, and ROC AUC score, and prints the results. Finally, it appends the metrics to lists for further analysis.
```
score_list = []
cross_val_list = []
roc_auc_list = []

for classifier in classifiers:
    model = classifier[0]
    model.fit(X_train, Y_train)
    model_name = classifier[1]
    
    pred = model.predict(X_test)

    score = model.score(X_test, Y_test)
    cross_val = cross_val_score(model, X_test, Y_test).mean()
    roc_auc = roc_auc_score(Y_test, pred)
    
    score_list.append(score)
    cross_val_list.append(cross_val)
    roc_auc_list.append(roc_auc)
    
    print(model_name, 'model score:     ' + str(round(score*100, 2)) + '%')
    print(model_name, 'cross val score: ' +str(round(cross_val*100, 2)) + '%')
    print(model_name, 'roc auc score:   ' + str(round(roc_auc*100, 2)) + '%')
    
    if model_name != classifiers[-1][1]:
        print('')
```
### Feedback

If you have any feedback, please reach out at ajalaoluwafemidaniel@gmail.com


### 🚀 About Me
#### Hi, I'm OLuwafemi! 👋
I am an AI Enthusiast and Data science & ML practitioner























[1]: https://github.com/oluwafemidan
[2]: https://www.linkedin.com/in/oluwafemidanielajala/
[3]: https://public.tableau.com/app/profile/oluwafemi.daniel/vizzes
[4]: https://twitter.com/ajala14055

[![GitHub](https://github.com/oluwafemidan/Fraud_Detection_Predictive/assets/146761013/2c70a08b-a628-4800-8a8d-1f738b00e865)][1]
[![LinkedIn](https://github.com/oluwafemidan/Fraud_Detection_Predictive/assets/146761013/82b1f60f-5244-4081-bc5b-ad72ef2daa7e)][2]
[![tableau](https://github.com/oluwafemidan/Fraud_Detection_Predictive/assets/146761013/d3d07da2-a8d4-4e36-8777-00231254610e)][3]
[![X](https://github.com/oluwafemidan/Fraud_Detection_Predictive/assets/146761013/4d790bae-2842-4d0f-af0a-1f48d59b704e)][4]




