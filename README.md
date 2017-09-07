# learn_evaluate_validate

## Confusion matrix

true positives, true negatives, false positives, false negatives

## Accuracy

accuracy = (true positives+true negatives)/total

Both consusion matrix and accuracy are metrics for classification.

## R2 score

R2 score is a measure for regressoin (continuous prediction).

Mean squared error is also a measure for regressoin.

R2 score is based on comparing our model with the simplest possible model. A pretty simple model is to take the average of all the values and draw a horizontal line through them. Then we compare the mean squared error of our model to the mean squared error of this simple model. We substract this fraction from 1, and get the R2 score.

R2 score is often used to evaluate linear regression. For linear correlation analysis, we will have a correlation coefficient called r2 or r (such as pearson correlation coefficient r), and we will also have a line. This line is not the result of linear regression. The loss function for that line is to make the sum of all the euclidean distances from the points to the line the smallest. 

For a 2-dimentional situation, pearson correlation coefficient r is calcualted by covariance(x,y)/(variance(x)*variance(y)). Covariance of x and y is the sum of (x-mean of x)(y-mean of y).

For PCA (principal component analysis), we also need to find a line. The loss function for that line is similar to correlation analysis, making the sum of all the euclidean distances from the points to the line the smallest.

## Type of errors

error due to bias (training error), error due to variance (testing error)

underfit, overfit

## Model complexity gragh

When comlexity is small, both training error and testing error are large, it is underfitting. When complexity is very large, training error is small but testing error is large, it it overfitting.

## Evaluation and validation

Testing data is used for model evaluation, and validation data is used for model validation.

Model validation is to determine hyperparameters. Some hyperparameters are not in the model, such as iteration times and learning rate for gradient descent. Some hyperparameters are in the model, but they are not continuous, such as the number of layers in neural network and the number of nodes in each layer. Therefore, they can not be simply trained in gradient descent.

sklearn中有函数可以用来随机的分配training data, testing data and validation data.

## K-fold cross validation

K-fold cross validation is actually used to evaluate a model or choose the best model from several models, that is, to validate a model. The model that has the smallest average validation error (or testing error) will be chosen.

The data will be randomly splitted into K groups, we will use 1 group as testing data and the other K-1 groups as training data. We will conduct traing and testing K times, and get the average testing error.
