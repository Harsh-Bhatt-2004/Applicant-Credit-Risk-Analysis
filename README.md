# Applicant Credit Risk Analysis

## Overview
This project is about developing a machine learning model to assess and predict the credit risk of loan applications. The project involves step by step processes on data like preprocessing, Exploratory Data Analysis(EDA), encoding, feature engineering & scaling, splitting data based on feature and target variables, import and train model based on that data, test if it is good for our data and last deploy the model.

## Problem Statement
Many financial institutions face uncertainty and risk when approving loan applications based on applicant details. Sometimes, they may overlook key factors, leading to potential risks in the future that can harm the company's reputation and standing in the market. Our aim is to identify the specific details and scenarios where there is a significant risk in approving a loan, based on a calculated risk percentage.


## Data Preprocessing
  - In our project, we handled missing values by identifying the null values and filling them using the most suitable method.
  - For numerical features, we used mean imputation, while for categorical features, we used mode imputation. 

## Exploratory Data Analysis(EDA)
  - While Performing Exploratory Data Analysis(EDA) we create histogram, scatter plots to see the relationship between columns in data.
  - Like, We can calculate mean, median or mode of data as well as see the correlation using heatmap for better insight gaining.
    
## Encoding Categorical Variables
  - Before going to create a model, we have some categorical columns, so using **LabelEncoder** we encode them all in numeric format.
  - This transformation ensured that all categorical variables were converted into a numerical format suitable for machine learning models.
     
## Feature Engineering and Selection
  - In this step, we identify the important features that will be used for model training. This involves analyzing the dataset to understand which features are most relevant to predicting the target variable.
  - We split the data into features (x) and the target variable (y). The features (x) represent the input data, while the target variable (y) represents the output we want to predict.

## Splitting the Data
  - Using, **train_test_split** which is available in sklearn.model_selection library, allow to split the feature and target variables into train and test part. 
  - Here, we specified ratio of **80-20** for training and testing part where we use **random_state** for remaining the prediction static.

## Training and Evalation
  - After successful partition of trainig and testing data we import the model like here we import **KNeighbourClassifier** and store it into **model** variable specifying that we have **8 neighbours** means from given point it choose nearest 8 neighbours.
  - Then train the model using training data like we use **model.fit(x_train_y_train)** and make prediction and evaluate the scores and modify the model if necessary. 

## Results
  - The overall accuracy of our model is **67%**, which indicates a moderate level of performance in predicting applicant credit risk.
  - From the scatter plots and other visualizations, we observe a good alignment between predicted and actual loan approvals, demonstrating the model's effectiveness.
  - The model shows promising results for future predictions, maintaining consistency in its performance.
 
## Conclusion
In conclusion, the classifier model created using the K-Nearest Neighbors (KNN) algorithm effectively works on the feature/input data provided by the user. Based on the training, it predicts the outcome in Yes/No (i.e., 1/0). This allows financial institutions to input applicant data into the model and receive a classified result, indicating whether they can approve or deny the applicant's loan request. The model provides a reliable tool for assessing credit risk and making informed lending decisions.
