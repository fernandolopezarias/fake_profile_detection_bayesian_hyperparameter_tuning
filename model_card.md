# Model Card

## Model Description

**Input:**
The model inputs are features from Instagram user profiles, encompassing both numerical and categorical data. These features include:

1. Presence of a profile picture.
2. Ratio of numbers to the length of the username.
3. Number of words in the full name.
4. Ratio of numbers to the length of the full name.
5. Whether the name matches the username.
6. Description length.
7. Presence of an external URL.
8. Privacy status of the account.
9. Number of posts, followers, and follows.

**Output:**
The model outputs a binary classification indicating whether a profile is likely to be fake (1) or not (0).

**Model Architecture:**
This model utilizes the Random Forest algorithm. Hyperparameter tuning is conducted using the Optuna framework to optimize parameters like the number of trees, max depth of trees, and other relevant settings.

## Performance
**Summary:**
The model's performance was evaluated using metrics such as accuracy, precision, recall, and F1 score. The best model achieved notable accuracy, reflecting its effectiveness in classifying profiles.

**Graph or Metrics:** (Note: A specific summary graph is not provided in the notebook. The following metrics are based on the notebook's reported performance.)

**Accuracy:** High accuracy level (specific value not provided).
Precision, Recall, F1 Score: These metrics are evaluated but specific values are not mentioned. Can be calculated based on the model's confusion matrix.

**Data Analyzed:**
The model was trained and tested on the Instagram dataset with 576 instances, which were split into training and testing sets.

## Limitations
**Sample Size and Diversity:**
The model is trained on a dataset of 576 profiles, which may not be representative of the diverse global Instagram user base.

**Generalization:**
The model's ability to generalize to other social media platforms or varied types of fake profiles is not established.

**Feature Limitation:**
The model is dependent on the dataset's features, which may not capture all aspects of fake profiles comprehensively.

## Trade-offs
**Model Simplicity vs. Complexity:**
While Random Forest is more complex than logistic regression, it strikes a balance between interpretability and the ability to capture nuanced patterns. However, it might still miss certain complex behaviors present in fake profiles.

**Dataset Specificity:**
The model is specifically tuned for the dataset in question, and its performance may vary when applied to data from different time periods or user demographics.

**Bias Potential:**
There is potential for the model to learn biases present in the dataset, which could affect its fairness and accuracy in real-world applications.
