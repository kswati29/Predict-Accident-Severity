# Predict-Accident-Severity-
Classification using Gaussian Naive Bayes, SVC and Neural Network algorithm approaches with MCA dimension reduction with performance comparison

## Introduction and Goal
Based on 75,550 personal injury accidents on public roads in UK that are reported to the police, classifying the severity of an accident as severe and non-severe is imperative needing rigorous attempts for effective and workable prevention.
One of the ways to reduce traffic accidents is to conduct an indepth assessment on the historical data that helps understand the factors associated with incident severity.
Providing the information to emergency services would help them evaluate the severity level of accidents, estimate the potential impacts of the casualties, and
ultimately help to improve the road safety. 

This noteboook attempts to identify the factors that correlate with the slight and serious (including fatal) Road Traffic Accident using Kaggle Dataset.
The project is to predict how various features like geographic location, weather conditions, type of vehicles etc. can be used to predict the severity of an accident. 

## Technique and Approach
The project goal is to build a classification model for road accidents in UK to predict the Accident Severity.
In particular, the notebook demonstrates 3 classifiers for data modeling using Naive Bayes, SVM and Neural Network for the task and uses MCA as dimension reduction technique.

Data: Road accidents in UK between 2010 and 2014
Link: https://www.kaggle.com/stefanoleone992/adm-project-road-accidents-in-uk
Dataset: 75550 x 33
Response: 0 : Slight and 1 : Fatal-Serious

A classifier is built using 3 models- Naive Bayes, SVM and Neural Network for the task. There are 2 parts to the process.

1. Data exploration, relevant teachniques from feature engineering, dimension reduction and feature selection are explored and implemented.
2. Data modeling based on Part 1 analysis, comparison of scores and final procedure selection for documentation.
**Metrics : Accuracy**

Overall Approach
We explored various data preparation and machine learning techniques:

**1.Data level**
The various approaches to prepare data explored are explained in brief as we go along. In general, amongst the various approaches tried, we talk about 2 approaches:

**a. Feature selection with Random Forest** at different variabilities (90%, 95%, 98%), with 95% yielding best accuracy scores overall.
**b. Dimension reduction technique with MCA** since the dataset is predominantly categorical with various n_components(5 to 22) with 22 yielding best accuracy scores overall.
Both methods yield comparable results and we demonstrate method 2 here for the project which gives little better accuracy score.

**2.Classifier level**
Since the dataset is large, stratified sampling technique is used with 50-50 train test split.
Various relevant algorithms in classifiers paired with feature selection/reduction techniques were explored for instance, Gaussian, Categorical, Multinomial and Mixed for Naive Bayes, Linear,Poly and Rbf kernel for SVC and shallow and deep network for neural network.
Further, data modeling is done with hyperparameter tuning through k-fold grid search CV for all classifiers and accuracy score is reported on test set.
Threshold tuning(range 0.4 to 0.6) and found 0.55 threshold yielding best results for majority classifiers.

## Results
1. SVM : 0.7575571  
2. Neural Network : 0.7558714  
3. Naive Bayes : 0.7527714
Amongst the classifiers, GaussianNB, poly SVM and Shallow Neural Network classifiers, although comparable but SVM algorithm yields best results overall based on the accuracy metrics.
Therefore, the project demonstrates that using these classification methods can be a useful tool to accurately classify traffic accidents according to their injury severity.
