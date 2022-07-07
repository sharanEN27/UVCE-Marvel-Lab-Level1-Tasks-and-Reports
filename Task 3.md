# Task 3 Report
## Metrics and Performance Evaluation
### Regression Metrics:
It is necessary to obtain the accuracy on training data, But it is also important to get a genuine and approximate result on unseen data otherwise model is of no use.

So, to build and deploy a generalized model we require to Evaluate the model on different metrics which helps us to better optimize the performance, fine-tune it, and obtain a better result.

If one metric is perfect, there is no need for multiple metrics. To understand the benefits and disadvantages of regression metrics because different evaluation metric fits on a different set of a dataset.

The sklearn.metrics module implements several loss, score, and utility functions to measure regression performance. Some of those have been enhanced to handle the multioutput case: mean_squared_error, mean_absolute_error, explained_variance_score, r2_score and mean_pinball_loss.

The 3 of the most commonly used ones are:

### 1. Mean Absolute Error 

The mean_absolute_error function computes mean absolute error, a risk metric corresponding to the expected value of the absolute error loss or l1-norm loss.

If y^i is the predicted value of the i-th sample, and yi is the corresponding true value, then the mean absolute error (MAE) estimated over nsamples is defined as

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/1.png?raw=true)

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/2.png?raw=true)

### 2. Mean Squared Error

The mean_squared_error function computes mean square error, a risk metric corresponding to the expected value of the squared (quadratic) error or loss.

If y^i is the predicted value of the i-th sample, and yi is the corresponding true value, then the mean squared error (MSE) estimated over nsamples is defined as

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/3.png?raw=true)

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/4.png?raw=true)

### 3. R² score, the coefficient of determination

The r2_score function computes the coefficient of determination, usually denoted as R².

It represents the proportion of variance (of y) that has been explained by the independent variables in the model. It provides an indication of goodness of fit and therefore a measure of how well unseen samples are likely to be predicted by the model, through the proportion of explained variance.

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/5.png?raw=true)

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/6.png?raw=true)

### Classification Metrics:
Classification is about predicting the class labels given input data. In binary classification, there are only two possible output classes. In multiclass classification, more than two possible classes can be present. I’ll focus only on binary classification.

A very common example of binary classification is spam detection, where the input data could include the email text and metadata (sender, sending time), and the output label is either “spam” or “not spam.” (See Figure) Sometimes, people use some other names also for the two classes: “positive” and “negative,” or “class 1” and “class 0.”

The sklearn.metrics module implements several loss, score, and utility functions to measure classification performance. Some metrics might require probability estimates of the positive class, confidence values, or binary decisions values. Most implementations allow each sample to provide a weighted contribution to the overall score, through the sample_weight parameter.

### 1. Accuracy Score

The accuracy_score function computes the accuracy, either the fraction (default) or the count (normalize=False) of correct predictions.

In multilabel classification, the function returns the subset accuracy. If the entire set of predicted labels for a sample strictly match with the true set of labels, then the subset accuracy is 1.0; otherwise it is 0.0.

If y^i is the predicted value of the i-th sample and yi is the corresponding true value, then the fraction of correct predictions over nsamples is defined as

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/7.png?raw=true)

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/8.png?raw=true)

### 2. Cohen’s kappa

The function cohen_kappa_score computes Cohen’s kappa statistic. This measure is intended to compare labelings by different human annotators, not a classifier versus a ground truth.

The kappa score (see docstring) is a number between -1 and 1. Scores above .8 are generally considered good agreement; zero or lower means no agreement (practically random labels).

Kappa scores can be computed for binary or multiclass problems, but not for multilabel problems (except by manually computing a per-label score) and not for more than two annotators.

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/9.png?raw=true)

### 3. Confusion matrix

The confusion_matrix function evaluates classification accuracy by computing the confusion matrix with each row corresponding to the true class (Wikipedia and other references may use different convention for axes).

By definition, entry  in a confusion matrix is the number of observations actually in group , but predicted to be in group . Here is an example:

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/10.png?raw=true)

### 4. Classification Report

The classification_report function builds a text report showing the main classification metrics. Here is a small example with custom target_names and inferred labels:

![](https://github.com/sharanEN27/Marvel-coursework/blob/main/Task%203%20images/11.png?raw=true)
