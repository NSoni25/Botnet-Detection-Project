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
