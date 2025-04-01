# Spam Email Prediction
This project focuses on predicting whether an email is spam or not using machine learning techniques. The dataset is analyzed, preprocessed, and used to train a classification model.

## Table of Contents
- Project Overview  
- Dataset Overview  
- Data Preprocessing  
- Model Training  
- Model Evaluation  
- Key Observations  

## Project Overview
The goal of this project is to build a predictive model using logistic regression to classify emails as either spam (1) or not spam (0) based on various textual features.

## Dataset Overview
The dataset is loaded from a CSV file named `spam.csv`. It contains information about a collection of emails, structured across multiple columns. Some key statistics about the dataset include:

- Total emails: **X**  
- Total columns: **Y**  
- Missing values: Some columns contain missing values, which are handled during preprocessing.

  ![image](https://github.com/user-attachments/assets/ed696e25-5bc3-4e71-a12e-ff2301a57ecc)


## Data Preprocessing
Before training the model, we perform the following data preprocessing steps:

![image](https://github.com/user-attachments/assets/35e5ca82-5dd5-4e7b-9619-123db78835df)


### Feature Engineering:
- Text data is converted into numerical format using `CountVectorizer` with **n-gram** features.
- Stop words are removed to improve model efficiency.

## Model Training
The dataset is split into training (80%) and testing (20%) subsets. A logistic regression model from the Scikit-learn library is trained to classify emails as spam or not spam.

![image](https://github.com/user-attachments/assets/a1617ad5-fcfd-4bfe-9958-5a8654665f4c)


![image](https://github.com/user-attachments/assets/325bcc92-b171-422a-a40f-b13e59a87b63)


## Model Evaluation
To assess the model’s performance, we use the following evaluation metrics:

![image](https://github.com/user-attachments/assets/9011f680-bfa7-4665-a31a-1a391f22bcf5)


### Confusion Matrix:
Provides insight into the model’s classification accuracy.

![image](https://github.com/user-attachments/assets/e97cf9e5-bf16-4fa4-a319-2ca17687efe0)


### Classification Metrics:
- Precision
- Recall
- Sensitivity
- Specificity

![image](https://github.com/user-attachments/assets/eb5d9b72-b021-46cc-9908-41fff27bfb33)


## Key Observations
To understand the impact of certain keywords on spam classification, we analyze the probability of an email being spam based on specific words:

```
As we have created a spam prediction model, it's important to classify all important emails as 0 (Not spam) and all spam emails as 1 (Spam).

Now, let's imagine a situation where our model incorrectly predicts an important email as spam (False Negative, FN). This would make our user very angry. In this situation, the most important metric is Recall     (Sensitivity) for the Not Spam class.
```


## Also predict letters, which isn't seen in the dataset

![image](https://github.com/user-attachments/assets/a15896ff-d1aa-43f1-9c14-4b98fff7206b)


Correctly predicted 3/3 letters either Spam or Not Spam
