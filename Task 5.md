# Task 5 Report
# K- Nearest Neighbor Algorithm

The k-nearest neighbors algorithm, also known as KNN, is a non-parametric, supervised learning classifier, which uses proximity to make classifications or predictions about the grouping of an individual data point. While it can be used for either regression or classification problems, it is typically used as a classification algorithm, working off the assumption that similar points can be found near one another.

Regression problems use a similar concept as classification problem, but in this case, the average the k nearest neighbors is taken to make a prediction about a classification. The main distinction here is that classification is used for discrete values, whereas regression is used with continuous ones. However, before a classification can be made, the distance must be defined.

In order to determine which data points are closest to a given query point, the distance between the query point and the other data points will need to be calculated. These distance metrics help to form decision boundaries, which partitions query points into different regions

Euclidean distance: This is the most commonly used distance measure, and it is limited to real-valued vectors. Using the below formula, it measures a straight line between the query point and the other point being measured.

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/1.png?raw=true)

For classification: A class label assigned to the majority of K Nearest Neighbors from the training dataset is considered as a predicted class for the new data point.

For regression: Mean or median of continuous values assigned to K Nearest Neighbors from training dataset is a predicted continuous value for our new data point.

At low K values, there is overfitting of data/high variance. Therefore test error is high and train error is low. At K=1 in train data, the error is always zero, because the nearest neighbor to that point is that point itself. Therefore though training error is low test error is high at lower K values. This is called overfitting. As we increase the value for K, the test error is reduced.

## Implement KNN using sci-kit’s neighbors.KNeighborsClassifier for multiple suitable dataset

The steps involved in implementing scikit learn library are as follows:
1. Initially the libraries required are imported

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/2.png?raw=true)

2. The iris dataset is loaded from the Iris.csv file stored in the location

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/3.png?raw=true)

3. All the features and their values can be displayed as shown

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/4.png?raw=true)

4. Since the species has many null values it cannot be considered for training and testing. Hence except that column and its values the rest are considered and stored in x

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/5.1.png?raw=true)

5. The species column with names are considered and stored in y

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/6.png?raw=true)

6. To locate the data point in multidimensional feature space, it would be helpful if all features are on the same scale. Hence normalization or standardization of data will help

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/7.png?raw=true)

7. The data splitted as training data and testing data
The size value 0.3 indicates that 70% of the samples are used to train the model and the remaining 30% to evaluate or test the model. For this purpose, we use we utilize the scikit learn library's train_test_split()  function as shown

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/8.png?raw=true)

8. The accuracy function is used to calculate the accuracy of the model

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/9.png?raw=true)

9. The confusion matrix is imported from the library and gives us an idea about which of the values are not classified properly

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/10.png?raw=true)

## Implement KNN from scratch. Compare results with sci-kit’s built in method for different datasets.

Implementation of KNN algorithm from scratch involves the following steps:

1. The euclidean_distance function is defined which computes the distances from a specific as described in the formula 

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/11.png?raw=true)

2. The KNN class is defined. It consists of fit, predict and _predict method. The fit method stores the training samples. The predict method stores multiple samples of data whereas the _predict method takes only one data sample. _predict method computes the distances and gets the k nearest samples and also the most common class label. 

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/12.png?raw=true)

3. The necessary libraries are imported which are required for the implementation of the model and the iris dataset is loaded from the datasets. X and y have the data values and target values respectively

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/13.png?raw=true)

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/14.png?raw=true)

4. The data splitted as training data and testing data
The size value 0.2 indicates that 80% of the samples are used to train the model and the remaining 20% to evaluate or test the model. For this purpose, we use we utilize the scikit learn library's train_test_split()  function as shown

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/15.png?raw=true)

5. The data is then fit into the data frame and the accuracy is calculated

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%205%20images/16.png?raw=true)

When compared both the models are returning approximately the same value
