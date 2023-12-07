# Model Card
## Model Description
**Input:**
The model inputs are features from Instagram user profiles, which include a mix of numerical and categorical data. 

Key features include:
- Presence of a profile picture
- Ratio of numbers to the length of the username
- Number of words in the full name
- Ratio of numbers to the length of the full name
- Whether the name matches the username
- Description length
- Presence of an external URL
- Privacy status of the account
- Metrics like the number of posts, followers, and follows.

**Output:**
The model outputs a binary classification indicating the likelihood of a profile being fake (1) or not (0).

**Model Architecture:**
The model employs the Random Forest algorithm. Hyperparameter tuning is performed using the Optuna framework, optimizing parameters such as the number of trees, max depth of trees, and other relevant settings.

## Performance
**Summary:**
The model demonstrates a high level of accuracy, precision, recall, and F1 score, reflecting its effectiveness in classifying Instagram profiles.

**Metrics:**

- Accuracy: Approximately 91.38%

- Precision: 91% for non-fake profiles (0), 92% for fake profiles (1)

- Recall: 94% for non-fake profiles (0), 89% for fake profiles (1)

- F1 Score: 92% for non-fake profiles (0), 90% for fake profiles (1)

**Data Analyzed:**
The model was trained and tested on the Instagram dataset, featuring 576 instances divided into training and testing sets.

**Confusion Matrix:**

- True Negatives (Non-Fake): 59

- False Positives (Non-Fake classed as Fake): 4

- False Negatives (Fake classed as Non-Fake): 6

- True Positives (Fake): 47

## Limitations
**Sample Size and Diversity:**
Trained on a dataset of 576 profiles, the model may not comprehensively represent the global diversity of Instagram users.

**Generalization:**
The model's ability to generalize to other social media platforms or different types of fake profiles remains untested.

**Feature Limitation:**
Dependence on specific dataset features might limit the model's ability to capture all aspects of fake profile behaviors.

## Trade-offs
**Model Simplicity vs. Complexity:**
Random Forest offers a balance between complexity and interpretability but may not capture extremely nuanced patterns of fake profiles.

**Dataset Specificity:**
While specifically tuned for the current dataset, the model's performance may vary with data from other time periods or demographics.

**Bias Potential:**
There's a possibility of the model learning biases present in the dataset, which could impact its fairness and accuracy in real-world scenarios.
