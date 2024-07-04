# Customer Churn Prediction using Machine Learning

## Project Overview 
This project aims to predict customer churn using the Telco Customer Churn dataset from Kaggle, provided by IBM. Building on insights from Prabadevi et al. (2023), Umayaparvathi (2016), and Petkovski (2016), it employs three machine learning models: Random Forest, K-Nearest Neighbors (KNN), and Gradient Boosting. After evaluating the models and performing hyperparameter tuning, Random Forest achieved the best results. Recommendations based on this model include enhancing customer support, offering personalized promotions, improving overall customer experience, regularly collecting feedback, and implementing targeted retention strategies to reduce churn and prevent revenue loss.

## Flow chart of the Project

![Flowchart](https://github.com/ss22aba/NEW/assets/117084208/2eae1323-1d7a-49dd-802d-6753aeae488f)

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
- **Gender** does not appear to be a significant factor in customer churn. Both male and female customers exhibit similar churn patterns
- **Senior citizens** (SeniorCitizen = 1) are more likely to churn than non-senior citizens (SeniorCitizen = 0).
- **Customers without partners** are more likely to churn compared to those without.
- **Customers without dependents** (Dependents = No) have a higher churn rate.

  
![demographic](https://github.com/ss22aba/NEW/assets/117084208/f7cf992e-e1ce-412d-8572-96e556ec9c10)

#### General Services

- PhoneService
- MultipleLines
- InternetService
- StreamingTV
- StreamingMovies

![General Service](https://github.com/ss22aba/NEW/assets/117084208/336dfb54-384c-4c91-821f-695029247a00)

#### Support Services

- OnlineSecurity
- OnlineBackup
- DeviceProtection
- TechSupport

![Support Service](https://github.com/ss22aba/NEW/assets/117084208/5d3601d4-1224-4fe0-b1dc-6cd7cdbbb958)

#### Payments

- Contract
- PaperlessBilling
- PaymentMethod

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
Based on the insights from the optimized Random Forest model, the following recommendations are proposed to reduce revenue loss and minimize customer churn:

- **Customized Offers and Discounts** : Use predictive insights to offer personalized discounts, promotions, or loyalty rewards to at-risk customers. Tailored offers can enhance customer satisfaction and incentivize them to stay.
  
- **Regular Feedback Collection** : Implement regular feedback collection mechanisms to understand customer needs and concerns. Use this feedback to continuously improve services and address any issues promptly.
  
- **Proactive Customer Support** : Establish a proactive customer support system to reach out to customers showing signs of dissatisfaction. This can include regular check-ins, personalized support, and addressing potential issues before they lead to churn.

- **Loyalty Programs** : Develop and enhance loyalty programs to reward long-term customers. Exclusive benefits and rewards for loyal customers can increase retention rates.

- **Customer Education Programs**: Create educational content to help customers better understand and utilize the services offered. Informed customers are more likely to see the value in staying with the company.

## References

1. Petkovski, A.J., Stojkoska, B.L.R., Trivodaliev, K.V. and Kalajdziski, S.A. (2016). ‘Analysis of churn prediction: A case study on telecommunication services in Macedonia’. 2016 24th Telecommunications Forum (TELFOR).

2. Prabadevi, B., Shalini, R. and Kavitha, B.R. (2023).‘Customer churning analysis using machine learning algorithms’. International Journal of Intelligent Networks, [online] 4.
doi:https://doi.org/10.1016/j.ijin.2023.05.005.

3. Umayaparvathi, V. and Iyakutti, K. (2016). ‘Attribute selection and Customer Churn Prediction in telecom industry’. 2016 International Conference on Data Mining and Advanced Computing (SAPIENCE). doi:https://doi.org/10.1109/sapience.2016.7684171.





