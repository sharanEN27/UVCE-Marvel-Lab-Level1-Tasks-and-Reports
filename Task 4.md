# Task 4 Report
## Linear and Logistic Regression - Coding the model from SCRATCH
### Linear Regression

Implementation of linear regression model on a particular dataset involves various functions. 
The key concepts involved in deriving the linear regression model are as follows

The Cost Function:
Cost function measures how a machine learning model performs. It is the calculation of the error between predicted values and actual values, represented as a single real number.
The difference between the cost function and loss function is as follows:

The cost function is the average error of n-samples in the data (for the whole training data) and the loss function is the error for individual data points (for one training example).
The cost function of a linear regression is root mean squared error or mean squared error. They are both the same; just we square it so that we don’t get negative values.

Given our simple linear equation y=mx+b, we can calculate MSE as:

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/0.png?raw=true)

Gradient Descent:
To minimize MSE we use Gradient Descent to calculate the gradient of our cost function. Gradient descent consists of looking at the error that our weight currently gives us, using the derivative of the cost function to find the gradient (The slope of the cost function using our current weight), and then changing our weight to move in the direction opposite of the gradient. We need to move in the opposite direction of the gradient since the gradient points up the slope instead of down it, so we move in the opposite direction to try to decrease our error.

We can calculate the gradient of this cost function as:

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/1.png?raw=true)

The steps involving in implementation of the linear regression model are as follows:
1. Firstly we create a class LinearRegression. In the init function we set the learning the rate value to 0.001 and number of iterations to default value 1000

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/2.png?raw=true)

2. Now we define a fit method which takes the training samples and labels associated with them and the gradient descent function is implemented in this step as per the formula specified

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/3.png?raw=true)

3. Then the predict method is defined which gets the new test samples 

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/4.png?raw=true)

4. The necessary libraries are imported 

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/5.png?raw=true)

5. The data splitted as training data and testing data
The size value 0.2 indicates that 80% of the samples are used to train the model and the remaining 20% to evaluate or test the model. For this purpose, we use we utilize the scikit learn library's train_test_split()  function as shown

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/6.png?raw=true)

6. The training data and testing data are fit into the dataframe and the test values are predicted

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/7.png?raw=true)

7. The cost function is defined as mse to calculate the mean squared error and the accuracy of the model is calculated

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/8.png?raw=true)

8. The scatter plot is used to visualize the data which has been approximated

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/9.png?raw=true)

### Logistic Regression

Unlike linear regression which outputs continuous number values, logistic regression transforms its output using the logistic sigmoid function to return a probability value which can then be mapped to two or more discrete classes.
Implementation of linear regression model on a particular dataset involves various functions. 

Sigmoid Function:
In order to map predicted values to probabilities, we use the sigmoid function. The function maps any real value into another value between 0 and 1. In machine learning, we use sigmoid to map predictions to probabilities.

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/10.png?raw=true)

Gradient descent:
To minimize our cost, we use Gradient Descent just like before in Linear Regression.

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/11.png?raw=true)

The steps involving in implementation of the linear regression model are as follows:
1. Firstly we create a class LinearRegression. In the init function we set the learning the rate value to 0.001 and number of iterations to default value 1000

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/12.png?raw=true)

2. Now we define a fit method which takes the training samples and labels associated with them and the gradient descent function is implemented in this step as per the formula specified

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/13.png?raw=true)

3. Then the sigmoid function is defined as per the formula specified

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/14.png?raw=true)

4. Then the predict method is defined which gets the new test samples and approximate the values as per a linear model and uses sigmoid function. It predicts 1 if the value is greater than 0.5 and 0 if the value is less than 0.5

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/15.png?raw=true)

5. The necessary libraries are imported and the iris dataset is loaded

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/16.png?raw=true)

6. The data splitted as training data and testing data

The size value 0.2 indicates that 80% of the samples are used to train the model and the remaining 20% to evaluate or test the model. For this purpose, we use we utilize the scikit learn library's train_test_split()  function as shown

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/17.png?raw=true)

7. The training data and testing data are fit into the dataframe and the test values are predicted

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/18.png?raw=true)

8. Lastly the accuracy function is used to obtain the accuracy of the model

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%204%20images/19.png?raw=true)




