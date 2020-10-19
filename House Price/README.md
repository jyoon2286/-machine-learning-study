<p align="center">
  <img  width="600" height="400" src=images/house_price.jpg>
</p>

# Name
House Prices: Advanced Regression Techniques

# Data
The data is from Kaggle and the link is https://www.kaggle.com/c/house-prices-advanced-regression-techniques

# Description
This is a Kaggle project that I study for regression analysis. The goal of this project is developing models that have the lowest RMSE(Root-Mean-Square Error). 
According to the Kaggle description, the practice skills are "Creative feature engineering" and "Advanced regression techniques like random forest and gradient boosting".
Like many other kaggle project, this proejct are already solved by many other data scientist. I reference got my source from the posting on this competition, but I built my own
model and understanding for this project.


# Model

<p align="center">
  <img  src=images/process.png>
</p>

#Feature Engineering



# Output
|  Feature engineering | ML algorithm  | RMSE |
|---|---|---|
| NA| LinearRegression Cross Value|0.155|
| NA| Ridge Cross Value|0.144|
| NA| Lasso Cross Value|0.198|
| NA| LinearRegression log transformed with optimal alpha value|0.132|
| NA| Ridge log transformed with optimal alpha value|0.124|
| NA| Lasso log transformed with optimal alpha value|0.12|
| Log transformed| LinearRegression log transformed with optimal alpha value|0.128|
| Log transformed| Ridge log transformed with optimal alpha value|0.122|
| Log transformed| Lasso log transformed with optimal alpha value|0.119|
| Anomaly detection| LinearRegression log transformed with optimal alpha value|0.129|
| Anomaly detection| Ridge log transformed with optimal alpha value|0.103|
| Anomaly detection| Lasso log transformed with optimal alpha value|0.1|
||Ridge and Lasso mixed model|0.10008|
||Ridge RMSE|0.103|
||Lasso RMSE|0.10002|
||XGBM and LGBM mixed model|0.101|
||XGBM RMSE|0.107|
||LGBM RMSE|0.101|

The best results was when I apply Regression tree model with Lasso which the RMSE was 0.10002 after feature engineering.  


# Reference
* https://github.com/data-doctors/kaggle-house-prices-advanced-regression-techniques
* https://www.kaggle.com/datajameson/advance-regression-house-price-prediction-top-4
