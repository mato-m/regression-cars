# Car price regression models

This repo shows the usage of two regression models in predicting the car prices based on different parameters.

Linear regression and random forest regressor are both used and their performance on this dataset is compared.

#### Dataset
The [dataset](https://www.kaggle.com/datasets/doaaalsenani/usa-cers-dataset) was downloaded from Kaggle.
It has 2499 rows and 12 columns. To predict the price of the car we can use only three other columns,
which are model, year and mileage. Since model is in form of a string, it needs to be converted to a number.
It was converted to a number using Ordinal Encoder, which encodes every unique string to an ordinal number.

We only consider cars that do not have "Salvage insurance" as their title status. By examining the
histograms we can see that a small portion of values are significantly distant from the center.
We can ignore these extreme values.

#### Linear regression

Linear regression is the simplest form of regression that aims to find the line that has a minimal
distance from each data point in the dataset.
Linear regression is represented as a linear equation of input values.
Root Mean Squared Error (RMSE) of Linear regression for this dataset was 6863.62.
This means that on average the distance between the actual price and the one that
linear regression line predicts is 6863.62.

#### Random forest regressor

Random forest is an ensemble learning algorythm, which means it uses the results of multiple
machine learning models in order to achieve the best accuracy. Random Forest combines a large
number of decision tree models in order to get the best possible model accuracy. It is often used
as both a classifier and a regressor. Root Mean Squared Error (RMSE) of 
Random forest regressor for this dataset was 1426.38. This means that random forest regressor
achieved much higher accuracy that the linear regression model.
