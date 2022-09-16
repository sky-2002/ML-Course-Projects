# ML-Course-Projects
This repository includes projects related to ML (also includes those from the course [CS550 Machine Learning](https://github.com/gagan-iitb/CS550), being offered at IIT Bhilai for the 22-23M semester).


## 1. Taxi-Fare prediction.
This project is about the new york city taxi fares dataset and contains various approachs that can be used to predict the taxi fares.
I have done a lot of preprocessing on the dataset as it had a lot of outliers. Also, a lot of exploratory data analysis has been done to analyse features and select the ones which are correlated with the target variable. Also, it is useful to visualize the distributions of our features.

Methods used are:
* Linear Regression (closed form approach)
  - In this, I used the closed form solution of linear regression problem and also applied cross-validation on the training data.
  - I have used this equation $\hat{w} = (A^TA)^{-1}(A^Ty)$ as the closed form solution.

* Non-parametric approach (KNN)
  - Used KNN algorithm on each point in test data and assigned the average of the target variable of its k-nearest neighbors in training data.
  - Analysed the results for different values of k and different distance metrics. The details are presented in the notebook above.
  
* Using Gradient descent
  - I used stochastic gradient descent as the dataset was very large and if I had used batch gradient descent, it would have taken a large amount of time. As    stochastic gradient descent randomly selects a data point in each iteration(instead of the whole batch of data), it is much faster.
  
Details of the above mentioned approaches.<br>
|**Approach used**|**MSE**|**MAPE**|
|-----------------|-------|--------|
|Closed form solution| 0.32|1.06|
|KNN (non parametric)|0.31|1.38|
|SGD|5.41|0.20|

I also came to know that MAPE is a better metric than MSE and hence I chose the SGD model as the best one because it has a low MAPE score.


## 2. Life Expectancy prediction.
In this problem we were to predict the life expectancy given various parameters like country, adult mortality, infant mortality and much more. I used maps and plots to create some interesting visualizations(using which we can infer a lot of things) here. Also, I performed Kolmogorov-Smirnov test to find out which features had a distribution similar to a gaussion one. 

Details of the methods used.<br>
|**Algorithm**|**R2-Score**|**MAPE**|
|-------------|------------|--------|
|Linear regression|0.95|0.017|
|Lasso regression|0.80|0.017|

Lasso was used to perform feature selection(as it assigns a 0 weight to irrelevant features)
