## Module 20 challenge

### Supervised Learning

In this challenge,we used techniques to train and evaluate a model based on loan risk.We uses a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

 We read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

Created the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

Split the data into training and testing datasets by using train_test_split.

 wE created and fit a logistic regression model by using the training data (X_train and y_train).

Saved the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

Evaluated the model’s performance by doing the following:

Generating a confusion matrix.

Printing the classification report.

 In the end we wrote  a brief report that includes a summary and analysis of the performance of the machine learning models that we used in this homework.


