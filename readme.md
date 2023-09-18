This project is about a python package for automated logging and visualization of metrics of classfication and regression algorithms in machine learning.

Features
* The module covers both regression and classification tasks. 
* The module integrates a wide range of metrics related to classification and regression
* The module can provide a barplot of the specified metrics from the specified subset of data
* The module can provide the confusion matrix for all the different ML algorithms


Functions
* Train and log for classification. All the classifiers are trained on the datasets and the results (accuracy, precision, recall, F1) are logged onto a dataframe which is displayed to the user. This function applies around 12 different classification algorithms as mentioned below:-
'svm-linear'
'svm-rbf'
'svm-poly'
'knn'
'naive bayes'
'decision tree'
'random forest'
'adaboost'
'gradient boost'
'xgboost'
'logistic regression'
'bagging classifier'

* Get confusion matrix. This function helps to get the confusion matrices for all the classification algorithms on the specified set (training/validation)

* Display metric plots. This function plots a barplot for the comparative analysis of the classication algorithms on the specified metric and on the specified subset. 

* Train and log for regression. All the regressors are trained on the datasets and the results (mae, mse, msle, median error, mape, max error) are logged onto a dataframe which is displayed to the user. This function applies around 11 different regression algorithms as mentioned below:- 
'linear regression'
'sgd regression'
'ridge regression'
'elastic net'
'decision tree regression'
'random forest regression'
'adaboost regression'
'gradient boost regression'
'xgboost regression'
'bagging regression'
'hist gradient boosting regression'

Syntax

from AutoLogging_ML import AutoLogger

# train_and_log_classification

a= AutoLogger.train_and_log_classification(x_train,x_test,y_train,y_test)
print(a)

a stores the dataframe comprising of all the metric values for the training and validation datasets. 

# get_metric_plots_classification

AutoLogger.get_metric_plots_classification(a,subset='None',metric='None')

returns the barplot of all the algorithms on the mentioned metric and mentioned subset.

subset= 'training' , 'validation'

metric= 'accuracy' , 'precision', 'recall', 'f1', 'msle', 'median absolute error', 'maximum error'

# get_confusion_matrix

AutoLogger.get_confusion_matrix(a,subset='None')

returns the confusion matrix of all the classification algorithms on the specified subset

subset= 'training'. 'validation'

# train_and_log_regression

b= AutoLogger.train_and_log_regression(x_train, x_test, y_train, y_test)

print(b)


b stores the dataframe comprising of all the metric values for the training and validation datasets.

# get_metric_plots_regression

AutoLogger.get_metric_plots_regression(b,subset=None,metric=None)


returns the barplot of all the algorithms on the mentioned metric and mentioned subset.

subset= 'training' , 'validation'

metric= 'mae' , 'mse', 'mape', 'r2', 'msle', 'median absolute error', 'maximum error'