# Predicting Qmatic Service Levels

The Department of Building on average serves approximately 1100 customers a day who obtain permits and other documents for building construction. The objective of this analysis is to predict high average wait times for customer to obtain their documents. 

Data: ~ 2,000,000 Qmatic transactions from October 2016 through December 2018

Target variable: High wait time greater than or equal to 25 minutes.

Features: Daily staff working hour, number of staff, transactions and unique customers, season dummy variable, daily weather data (average temperature, snow, rain), delivered service categories.

Modeling: A number of classification models were implemented to determine which performed better. The models included decision trees, random forests, gradient boosted decision trees, logistic regress, support vector machines, Naïve Bayes and K-nearest neighbors.

Random forests produced the most accurate results:
5-fold cross valuation accuracy: 0.832
Training accuracy: 0.86
Testing accuracy: 0.85
AUC: 0.82

Based on the random forest analysis, these features were determined to be good predictors:
Season Fall (Sept, Oct and Nov): 8 times more likely compared to other seasons 
Number of customers greater than 1260
Number of service category Fast App transactions greater than 260
Number of delivered service AP Pro Cert Filing transactions greater than 90

Plots

![average waiting time seconds](https://user-images.githubusercontent.com/11237613/51345028-fa038880-1a67-11e9-9b93-0e86de52cc3e.png)

![time series of waiting time october 2017](https://user-images.githubusercontent.com/11237613/51345111-2e774480-1a68-11e9-9548-b0ce3de87de4.png)
