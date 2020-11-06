<p align="center">
  <img width="600" height="400" src = images/analysis.jpg>
</p>

# Name
Clustering customer group for online retail data Set

# Data
The data is from UCI Machine Learning Respository and the link is https://archive.ics.uci.edu/ml/datasets/Online+Retail

# Cluster Evaluation

The majority of clustering data sets don't have a suitable data set to compare each other. Also, clustering may look similar to classification, but it differs a lot in character.
Data classification There is a wider collection of data with a wider cluster value, with a more refined leveling clustering within it, even if it finds a hidden separate group and gives meaning to it or belongs to another classification value.
Due to the nature of unsupervised learning, it is difficult to accurately evaluate the performance of any indicator. Nevertheless, silhouette analysis is used as a method of evaluating the performance of clustering.

# Visualization
Evaluation of silhouette coefficients after clustering with K-Means : Data points in groups are overrlaped

<p align="center">
  <img width="600" height="400" src = images/silhouette_kmeans_plot.jpg>
</p>
Visualization after log transformation

<p align="center">
  <img width="600" height="400" src = images/silhouette_kmeans_plot_2.jpg>
</p>

# Output 

# Reference 
* https://scikit-learn.org/stable/auto_examples/cluster/plot_kmeans_silhouette_analysis.html
