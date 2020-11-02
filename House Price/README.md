<p align="center">
  <img  width="600" height="400" src=images/house_price.jpg>
</p>

# Name
Predicting House Prices: Advanced Regression Techniques

# Data
The data is from Kaggle and the link is https://www.kaggle.com/c/house-prices-advanced-regression-techniques

# Description
This is a Kaggle project that I study for regression analysis. The goal of this project is developing models that have the lowest RMSE(Root-Mean-Square Error). 
According to the Kaggle description, the practice skills are "Creative feature engineering" and "Advanced regression techniques like random forest and gradient boosting".
Like many other kaggle project, this proejct are already solved by many other data scientist. I reference got my source from the posting on this competition, but I built my own
model and understanding for this project.


# Models

<p align="center">
  <img  src=images/process.png>
</p>
First thing that I did was checking label value to see if there are any observation. As you can see the left graph, the target value which is sale price was skewed to left. I applied log transformed to make it normal distribution. 
<p align="center">
  <img  src=images/graph1.png>
</p>
I applied Linear Regression, Ridge, and Lasso model with Cross Value evalution. I visualized the regression coefficient values and column names with top 10 and bottom 10 (the largest 10 as -value. 
<p align="center">
  <img  src=images/graph3.png>
</p>
Once I did that, I tunned the hyper parameter while changing the alpha value of each model, and applied same models. From the first result, I found the lasso model had quite high RMSE value, so I started the alpha value 0.001, 0.005, and so on, which they are quite close and detail alph value. The result was that the RMSE for Lasso regression reduced to similar value with Ridge regression. 
<p align="center">
  <img  src=images/graph4.png>
</p>

# Feature Engineering
### Log Transformed
After checking the data distribution skewness for numeric features, I applied log transformed to the all skewed data and tunned hyperparameter optimization for the alpha value. The below visualization shows the coefficient value for each feature. 
<p align="center">
  <img  src=images/graph5.png>
</p>

### Outlier
After applying log tranformed, I created a graph for the salesprice to see if there was any outlier data. The tow points in red box seemed not related with the all other points,so I found the index of the two points and got rid of the training and testing data.  
<p align="center">
  <img  src=images/graph6.png>
</p>

### Linear Regression Model & Regression Tree Model 

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
