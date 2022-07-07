# Task 1 Report
# Linear and Logistic Regression - HelloWorld for AIML
## 1. Linear Regression - Predict the price of a home, based on multiple different variables.Use sci-kit’s *linear_model.LinearRegression()*

Linear regression is one of the most popular machine learning algorithms. It is a statistical method that is used for predictive analysis.

Linear regression algorithm shows a linear relationship between a dependent (y) and one or more independent (x) variables, hence called as linear regression.

The software used for implementing the algorithm is Jupyter Notebook using python
For predicting the house prices of the boston dataset some of the standard built in python libraries have to be imported. They are numpy, pandas, seaborn, matplotlib and scikitlearn as sklearn.

NumPy is a very popular python library for large multi-dimensional array and matrix processing, with the help of a large collection of high-level mathematical functions 

Pandas is one of the tools in Machine Learning which is used for data cleaning and analysis. It has features which are used for exploring, cleaning, transforming and visualizing from data.

Seaborn is a plotting library that offers a simpler interface, sensible defaults for plots needed for machine learning

Matplotlib is a data visualization library that is used for 2D plotting to produce publication-quality image plots and figures in a variety of formats

Scikit learn is one of the most important libraries required for implementing machine learning algorithms. It provides a selection of efficient tools for machine learning and statistical modeling including classification, regression, clustering and dimensionality reduction via a consistence interface in Python.

The steps involved in implementing the model are as follows:

1. Initially the libraries are imported

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/1.png?raw=true)

2. The Boston housing price data is loaded from the datasets. The target contains the prices of the houses feature_names contain the names of all the features in the dataset (except target variables).
Before moving on to the next step, the data is checked for any missing values i.e the null values.
There are no missing values in the dataset

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/2.png?raw=true)

3. The data splitted as training data and testing data
The size value 0.2 indicates that 80% of the samples are used to train the model and the remaining 20% to evaluate or test the model. For this purpose, we use we utilize the scikit learn library's train_test_split()  function as shown

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/3.png?raw=true)

4. Scikit learn's LinearRegression() is used to train our model on both the training and test sets

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/4.png?raw=true)

5. This step is to determine whether the model is overfitting or not. Overfitted models perform well on test datasets but do not predict well on real-world datasets
The root mean squared error(rms) and R2 score is used to assess the overfitting. The R2 score is of both training and testing data are almost equal to one. Hence the model is not overfitting

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/5.png?raw=true)

6.Finally the actual prices vs predicted prices are visualized using scatter plot

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/6.png?raw=true)

## 2. Logistic Regression - Train a model to distinguish between different species of the Iris flower based on sepal length, sepal width, petal length, and petal width

Logistic Regression is a supervised classification algorithm. Logistic regression measures the relationship between one or more independent variables (X) and the categorical dependent variable (Y) by estimating probabilities using a logistic(sigmoid) function. Linear regression is not used for classification. Classification needs probability belonging to the class, and it should be in the range between 0 and 1, while linear regression does not bound the predicted probability outcome in range. The logistic/sigmoid function is used because of its behaviour of compressing the output between 0 and 1.

The steps involved in implementing the model are as follows:

1. Initially the libraries are imported

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/1.1.png?raw=true)

2. The iris dataset is loaded from the Iris.csv file stored in the location

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/1.2.png?raw=true)

3. The four features, SepalLength, SepalWidth, PetalLength, and PetalWidth. The last feature, 'Species,' is the target feature we will predict

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/1.3.png?raw=true)

4. Before moving on to the next step, the data is checked for any missing values i.e the null values

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/1.4.png?raw=true)

There are no missing values in the dataset

5. The facegrid from seaborn library is used visualize the Petal length vs Petal width for and Sepal length vs Sepal width for different species

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/1.5.png?raw=true)


6. All the data excluding the ID and species are taken as training and testing data 

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/1.6.png?raw=true)

7. The data splitted as training data and testing data.
The size value 0.2 indicates that 80% of the samples are used to train the model and the remaining 20% to evaluate or test the model. For this purpose, we use we utilize the scikit learn library's train_test_split()  function as shown

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/1.7.png?raw=true)


8. Scikit learn's LogisticRegression() is used to train our model on both the training and test sets. The accuracy_score function imported from metrics library is used to calculate the accuracy of the model

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%201%20images/1.8.png?raw=true)
