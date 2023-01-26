# Neural Network Charity Analysis

## Overview 

The purpose of this analysis is to creat a Loan riskprediction model with sufficient performance (accuracy level > 75%).

## Results
### Data preparation

<b> Processing of categirical variables: </b> After removal of 'NAME' and 'EIN' columns, the need for bucketing was identified via inspection of the number of unique values per column. The bucketing has been performed for 'APPLICATION_TYPE' and 'CLASSIFICATION' features wich reduced the number of unique values. The subsequent step was one-hot encoding of above mentioned variables. 

<b> Data split </b> Feature and target data have been split into training and testing sets  for model verification purposes.

<b> Data scaling </b> The data has been normalised using StandardScaler instance to avoid outlier influence on the model performance.

### Model training 
Deep neural network model with two hidden layers and ReLU activation function have been fit on training set and validated on the testing set.

### Results
The results of the abovementioned model are presented below.
<kbd><img src="https://github.com/ArmineKhanan/Neural_Network_Charity_Analysis/blob/main/images/1st_model%20result.png" alt="Model results" title="INITIAL MODEL RESULTS"></kbd>
Now we will try to enhance model accuracy score via optimization.
## Optimization
<b>The first atempt</b> of the optimization, return and bucketing of the 'NAME' variable bettered the accuracy significantly hitting the goal of <b>above 75%</b>.
<kbd><img src="https://github.com/ArmineKhanan/Neural_Network_Charity_Analysis/blob/main/images/optimised_dodel_result.png" alt="Model results" title="OPTIMIZED MODEL RESULTS"></kbd>

We also tried to optimize the model by changing the activation function of hidden layers and introducing bucketting amendments in 'CLASSIFICATION' variable. These also contributed to the accuracy score, but not significantly.

### Saving the results
We leveraged the Keras Sequential model's save method to export the entire model (weights, structure, and configuration settings) to an Hierarchical Data Format (HDF5 Links to an external site.) file as required.

## Summary

Within the challenged we prcessed the data trained the model, checked the performance and make efforts towards its optimization. As a result we managed to significantly enhance 2-layer deep neural network performance by feature addition. 
