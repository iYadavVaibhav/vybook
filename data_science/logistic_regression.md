---
layout: post
title: Machine Learning - Logistic Regression Theory
categories: notes machineLearning
last_modified_at: 2019-07-14 11:19:55
---
# Logistic Regression
Logistic Regression is mainly used when we have to work on probability. It outputs values between 0 and 1. So 0.5 is cutoff point and anything below 0.5 goes to class 0 and rest to class 1.

Logistic is also called **Sigmod**. Shown in function below.

$$
\phi (z) = \frac{1}{1 + e^{-z}}
$$

this always outputs b/w 0 and 1.

### Difference between logistic and linear equations

**linear model:**  $ y = b_0 + b_1x $

where as logistic is shown in equation below (also same as $\phi (z)$ eq above) :

$$
p = \frac{1}{1 + e^{-(b_0 + b_1 x)}}
$$


### Model Evaluation

Use **confusion matrix** to evaluate classification model.

Classifiaction model is when we classify our predisctions against test data.

Confusion matrix puts predictions and tests together to compare.

n=165 | Predicted=NO | Predicted=YES | 
--- | --- | --- | ---
Actual: NO | TN = 50 | FP = 10 | 60
Actual: YES | FN = 5 | TP = 100 | 105
 | 55 | 110 | 

False Positive FP is Type 1 error
FN is Type 2 error

### Accuracy:

**Correct:** (TP + TN) / total = 150/165 = 0.91

Our model is 91% correct,

**Wrong:** (FP + FN)/100 = 15/165 = 0.09

Our mode is 9% wrong.


