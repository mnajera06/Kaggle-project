

<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/UTA-DataScience-Logo.png" />

# **Mushroom Classification**: Edible vs. Poisonous

### **Overview**

**Challenge**:The primary objective of this challenge is to build a machine learning model capable of accurately classifying mushrooms as either edible or poisonous based on their various physical characteristics. The goal is to achieve high predictive accuracy to assist in identifying safe mushrooms.

**Approach**: The challenge is formulated as a  binary classification task.I started by data loading, inspecting it, cleaning and handeling irrelevent values.The features were then one-hot encoded for the decision tree to handle, and train on.

**Summary** of the performance: The decision tree was a success and achieved 100% accurecy on the test sets. The confusion matrix and ROC curve even confirm this by showing no false positives or negatives.


## Data
* Type: CSV file with categorical features
* Size: 8124 rows, 23 columns
* Instances: The data was slipt into training 60%, validation 20%, and testing 20%

### Preprocessing / Clean up
* Feature Removal: The veil-type was dropped because it only had one vlaue in it, making it essentially useless.
* One-Hot Encoding: used it to convert categorical features into numerical format, making them suitable for machine learning algorithms. No rescaling was needed as all features became binary (0 or 1) after encoding.


## Data Visualization
The target variable distribution was approximately 51.8% edible and 48.2% poisonous, making the dataset well balanced.

<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20172655.png" />



<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20173354.png" />
<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20173411.png" />

### Findings
 **Grouped Bar Charts**: Visualizations for key distinguishing features were created to show their distribution across edible and poisonous classes.
*  Odor: Clear disctinction between poisonous and edible as almost 100% of the mushrooms are clearly divided into their respective classes. Making it a very good indicator of poisonous or edible.
*  Ring-type:decent indicator, but does not show a clear dictinction like odor.
* Stalk Surface above ring: Shows a distinction between the two classes but not greatly so.
* Gill color: Decent indicator as some colors are more associated with a class.
* Spore print color: Like odor, this feature shows a clear discintion between poisonous and edible.
* Bruises: While not as good as other indicators, it does show a some dictinction between the two classes.




### Problem Formulation
* Input: The input to the models consists of 95 one-hot encoded binary features representing the physical characteristics of the mushrooms.
* Output: The output is a binary class label: 0 for edible mushrooms and 1 for poisonous mushrooms.
Models:
* Decision Tree Classifier: Used for ability to handle categorical data directly and how simple it is.
Loss, Optimizer, other Hyperparameters: The hyperparameter was 'random_state=42', it also has not cap on its depth .Since I used a decision tree, loss and optimizer doesn't apply here.



### 6. Performance Comparison

| Model                  | Validation Accuracy | Test Accuracy | Test Precision | Test Recall | Test F1-Score |
|------------------------|---------------------|---------------|----------------|-------------|---------------|
| Decision Tree          | 1.00                | 100%          | 1.00           | 1.00        | 1.00          |

<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20172552.png" />
<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-02%20203121.png" />
<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-02%20203533.png" />

**Confusion Matrix**: The confusion matricies confirm that the decision tree on the test and validation set had perfect performance, classyfing everything perfectly with no false positives or negatives.

**ROC Curve**: The ROC Curve evaluates the performance of the decision tree. Both ROC curves show that the decision tree was able to correctly classify everything into their repective class, further confirming the confusion matricies.

**Decision Tree**: The decision tree was visualized to showcase its proccess of decision making.

## Conclusion
* From this it is evident that a decision tree can disern a poisonous mushroom from an edible mushroom from just physical characteristics.
* The Decision Tree model achieved exceptional performance (100% accuracy on the test set) in classifying mushrooms as edible or poisonous. This indicates that the features provided in the dataset are highly effective discriminators.
* Another point to take away is that some characteristics are more helpful than other, like odor and gill color.

## Future Work
* Explore more complex models like Random Forests or Gradient Boosting to see if they offer any benefits beyond interpretability.
* Expand this to more real-life problems, were it can be used to help people quickly identifiy if a mushroom is poisonous or edible.
