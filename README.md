# Customer Churn Prediction using Machine Learning

## Project Overview 
This project aims to predict customer churn using the Telco Customer Churn dataset from Kaggle, provided by IBM. Building on insights from Prabadevi et al. (2023), Umayaparvathi (2016), and Petkovski (2016), it employs three machine learning models: Random Forest, K-Nearest Neighbors (KNN), and Gradient Boosting. After evaluating the models and performing hyperparameter tuning, Random Forest achieved the best results. Recommendations based on this model include enhancing customer support, offering personalized promotions, improving overall customer experience, regularly collecting feedback, and implementing targeted retention strategies to reduce churn and prevent revenue loss.

## Flow chart of the Project

![Flowchart- customer churn](https://github.com/ss22aba/NEW/assets/117084208/f2c477f1-be80-4bdc-8945-3ce7edfcddcd)

##  Required Libraries 

1. Data Handling Libraries:

pandas : Used for data manipulation and analysis.
numpy : Used for numerical operations.

2. Time Management:

time: Standard Python library for time-related functions.

3. Visualization Libraries:

matplotlib.pyplot : Used for creating static visualizations.
seaborn : Based on Matplotlib, used for statistical data visualization.
plotly.express : Used for easy-to-use interactive visualizations.
plotly.graph_objects : Used for creating more complex interactive visualizations.
plotly.subplots : Used for creating subplot figures.
missingno : Used for visualizing missing data.

4. Preprocessing Libraries:

sklearn.model_selection : Used for splitting the data into training and testing sets.
sklearn.preprocessing: Used for scaling the features.

5. Evaluation Libraries:

sklearn.metrics (imported confusion_matrix, ConfusionMatrixDisplay, accuracy_score, classification_report, roc_curve, auc, roc_auc_score): Used for evaluating the performance of the models.
sklearn.dummy : Used for creating simple baseline classifiers.
sklearn.inspection : Used for assessing the importance of features.
skopt : Used for Bayesian optimization of hyperparameters.

6. Model Libraries:

sklearn.neighbors : Used for K-Nearest Neighbors classification.
sklearn.ensemble : Used for ensemble learning methods (Random Forest and Gradient Boosting).

7. Warnings Management:

warnings: Standard Python library for managing warning messages (configured to ignore FutureWarning).

## Dataset
- Telco Customer Churn Dataset is the dataset used.
- **Data Format** : CSV Format (Each record is structured as a row in the CSV file, with columns representing different attributes of the customers and their service usage).
- **Number of Records** : The dataset usually contains around 7,000 to 7,500 records.
- **Data File Size** : 977.5 kB (0.95 MB)
- **Dataset Provider** : IBM
- **Dataset Link** : https://www.kaggle.com/datasets/blastchar/telco-customer-churn

## Exploratory Data Analysis

### Churn distribution
<img width="1156" alt="churn distribution" src="https://github.com/ss22aba/NEW/assets/117084208/44dca2ea-d764-406f-aa44-6a9c0ee2fbae">

### Numerical Features
- Tenure
- Monthly Charges
- Total Charges

The KDE plot for tenure reveals that customers who have been with the company for a short period (low tenure) are more prone to churn. 

<img width="938" alt="KDE Tenure" src="https://github.com/ss22aba/NEW/assets/117084208/07398231-a437-40af-9c98-67c4ebb42ce4">

The KDE plot for monthly charges reveals that customers with higher monthly charges are more likely to churn. 

<img width="938" alt="KDE Month" src="https://github.com/ss22aba/NEW/assets/117084208/9775831a-4a5a-463c-9800-befc9a33af11">

The KDE plot for total charges implies that customers with lower total charges are more prone to churn. This could be due to shorter tenure or dissatisfaction with the service.

<img width="945" alt="KDE Total charges" src="https://github.com/ss22aba/NEW/assets/117084208/805cf3a0-228e-4bef-9055-37760f37da6f">

### Categorical Features
#### Demographic Information

- Gender
- SeniorCitizen
- Partner
- Dependents

##### Description
- Gender does not appear to be a significant factor in customer churn. Both male and female customers exhibit similar churn patterns
- Senior citizens are more likely to churn than non-senior citizens.
- Customers without partners are more likely to churn compared to those without.
- Customers without dependents (Dependents = No) have a higher churn rate.

![demographic](https://github.com/ss22aba/NEW/assets/117084208/59945e2e-fbcd-4527-aa56-5cb1cf40849c)


#### General Services

- PhoneService
- MultipleLines
- InternetService
- StreamingTV
- StreamingMovies

##### Description
- Customers without phone service are more likely to churn.
- Customers without multiple lines tend to churn.
- Customers with no internet service or fiber optic service have a higher churn rate, with fiber optic showing a significant proportion of churn.
-  The churn rate is higher among customers who do not use streaming TV services.
-  The churn rate is higher among customers who do not use streaming movie services.

![General Service](https://github.com/ss22aba/NEW/assets/117084208/336dfb54-384c-4c91-821f-695029247a00)

#### Support Services

- OnlineSecurity
- OnlineBackup
- DeviceProtection
- TechSupport

##### Description
- Customers without online security services show a higher tendency to churn.
- The churn rate is higher among customers who do not use online backup services.
- Customers without device protection services are more likely to churn.
- The churn rate is higher among customers who do not have tech support services.

![Support Service](https://github.com/ss22aba/NEW/assets/117084208/5d3601d4-1224-4fe0-b1dc-6cd7cdbbb958)

#### Payments

- Contract
- PaperlessBilling
- PaymentMethod

##### Description
- Month-to-month contracts are more prone to churn.
- Customers with paperless billing show a higher churn rate compared to those with traditional billing methods.
- Churn rates are higher among customers using electronic checks.

![Payments](https://github.com/ss22aba/NEW/assets/117084208/b8c46fa4-ce49-4bd1-844f-ce06975e2290)

## Summary of the Base Models Performance 

![Base Model Performance ](https://github.com/ss22aba/NEW/assets/117084208/140f73c3-3289-4968-8487-8c40dc8c5e79)

## Summary of the Hyperparameter tuned models Performance

Random Forest achieved the best results with an accuracy of 0.80.

![Hypertuned Model Performance ](https://github.com/ss22aba/NEW/assets/117084208/ca62d781-a572-49cd-872e-b669a5a28846)

### ROC curve for the Random Forest Classifier

![ROC- Random Forest](https://github.com/ss22aba/NEW/assets/117084208/e0cdbde8-04c6-4110-8ca2-fb9c0c698cd2)

## Important Predictors

![Important Predictors](https://github.com/ss22aba/NEW/assets/117084208/1dd07b8d-28bf-452d-a89d-0d21f56f2b93)


## Recommendations to Reduce Customer Churn
Based on the insights from the optimized Random Forest model and the EDA, the following recommendations are proposed to reduce revenue loss and minimize customer churn:

1. **Promote Long-Term Contracts :** 

Why: Customers on longer contracts (one or two years) are less likely to leave compared to those on month-to-month plans.

Action: Offer discounts, bundles, or rewards to encourage customers to choose longer contracts. Emphasize the benefits and savings in your marketing.

2. **Improve Paperless Billing :**

Why: Customers using paperless billing are leaving more often, which might mean they are unhappy with the process.

Action: Make paperless billing easier to use and more reliable. Provide strong customer support for any issues and make sure the system works smoothly.

3. **Encourage Automated Payments :**

Why: Customers using automated payments (like bank transfers or credit cards) are less likely to leave than those paying manually or with electronic checks.

Action: Offer benefits like discounts or rewards for switching to automated payments. Educate customers on the ease and reliability of these payment methods.

4. **Focus on Month-to-Month Customers :**

Why: Customers with month-to-month contracts are more likely to leave, so they need more attention to keep them.

Action: Run special retention campaigns for month-to-month customers, offering promotions, personalized communication, and special perks. Regularly check in to address their needs and concerns.

5. **Enhance Customer Support Services :**

Why: Good support services (like online security, backup, device protection, and tech support) help keep customers from leaving.

Action: Improve the quality and availability of these support services. Train support staff well and ensure quick resolution of issues. Educate customers on the benefits of these services to increase their use and satisfaction.




## References

1. Petkovski, A.J., Stojkoska, B.L.R., Trivodaliev, K.V. and Kalajdziski, S.A. (2016). ‘Analysis of churn prediction: A case study on telecommunication services in Macedonia’. 2016 24th Telecommunications Forum (TELFOR).

2. Prabadevi, B., Shalini, R. and Kavitha, B.R. (2023).‘Customer churning analysis using machine learning algorithms’. International Journal of Intelligent Networks, [online] 4.
doi:https://doi.org/10.1016/j.ijin.2023.05.005.

3. Umayaparvathi, V. and Iyakutti, K. (2016). ‘Attribute selection and Customer Churn Prediction in telecom industry’. 2016 International Conference on Data Mining and Advanced Computing (SAPIENCE). doi:https://doi.org/10.1109/sapience.2016.7684171.





