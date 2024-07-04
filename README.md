# Customer Churn Prediction using Machine Learning

## Project Overview 
Customer churn prediction is crucial for businesses in competitive sectors like telecommunications, finance, and e-commerce. Accurately predicting churn helps companies implement retention strategies, reducing revenue loss and improving customer satisfaction. This project aims to develop a churn prediction system using three machine learning models:  **Random Forest, K-Nearest Neighbors (KNN), and Gradient Boosting**.

Random Forest constructs multiple decision trees to reduce overfitting and capture complex data interactions. KNN classifies data points based on their nearest neighbors, effective for non-linear relationships. Gradient Boosting sequentially builds models to correct errors, capturing intricate patterns for high accuracy.

These models will be enhanced through hyperparameter tuning to optimize performance. By adjusting parameters like the number of trees in Random Forest, neighbors in KNN, and boosting stages in Gradient Boosting, the goal is to achieve the best accuracy.

At the conclusion of the project, the effectiveness of the three hyper-tuned models will be assessed, and the best model will be chosen. This project aims to develop a state-of-the-art churn prediction system using advanced machine learning techniques and rigorous optimization, providing a reliable solution for improving customer retention strategies.

## Flow chart of the Project

![Flowchart](https://github.com/ss22aba/NEW/assets/117084208/2eae1323-1d7a-49dd-802d-6753aeae488f)


## Dataset
- Telco Customer Churn Dataset is the dataset used.
- **Data Format** : CSV Format (Each record is structured as a row in the CSV file, with columns representing different attributes of the customers and their service usage).
- **Number of Records** : The dataset usually contains around 7,000 to 7,500 records.
- **Data File Size** : 977.5 kB (0.95 MB)
- **Dataset Provider** : IBM via Kaggle
- **Dataset Link** : https://www.kaggle.com/datasets/blastchar/telco-customer-churn

## Exploratory Data Analysis

### Churn distribution
<img width="1156" alt="churn distribution" src="https://github.com/ss22aba/NEW/assets/117084208/44dca2ea-d764-406f-aa44-6a9c0ee2fbae">

### Numerical Features
- Tenure
- Monthly Charges
- Total Charges
<img width="938" alt="KDE Tenure" src="https://github.com/ss22aba/NEW/assets/117084208/07398231-a437-40af-9c98-67c4ebb42ce4">

<img width="938" alt="KDE Month" src="https://github.com/ss22aba/NEW/assets/117084208/9775831a-4a5a-463c-9800-befc9a33af11">

<img width="945" alt="KDE Total charges" src="https://github.com/ss22aba/NEW/assets/117084208/805cf3a0-228e-4bef-9055-37760f37da6f">

### Categorical Features
#### Demographic Information

- Gender
- SeniorCitizen
- Partner
- Dependents
  
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

