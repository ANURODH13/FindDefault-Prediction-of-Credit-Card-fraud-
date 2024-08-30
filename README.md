Problem Statement:
A credit card is one of the most used financial products to make online purchases and payments. Though the Credit cards can be a convenient way to manage your finances, they can also be risky. Credit card fraud is the unauthorized use of someone else's credit card or credit card information to make purchases or withdraw cash. It is important that credit card companies are able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase.

About Credit Card Fraud Detection:
What is credit card fraud detection?

Credit card fraud detection is the collective term for the policies, tools, methodologies, and practices that credit card companies and financial institutions take to combat identity fraud and stop fraudulent transactions.

In recent years, as the amount of data has exploded and the number of payment card transactions has skyrocketed, credit fraud detection has become largely digitized and automated. Most modern solutions leverage artificial intelligence (AI) and machine learning (ML) to manage data analysis, predictive modeling, decision-making, fraud alerts and remediation activity that occur when individual instances of credit card fraud are detected.

Anomaly detection

Anomaly detection is the process of analyzing massive amounts of data points from both internal and external sources to produce a framework of “normal” activity for each individual user and establish regular patterns in their activity.

Data used to create the user profile includes:

Purchase history and other historical data
Location
Device ID
IP address
Payment amount
Transaction information
When a transaction falls outside the scope of normal activity, the anomaly detection tool will then alert the card issuer and, in some cases, the user. Depending on the transaction details and risk score assigned to the action, these fraud detection systems may flag the purchase for review or put a hold on the transaction until the user verifies their activity.

What can be an anomaly?

A sudden increase in spending
Purchase of a large ticket item
A series of rapid transactions
Multiple transactions with the same merchant
Transactions that originate in an unusual location or foreign country
Transactions that occur at unusual times
If the anomaly detection tool leverages ML, the models can also be self-learning, meaning that they will constantly gather and analyze new data to update the existing model and provide a more precise scope of acceptable activity for the user.

Project Introduction:
The dataset contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

In this Project, we have to build a classification model to predict whether a transaction is fraudulent or not. We will use various predictive models to see how accurate they are in detecting whether a transaction is a normal payment or a fraud. Let's start!

Project Outline:
Exploratory Data Analysis: Analysing and understanding the data to identify patterns, relationships, and trends in the data by using Descriptive Statistics and Visualizations.
Data Cleaning: Checking for the data quality, handling the missing values and outliers in the data.
Dealing with Imbalanced data: This data set is highly imbalanced. The data should be balanced using the appropriate Resampling Techniques (NearMiss Undersampling, SMOTETomek) before moving onto model building.
Feature Engineering: Transforming the existing features for better performance of the ML Models.
Model Training: Splitting the data into train & test sets and use the train set to estimate the best model parameters.
Model Validation: Evaluating the performance of the models on data that was not used during the training process. The goal is to estimate the model's ability to generalize to new, unseen data and to identify any issues with the model, such as overfitting.
Model Selection: Choosing the most appropriate model that can be used for this project.
Model Deployment: Model deployment is the process of making a trained machine learning model available for use in a production environment.
Project Work Overview:
Our dataset exhibits significant class imbalance, with the majority of transactions being non-fraudulent (99.82%). This presents a challenge for predictive modeling, as algorithms may struggle to accurately detect fraudulent transactions amidst the overwhelming number of legitimate ones. To address this issue, we employed various techniques such as undersampling, oversampling, and synthetic data generation.

Undersampling: We utilized the NearMiss technique to balance the class distribution by reducing the number of instances of non-fraudulent transactions to match that of fraudulent transactions. This approach helped in mitigating the effects of class imbalance. Our attempt to address class imbalance using the NearMiss technique did not yield satisfactory results. Despite its intention to balance the class distribution, the model's performance was suboptimal. This could be attributed to the loss of valuable information due to the drastic reduction in the majority class instances, leading to a less representative dataset. As a result, the model may have struggled to capture the intricacies of the underlying patterns in the data, ultimately affecting its ability to accurately classify fraudulent transactions.

Oversampling: To further augment the minority class, we applied the SMOTETomek method with a sampling strategy of 0.75. This resulted in a more balanced dataset, enabling the models to better capture the underlying patterns in fraudulent transactions.

Machine Learning Models: After preprocessing and balancing the dataset, we trained several machine learning models, including:

Logistic Regression
K-Nearest Neighbors (KNN)
Random Forest Classifier
AdaBoost Classifier
XGBoost Classifier
Evaluation Metrics: We evaluated the performance of each model using various metrics such as accuracy, precision, recall, and F1-score. Additionally, we employed techniques like cross-validation and hyperparameter tuning to optimize the models' performance.

Model Selection: Among the various models and balancing methods experimented with, the XGBoost model stands out as the top performer when using oversampling techniques. Despite the inherent challenges posed by imbalanced datasets, the XGBoost algorithm demonstrates robustness and effectiveness in capturing the underlying patterns associated with fraudulent transactions. By generating synthetic instances of the minority class through oversampling methods like SMOTETomek, the XGBoost model achieves a more balanced representation of the data, enabling it to learn and generalize better to unseen instances. This superior performance underscores the importance of leveraging advanced ensemble techniques like XGBoost, particularly in the context of imbalanced datasets characteristic of credit card fraud detection.

In summary, our approach involved preprocessing the imbalanced dataset using undersampling and oversampling techniques, followed by training and evaluating multiple machine learning models. By systematically exploring different methodologies and algorithms, we aimed to develop robust fraud detection XGBoost model capable of accurately identifying fraudulent transactions while minimizing false positives.

Future Work:
Anomaly detection techniques, including isolation forests and autoencoders, offer specialized capabilities for identifying outliers and anomalies within datasets. By incorporating these methods alongside traditional classification approaches, we can enhance the effectiveness of fraud detection systems. Isolation forests excel at isolating anomalies by randomly partitioning data points, making them particularly useful for detecting fraudulent transactions that deviate from normal patterns. Autoencoders, on the other hand, leverage neural networks to reconstruct input data, effectively learning representations of normal behavior and flagging deviations as potential anomalies.

Exploring the integration of advanced deep learning models like Convolutional Neural Networks (CNNs) and Recurrent Neural Networks (RNNs) alongside traditional machine learning techniques holds significant promise for enhancing fraud detection systems. These neural network architectures offer unique capabilities for processing sequential and structured data, which are crucial in identifying anomalous patterns indicative of fraudulent activities. By leveraging CNNs and RNNs, alongside hybrid models that combine the strengths of both deep learning and traditional algorithms, we can improve accuracy, adaptability, and overall performance in fraud detection. Additionally, techniques such as unsupervised learning, transfer learning, and feature extraction through deep learning can further enhance the efficiency and effectiveness of fraud detection systems. Through these advancements, we aim to bolster our ability to detect and prevent fraudulent transactions, ultimately safeguarding financial systems and protecting consumers from financial losses.
![image](https://github.com/user-attachments/assets/294ea852-ed91-44e1-a886-fffe653a21f1)

