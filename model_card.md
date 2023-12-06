# Model Card
## Model Description
**Input:** The model inputs are features of Instagram user profiles. These include numerical and categorical data such as the presence of a profile picture, the ratio of numbers to the length of the username, the number of words in the full name, the ratio of numbers to the length of the full name, whether the name matches the username, description length, presence of an external URL, privacy status of the account, number of posts, followers, and follows.

**Output:** The model outputs a binary classification indicating whether a profile is likely to be fake (1) or not (0).

**Model Architecture:** The model uses logistic regression. Hyperparameter tuning is conducted using the Optuna framework to optimize the regularization strength 'C'.

## Performance
**Summary:** The model's performance was evaluated using metrics like accuracy, precision, recall, and F1 score. The best model achieved an accuracy of approximately 91.74%.

**Graph or Metrics:** (Note: A specific summary graph is not provided in the notebook. The following metrics are based on the notebook's reported performance.)

**Accuracy:** ~91.74%
Precision, Recall, F1 Score: Not explicitly mentioned but can be calculated based on the confusion matrix provided.

**Data Analyzed:** The model was trained and tested on the provided Instagram dataset with 576 instances, split into training and testing sets.

## Limitations
**Sample Size and Diversity:** The model is trained on a relatively small dataset (576 profiles), which may not represent the global Instagram user base.

**Generalization:** The model's ability to generalize to other social media platforms or varied types of fake profiles is not established.

**Feature Limitation:** The model relies on the features provided in the dataset, which may not capture all aspects of fake profiles.

## Trade-offs
**Model Simplicity vs. Complexity:** The use of logistic regression, a relatively simple model, facilitates ease of interpretation and faster training times but might lack the complexity needed to capture more nuanced patterns that more sophisticated models might identify.

**Dataset Specificity:** The model is specifically tuned for the dataset in question. Its performance might degrade when applied to data from different time periods or user demographics.

**Bias Potential:** The model may inadvertently learn biases present in the dataset, which could affect its fairness and accuracy in real-world applications.
