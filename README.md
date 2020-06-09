# group-project-group-l
group-project-group-l created by GitHub Classroom

#### SMOTE technique

Created data_all by combining the two datasets that were available as it is i.e. imbalanced data, scenarios for a device being detected with a  botnet. Split the data into training and test dataset and applied SMOTE on the training data.

## FEATURE SELECTION USING EMBEDDED METHOD

The reason we choose embedded method was because they are iterative in a sense that the model training process. Regularization techniques are more most commonly used in these techniques,lassoCV regularization is the basic of all the embedded methods.

# Correlation between features

Correlation technique to find out whether there is any relationship exist between the features, the correlation will help us to analyze data at more deep level.

Correlation we have find strong positive relation and negative relations.Below are some examples:

1)max_active and duration are weekly positive correlated to each other.The diagonal formed is a thin but it is not very much to neglect that value.

2.)max_active and std_bkptl are negative correlated to each other but duration and std_bkptl has positive relation.

3.)std_active and max_active has strong positive coorelation and std_active and duration has week positive realtion.

Pairplot and confusion matrix are used to visualize the relationship between the variable.


# Implementing different Modelling technique to calculate accuracy score, confusion matrix,precision value.


## train_test_split function:

The function will split the data into training and testing dataset.Training dataset is used for building the model and testing dataset is to using the model on different model to predict its performance.

## Accuracy_score

Accuracy_score is used to calculate accuracy of the model.Accuracy is defined to calculate no of correct predictions to the total no of predictions.Higher the value of accuracy score, gives more confident to the model to predict the correct output.


## confusion_matrix

confusion matrix is used to evaluate the quality of the output of a classifier on the data set.The diagonal values represents those number of points for which classifier has predicted the true label, while off-diagonal values are those that are not predict by the classifier. The higher the diagonal values of the confusion matrix the better is our model is.

## precision value

Precision is defined as the number of true positives values divided by the number of true positives plus the number of false positives values.


## BernoulliNB Training

Our data is categorical data, we need to detect on which IP server botnet is detected, so we are applying BernoulliNB technique and calculate the confusion matrix, accuracy score and precision value on test data set.

## Decision Tree

It is a technique that builds classification model in the form of tree like structure.It is used to specify the sequence of decision and consequences.

## KNN Classifier

It falls under supervised learning and is used for classification and regression when we know the attributes of the data. We classfiy a point depending upon the nearest neighbor values. It was found that the model predicts best when the k value is 3.

## NEURAL NETWORK : MULTILAYER PERCEPTRON 

A multilayer perceptron (MLP) is a feedforward artificial neural network that generates a set of outputs from a set of inputs. An MLP is characterized by several layers of input nodes connected as a directed graph between the input and output layers. MLP uses backpropogation for training the network.

## Accuracy Score and t-test

Accuracy score is calculated using cross_val_score which calculates a range of the output depending upon the number of folds. Highest score range was observed to be in KNN classifier. Two sided hypothesis test was applied considering the significance level as 0.05. If the significance level greater than 0.05 then we do not reject the hypothesis test and our results are valid.

## comparision between various model and choosing the final file 
 now we have decided that we need to use decission tree for the project and we made a prediction file with random values 
 and tested it.




