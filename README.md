# Logistic-Regression
Logistic regression implementation in python.
<br></br>
In this project, a logistic regression model has been developed for the [Bank Note Authentication Dataset](https://archive.ics.uci.edu/ml/datasets/banknote+authentication) using gradient descent method. Accuracy, Precision, Recall and F-score values have been calculated. L1 and L2 regularisation has been implemented to explore the effect of regularisation on accuracy and magnitude of weights. Feature importance was determined using the final weights obtained.


## Dataset details
- Number of rows: 1372
- Attributes:
    - Variance
    - Skewness
    - Curtosis
    - Entropy
    - Class (Dependent Attribute)

- Sample data points
1. 3.6216, 8.6661, -2.8073, -0.44699, 0 
2. 4.5459, 8.1674, -2.4586, -1.4621, 0 
3. 0.4283, -0.94981 ,-1.0731 ,0.3211, 1 
4. 1.5904, 2.2121, -3.1183, -0.11725, 1


## Methodology

The dataset was normalised (standardised) using Z-score normalisation. The dataset was split into training and testing data using an 80-20 split. Logistic Regression without regularisation, and with L1 and L2 regularisation was carried out and the accuracy, precision, recall and f-score values were calculated for each model. Different weight initialisations (weights initialised to zeroes, weights taken from a normal distrubution, weights taken from a uniform distribution), learning rates, number of iterations and lambda (regularisation parameter) values were tried.

## Results

- For logistic regression without regularisation, with weights initalised to all zeroes, learning rate = 0.8 , number of iterations = 1500, an accuracy of 99.27 and f-score of 99.25 was achieved on the test set. The final weights for this model were (including bias term): <br> </br>
[[-2.277894 ], [-6.41902018], [-6.67073906], [-6.19920365], [ 0.27300584]]
 <br> </br>
- For logistic regression with L1 regularisation, with learning rate = 0.04 , regularisation parameter = 0.02, number of iterations = 1500, an accuracy of 96.00 and f-score of 95.78 was achieved on the test set. The final weights for this model were (including bias term): <br> </br>
[[-1.65585554e-01], [-2.27335876e+00], [-1.70111197e+00], [-1.34845301e+00], [1.33475071e-03]] 
 <br> </br>
- For logistic regression with L2 regularisation, with learning rate = 0.04 , regularisation parameter = 0.04, number of iterations = 1500, an accuracy of 97.09 and f-score of 96.87 was achieved on the test set. The final weights for this model were (including bias term): <br> </br>
[[-0.28227054], [-1.70082037], [-1.21894639], [-0.91768412], [ 0.05752311]]
 <br> </br>


## Conclusion
- Regularisation effectively decreases the magnitude of weights. 
- L1 regularisation shrinks the weight corresponding to the least important feature (Entropy) to zero. 
- In all the models, the magnitude of weights for the first three attributes (Variance, Skewness, Curtosis) are higher than that for the fourth attribute, Entropy. Thus, for unit increase in the value of the first three attributes, the log odds changes by a larger amount. Therefore, Variance, Skewness and Curtosis are more important in classification of bank note images than Entropy.




