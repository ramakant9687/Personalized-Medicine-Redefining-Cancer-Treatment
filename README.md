# Personalized-Medicine-Redefining-Cancer-Treatment
To detect type of mutation in a gene using gene, variation and text by the help of various Machine Learning Algorithms.
Description
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/



Machine Learning Problem Formulation
Data
Data Overview
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/data
We have two data files: one conatins the information about the genetic mutations and the other contains the clinical evidence (text) that human experts/pathologists use to classify the genetic mutations.
Both these data files are have a common column called ID
Mapping the real-world problem to an ML problem
Type of Machine Learning Problem
There are nine different classes a genetic mutation can be classified into => Multi class classification problem

Performance Metric
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment#evaluation

Metric(s):

Multi class log-loss
Confusion matrix
Machine Learing Objectives and Constraints
Objective: Predict the probability of each data-point belonging to each of the nine classes.

Constraints:

Interpretability
Class probabilities are needed.
Penalize the errors in class probabilites => Metric is Log-loss.
No Latency constraints.
Train, CV and Test Datasets
Split the dataset randomly into three parts train, cross validation and test with 64%,16%, 20% of data respectively

Exploratory Data Analysis
Reading Data
Reading Gene and Variation Data
Reading Text Data
Preprocessing of text
Test, Train and Cross Validation Split
Splitting data into train, test and cross validation (64:20:16)
Distribution of y_i's in Train, Test and Cross Validation datasets
Prediction using a 'Random' Model
In a 'Random' Model, we generate the NINE class probabilites randomly such that they sum to 1.

Univariate Analysis
Univariate Analysis on Gene Feature
Machine Learning Models
Base Line Model
Naive Bayes
K Nearest Neighbour Classification
Logistic Regression With Class balancing Without Class balancing
Linear Support Vector Machines
Random Forest Classifier
Hyper paramter tuning (With One hot Encoding)
Hyper paramter tuning (With Response Coding)

Stack the models
Log loss (train) on the stacking classifier : 0.5386754023282136 Log loss (CV) on the stacking classifier : 1.138717562146062 Log loss (test) on the stacking classifier : 1.1742087492677697 Number of missclassified point : 0.38646616541353385

Maximum Voting classifier
Log loss (train) on the VotingClassifier : 0.8329702627479129 Log loss (CV) on the VotingClassifier : 1.1887678593349613 Log loss (test) on the VotingClassifier : 1.2061284826287209 Number of missclassified point : 0.3849624060150376

Logistic regression with CountVectorizer Features, including both unigrams and bigrams
Log loss : 1.1025061826224287 Number of mis-classified points : 0.36278195488721804

adding Variation Feature,Text Feature to improve the performance
Log loss : 0.9976654523552164 Number of mis-classified points : 0.3233082706766917

Conclusion
After some feature engineering we manage to decrease the log loss below < 1.
We can adopt more feature enginnering methods and reduce the log loss furhermore.
