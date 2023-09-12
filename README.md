# Email Spam Detection

## Introduction

The project focuses on developing a machine learning model to classify emails as either spam or not spam (ham) using the Naive Bayes classification algorithm. Spam emails are unwanted and potentially harmful messages, while ham emails are legitimate and desired communications.

## Project Workflow

1. **Data Import:** The project begins by importing necessary libraries, such as NumPy and pandas. A dataset named 'spam.csv' is loaded using pandas, which contains email messages and their corresponding categories (spam or ham).

2. **Exploratory Data Analysis (EDA):** The dataset is explored to understand its structure and contents. This includes examining the columns, checking for missing values, and gaining insights into the data.

3. **Data Preprocessing:** The "Unnamed: 0" column, which appears to be an unnecessary identifier, is dropped from the dataset. Missing values are also checked, ensuring data completeness.

4. **Label Encoding:** A new binary column "Spam" is created, where emails categorized as "spam" are assigned the value 1, and "ham" emails are assigned 0. This column will serve as the target variable for the machine learning model.

5. **Data Splitting:** The dataset is split into training and testing sets using the `train_test_split` function from scikit-learn. This allows for training the model on one portion of the data and evaluating its performance on another.

6. **Text Vectorization:** The email text data is converted into numerical format using the CountVectorizer, which represents the text as a matrix of word frequencies. This is a crucial step in preparing the text data for machine learning.

7. **Multinomial Naive Bayes Model:** A Multinomial Naive Bayes classifier is chosen for this task because the email data is in discrete form, similar to movie ratings, where each word has a certain frequency to represent it. The scikit-learn library's `MultinomialNB` class is used to create the Naive Bayes model.

8. **Model Training:** The Naive Bayes model is trained on the training data. A scikit-learn pipeline is used to streamline the process, including text vectorization and model training.

9. **Email Classification:** Two example emails are provided to the model to demonstrate its functionality. The model predicts whether each email is spam or ham based on the text content.

10. **Model Evaluation:** The model's performance is assessed using the testing dataset, and its accuracy score is calculated. This score indicates how well the model can classify emails as spam or ham.

## Conclusion

The "Email Spam Classification using Naive Bayes" project showcases the process of building a machine learning model to detect spam emails. By utilizing the Multinomial Naive Bayes classifier and CountVectorizer for text representation, the model demonstrates the ability to classify emails accurately. The project highlights the importance of data preprocessing, feature engineering, and model evaluation in the context of email classification, contributing to the broader field of email filtering and cybersecurity.
