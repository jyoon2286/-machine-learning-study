<p align="center">
  <img width="600" height="400" src = images/fraud.jpg>
</p>

# Name
Credit Card Fraud Detection

# Data
The data is from Kaggle and the link is https://www.kaggle.com/mlg-ulb/creditcardfraud 
# Description
According to Kaggle description, "The datasets contains transactions made by credit cards in September 2013 by european cardholders.
This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions." AS it mentioned in Kaggle, the data is not balanced, so I used three feature engineerings to solve the problem and build the models.  

# Model
The two models that I used are Logistic Regression and LightGBM.

# Feature engineering
* Log<br>
As you can see the graph down below, the amount feature is skwed so I used log to make it normal distribution. 
<p align="center">
  <img  src=images/graph1.png>
</p><br>

* IQR(Inter Quantile Range)<br>
  * The minimum value is specified by subtracting 1.5 * IQR value from the 1/4th quartile, and the maximum value is specified by adding 1.5 * IQR value from the 3/4th quartile.
The values outside the minimum and maximum values are designated as Outliers.<br>
<p align="center">
  <img width="100" height="300" src=images/IQR.png>
</p><br>


* SMOTE(Synthetic Minority Over-Sampling Technique)
  * When learning a data set with an unbalanced distribution of labels, it is difficult to learn a proper type because the number of data with an abnormal label is very small, whereas the number of data with a normal label is very large, so learning is unilaterally biased to a normal label. It is difficult to detect abnormal data properly.
  * SMOTE is that the data is newly multiplied using K-nearest neighborhood, and oversampled.
  * Undersampling vs. Oversampling
  
    * Undersampling
      * Reduced sampling of data sets with many labels to the level of data sets with fewer labels
    * Oversampling
      * Proliferate data sets with few labels to the level of data sets with many labels  
     
 <p align="center">
  <img  src=images/OSvsUS.png>
</p><br>

# Output
|  Feature engineering | ML algorithm  | Percision   | Recall  | ROC-AUC  |
|---|---|---|---|---|
| NA | Logistic Regression | 0.8750  | 0.6149  | 0.9570  |
| NA | LightGBM  | 0.9492   | 0.7568  |0.9797 |
| Log | Logistic Regression | 0.8812  | 0.6014  | 0.9727 |
| Log | LightGBM   |0.9576   | 0.7635  | 0.9786  |
| IQR | Logistic Regression |0.8750   | 0.6712  |0.9743   |
| IQR | LightGBM   | 0.9680  |0.8288   |  0.9831 |
| SMOTE | Logistic Regression | 0.0542  | 0.9247  | 0.9737  |
| SMOTE | LightGBM   |0.9323   |0.8439   | 0.9789  |

The best results are when I get rid of outlier using IQR as feature engineering and LightGBM for ML algorithm, and I use SMOTE as feature engineering and LightGBM for ML algorithm. 


# Reference
* StandardScaler: https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html
* Random oversampling and undersampling: https://machinelearningmastery.com/random-oversampling-and-undersampling-for-imbalanced-classification/#:~:text=Random%20oversampling%20involves%20randomly%20selecting,them%20from%20the%20training%20dataset.
* oversampling and unversampling picture: https://www.kdnuggets.com/2020/01/5-most-useful-techniques-handle-imbalanced-datasets.html
* SMOTE :https://machinelearningmastery.com/smote-oversampling-for-imbalanced-classification/

