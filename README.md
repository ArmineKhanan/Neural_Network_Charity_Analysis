# Neural Network Charity Analysis

## Overview 

We are challenged to develop a Loan risk prediction model with sufficient performance (accuracy level > 75%).

## Results
### Data preparation

<b> Processing of categorical variables: </b> First, we removed 'NAME' and 'EIN' columns. We identified the need for bucketing via the inspection of the number of unique values per column. We performed bucketing for 'APPLICATION_TYPE' and 'CLASSIFICATION' features. The subsequent step was the one-hot encoding of the above-mentioned variables.

<b> Data split: </b> Feature and target data have been split into training and testing sets for model verification purposes.

<b> Data scaling: </b> We normalized data using the StandardScaler instance to avoid outlier influence on the model performance.

### Model training 
A deep neural network model with two hidden layers and ReLU activation function has been fit on a training set and validated on the testing set.

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
