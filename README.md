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

**Week 3: Prelimary EDA**

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

**Week 4: EDA**

We look through the data carefully and do some eda, which including:

- Order EDA
- User info EDA

**Week 5: Dataset Making**

We do some feature engineering to create features for our dataset and do retention rate analysis to decide the label of our dataset.

- Feature Engineering (feature) :
  - Daily Features: counts, coupon worth
  - User basic features: user basic information, kitchen basic information
- Retention Rate Analysis (label):
  - Analyze whether rentention in Last Day/Last 5 Days/ Last 7 Days/ Last Two Weeks/ Last Month
  - Decide whether retention or not in last two week as our label

**Week 6: Feature Engineering and Baseline Models**

We read lots of paper this week and did more feature engineering and build baseline model.

- related paper reading:
  - 《Churn prediction of mobile and online casual games using play log data》etc.
- More Feature Engineering:
  - active days, account length, avg, min, max time between two orders etc...
- Baseline Models:
  - predict 0
  - Predict 1
  - random predict
  - Logistic Regression
  - Ridge

**Week 7: Clean Data, Feature Selection and Model Improvement**

We clean data, do some feature selection and do basic transfer to improve data.

- Clean Data:
  - Draw distribution of each variable to fill in NA
  - Transform some category features as binary features
- Feature Selection:
  - Use correlation matrix to see correlationship between features
  - Distribution of each variable
  - Draw pair plot to find highly correlated features
  - Run Random Forest to gain important features
- Model Improvement:
  - drop bot
  - Standard scale
  - log transfer weekly features
  - log transfer most features
  - turn parameters
- Evaluation:
  - Decide use ROC_AUC_SCORE as evaluation

**Week 8: Iteration**

We iterate our model and add more features.

- Feature Engineering:
  - add dummy variable to indicate if it's NA
  - add PCA
  - change coupon worth total to coupon worth avg and max
  - log transform some variables
  - convert some categorical variables into binary variables
- Model Improvement:
  - Add Standard Scale
  - Delete Daily Features
  - Delete Outliers

**Week 9: Iteration 2**

We continue iteration our models and try some non-linear models.

- Feature Engineering:
  - Delete Daily Features
- Preprocessing:
  - Oversample (SMOT)
  - Remove outliers( any value outside mean+- 3 standard divation)
- Model Improvement (Linear->Non-linear):
  - Light GBM Classification
  - Random Forest Classification

**Week 10: Iteration 3**

We read more paper and gain more ideas to improve our current clasification model.

- Related Paper Reading:
  - 《A review of feature selection techniques in bioinformatics》
- Feature Engineering:
  - user_comment/not
  - kitchen features(like like_num, price)
- Feature Selection:
  - Rank ROC scores of model with single feature
  - Compare rankings of features from different models (top 70)
- Model Preprocessing:
  - Bootstrap instead of SMOT

**Week 11 Wrap Up, Prelimary Error Anaysis and Survival Analysis Defination**

We stop iterate our classification model and wrap up our models, did some primary error analysis and read some documents about survival analysis and define our problem.

- Classification Model Wrap Up:
  - Feature Engineering: PCA & Clusters
  - Try LSTM with daily features
  - Stack
- Prelimary Error Analysis:
  - Analyzed users with true label 1 but got predicted to be 0
  - Randomly Choose 5 people and check each order they made
- Survival Analysis:
  - Read documents about survival analysis models: [LIFELINES](<https://lifelines.readthedocs.io/en/latest/>)
  - Define our problem in survival analysis(event, start, end, censored)

**Week 12: Error Analysis**

We mainly did error analysis about our classification problem.

- Single Features Error Analysis
- count plot of every day with FN, FP, TN, TP parts
- coupon sum plot of every day with FN, FP, TN, TP parts

**Week 13: Survival Analysis and Regression**

We did survival analysis and failed to get correct results and then changed our problem to regression problem.

- Survival Analysis: Cox (failed)
- Regression:
  - Models: Ridge\LightGBM\LSTM
  - Evaluation: MAE

**Week 14: Wrap Up and Summarize**

Wrap all things up



