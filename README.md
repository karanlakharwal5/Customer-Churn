## Telecom Customer Churn Prediction  


There were three datasets namely:  
+ churn_data.csv - gives basic data about the customers from the last month and if they churned or not  
+ customer_data.csv - cutmore demographics like id, gender etc.  
+ internet_data.csv - the services availed by the customer. 

These datasets were joined using customer_id as the index


Upon the exploratory analysis I found below features to be of importance:
tenure, Contract(Month-to-month),Contract(Month-to-month), InternetService(FiberOptics), PaymentMethod(ElectronicCheck), OnlineSecurity(No), TotalCharges to be the most influencing features that determine if a Customer Churns or not.

After exploratory analysis, I tried to  clean the data. A few entries in features were substituted  to replace "No Internet Service" with "No".
To encode the remaining categorical features I used the category_encoders library because it saves a lot of work as compared to label encoding and one hot encoding as it keeps the feature names and their distinct values intact to be used a feature labels.

I initially planned to perform Logistic Regression on the dataset and after we were done we thought of playing with other classification algorithms also. We implemented NaiveBaiyes, KNN, Neural Netwroks and Decison Trees on the dataset.

In addition to these, I found out what **HyperParameter Tuning** is and incorporated it into the KNN Model which was a great learning experience.

Each classification model has its own method of learning from data.
Below are the scores on prediction of test dataset for all the models that we implemented.

| Model | Scores  | AUC Scores|
| ------| --- |----|
| Logistic Regression| 0.8122|0.7292|
| KNN| 0.7940|0.6888|
| NaiveB| 0.7804|0.7314|
| NeuralNetwork| 0.8094|0.6943|
| DecisionTree| 0.7935|0.7025|

