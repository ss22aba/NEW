Customer Churn

Customer churn is defined as the phenomenon where customers or subscribers discontinue their business relationship with a firm or service.

In the telecom industry, customers have the option to choose from a variety of service providers and often switch between them. This results in an annual churn rate of 15-25 percent in this highly competitive market.

Individualised customer retention is challenging because most firms have a large customer base and cannot afford to allocate significant time and resources to each individual. The costs would be prohibitive and outweigh the potential additional revenue. However, if a company could predict which customers are likely to leave ahead of time, it could concentrate retention efforts on these "high-risk" clients. The ultimate goal is to expand coverage and enhance customer loyalty. The key to success in this market lies in understanding and serving the customer.

Customer churn is a critical metric because retaining existing customers is significantly less expensive than acquiring new ones.

To detect early signs of potential churn, it is essential to develop a comprehensive view of customers and their interactions across various channels. By addressing churn proactively, businesses can not only maintain their market position but also grow and thrive. The more customers a company retains, the lower the acquisition costs and the higher the profitability. Therefore, the company's primary focus for success should be on reducing customer attrition and implementing effective retention strategies.

Objective

Finding the % of Churn Customers and customers that keep in with the active services.
Analysing the data in terms of various features responsible for customer Churn
Finding a most suited machine learning model for correct classification of Churn and non churn customers.

Dataset Description

Churn Status: Indicates whether customers left within the last month (column: Churn).

Subscribed Services: Details the services each customer has signed up for, including phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies.

Customer Account Information: Contains data on customer tenure, contract type, payment method, paperless billing status, monthly charges, and total charges.

Demographic Information: Provides demographic details such as gender, age range, and whether customers have partners and dependents.

Dataset in detail :

Gender -- Whether the customer is a male or a female

SeniorCitizen -- Whether a customer is a senior citizen or not

Partner -- Whether the customer has a partner or not (Yes, No)

Dependents -- Whether the customer has dependents or not (Yes, No)

Tenure -- Number of months the customer has stayed with the company

Phone Service -- Whether the customer has a phone service or not (Yes, No)

MultipleLines -- Whether the customer has multiple lines or not

InternetService -- Customer's internet service provider (DSL, Fiber Optic, No)

OnlineSecurity -- Whether the customer has online security or not (Yes, No, No Internet)

OnlineBackup -- Whether the customer has online backup or not (Yes, No, No Internet)

DeviceProtection -- Whether the customer has device protection or not (Yes, No, No internet service)

TechSupport -- Whether the customer has tech support or not (Yes, No, No internet)

StreamingTV -- Whether the customer has streaming TV or not (Yes, No, No internet service)

StreamingMovies -- Whether the customer has streaming movies or not (Yes, No, No Internet service)

Contract -- The contract term of the customer (Month-to-Month, One year, Two year)

PaperlessBilling -- Whether the customer has paperless billing or not (Yes, No)

Payment Method -- The customer's payment method (Electronic check, mailed check, Bank transfer(automatic), Credit card(automatic))

MonthlyCharges -- The amount charged to the customer monthly

TotalCharges -- The total amount charged to the customer

Churn -- Whether the customer churned or not (Yes or No)

Implementation:

Libraries: sklearn, Matplotlib, pandas, seaborn, and NumPy
