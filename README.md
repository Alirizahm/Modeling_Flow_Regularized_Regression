# Modeling Flow Regularized Regression
Author's : Aliriza Hamonangan Matondang
## Instructions
1. Split data: train - validate - test 
2. Draw correlation plot on training data and perform feature selection on
highly correlated features 
3. Fit the models on training data (lambdas = [0.01, 0.1, 1, 10]) 
- Ridge regression
- LASSO
4. Choose the best lambda from the validation set
- Use RMSE as metric
- Interpret a sample of the coefficients of the best model
  - Ridge regression
  - LASSO
5. Evaluate the best models on the test data (+ interpretation)
- MAE
- MAPE
- RMSE

## The results
2. Draw correlation plot on training data and perform feature selection on
highly correlated features
<img width="430" alt="000003" src="https://user-images.githubusercontent.com/92624520/162208648-a8f8c0ab-2a91-4930-86d5-e292c5cbe4bd.png">

Finding:
- The variable that can be dropped is rad because it correlates more than the threshold of 0.8 with tax, however, tax has a higher value than tax when it is viewed from closest to -1 there is madv

3. Fit models on training data (lambdas = [0.01, 0.1, 1, 10])

Findings: 
- There is no significant difference when it is compared to ridge with lasso for all lamda values
- The highest Intercept value is at lamda 10
- Lamda value of 10 on ridge regression & lasso has the same value
- Lamda values of 0.1 and 1 have the same value on ridge regression
- Lamda values 0.1 and 1 have the same value on lasso
- Interpretation of ridge regression & lasso

Ridge Regresion

"ridge_reg_pointzeroone", medv : 2.80 + -7.97 crim + 3.79 zn + -4.10 indus + 2.89 chas + 1.60 nox + 4.51 rm + 5.67 age + -1.31 dis + -2.42 tax + -9.03 ptratio + 6.57 black + -4.77 lstat

An increase of 1 point in the value of the predictor coefficient, while the value of other features remains, will be associated with an increase in the value of the predictor coefficient on medv

"ridge_reg_pointone"
medv : 2.72 + -7.86 crim + 3.68 zn + -4.20 indus + 2.88 chas + -1.51 nox + 4.52 rm + 5.01 age + -1.26 dis + -4.97 tax + -8.93 ptratio + 6.63 black + -4.70 lstat

An increase of 1 point in the value of the predictor coefficient, while the value of other features remains, will be associated with an increase in the value of the predictor coefficient on medv

"ridge_reg_one"
medv : 2.72 + -7.86 crim + 3.68 zn + -4.20 indus + 2.88 chas + -1.51 nox + 4.52 rm + 5.01 age + -1.26 dis + -4.97 tax + -8.93 ptratio + 6.63 black + -4.70 lstat

An increase of 1 point in the value of the predictor coefficient, while the value of other features remains, will be associated with an increase in the value of the predictor coefficient on medv

"ridge_reg_ten"
medv : 21.7 + -0.06 crim + 0.02 zn + -0.08 indus + 2.10 chas + -4.34 nox + 2.88 rm + -0.008 age + -0.19 dis + -0.003 tax + -0.57 ptratio + 0.005 black + -0.24 lstat

An increase of 1 point in the value of the predictor coefficient, while the value of other features remains, will be associated with an increase in the value of the predictor coefficient on medv

Lasso

"Lasso_pointzeroone"
medv : 2.80 + -7.97 crim + 3.79 zn + -4.10 indus + 2.89 chas + -1.60 nox + 4.51 rm + 5.67 age + -1.31 dis + -2.42 tax + -9.03 ptratio + 6.57 black + -4.77 lstat

An increasing of 1 point in the value of the predictor coefficient, while the value of other features remains, will be associated with an increasing in the value of the predictor coefficient on medv

"Lasso_pointone"
medv : 2.72 + -7.86 crim + 3.68 zn + -4.20 indus + 2.88 chas + -1.51 nox + 4.52 rm + 5.01 age + -1.26 dis + -4.97 tax + -8.93 ptratio + 6.63 black + -4.70 lstat

An increasing of 1 point in the value of the predictor coefficient, while the value of other features remains, will be associated with an increasing in the value of the predictor coefficient on medv

"Lasso_one"
medv : 2.72 + -7.86 crim + 3.68 zn + -4.20 indus + 2.88 chas + -1.51 nox + 4.52 rm + 5.01 age + -1.26 dis + -4.97 tax + -8.93 ptratio + 6.63 black + -4.70 lstat

An increasing of 1 point in the value of the predictor coefficient, while the value of other features remains, will be associated with an increasing in the value of the predictor coefficient on medv

"Lasso_ten"
medv : 21.7 + -0.06 crim + 0.02 zn + -0.08 indus + 2.10 chas + -4.34 nox + 2.88 rm + -0.008 age + -0.19 dis + -0.003 tax + -0.57 ptratio + 0.005 black + -0.24 lstat

An increasing of 1 point in the value of the predictor coefficient, while the value of other features remains, will be associated with an increasing in the value of the predictor coefficient on medv

4. Choose the best lambda from the validation set

Finding :
- the best lamda is 0.01 which can be used on the model


5. Evaluate the best models on the test data (+ interpretation)

Findings :

MAE

- The approximate accuracy value of the model is 6.82
- The average error distance between the model and the actual data is 3.89 
- The average percentage of model error with actual data is 17.1%

Lasso

- The approximate accuracy value of the model is 6.82
- The average error distance between the model and the actual data is 3.89
- The average percentage of model error with actual data is 17%
- Based on the evaluation results are not so different, but lasso tends to be better than ridge regression
