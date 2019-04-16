# si_699_user_retention

This document can be divided into three parts.

- Description
- Overall Summary
- Summary of Every Week

### Description

This project is about investigating user retention in three months, it mainly can be divided into two part: 

- Predict whether they will come to use this app in last two weeks
- Predict how many days will they place their next order according to the history of their orders

### Overall Summary

Our project can be mainly devided into three phases: 

- The first phase is about defining problem and preparing.
- The second phase is about iterate our classification problem. 
- The third phase is about error analysis and regression problem.

We spend the first three weeks in our first phase. we investigating data and did some basic prepare jobs: We look through the data and define our problem, brainstorm the solutions and what will be deliverable in week 3.  We investigate the dataset and get a sense of what the data looks like in week 4. We further investigate our dataset in week5 and do retention rate analysis to define labels in our prediction problem.

In phase two, we iterate our classification problem in week 6 to week 10. After we first defining our problem as a classification problem, we did traditional machine learning process to our problem: In week 6, we did some basic feature engineering and make some baseline for our prediction problem. We did some feature selection and data cleaning in week 7, did some EDA in our new dataset and do some simple jobs to baseline models, such as log transfer and standard scale. In week 8, we continue iterating: we add more features, do other proprecessing to improve our baseline model and use ROC score as our model evaluation. We continue iterating in week 9, and use other models besides baseline models. In week 10, we did our last iteration in this problem.  We add more features, use rank to do feature selection, bootstrap and stack.

In phase three, we spend the last three weeks to do error analysis and regression problem. We did some error analysis for our classification problem and changed our problem to regression problem: In week 11, we add PCA and clusters as new features, try LSTM and do preliminary Error Analysis for our problem and define our problem in Survival Analysis. We did more error analysis with single features and the overall classification result in week 12. In week 13, we failed to use survival analysis model and changed to regression.

### Summary of Every Week

#####Week 3

We look through the data and define our problem, brainstorm the solutions and what will be deliverable in week 3:

- Look Through Data and Get a Sense What to Do
  - 2 million users profiles
  - 3 months behavioral log
- Define Problem
  - User Profiling
  - User Retention Prediction: to predict if a user is active, inactive, or at-risk of churning
- Brainstorm Methods and Deliverable Results
  - Methods: 
    - basic EDA
    - user profiling: K-means+PCA
    - user retention: classification+regression
  - Deliverable results
    - Structured User profiles
    - Predicted labels/scores
      - classification+precision,recall,f1-score
      - regression+MAE

#####Week 4

#####Week 5

#####Week 6

#####Week 7

#####Week 8

#####Week 9

#####Week 10

#####Week 11

#####Week 12

#####Week 13

##### Week 14



