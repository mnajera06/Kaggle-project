
#**Mushroom Classification**: Edible vs. Poisonous

###**Overview**

 Challenge:The primary objective of this challenge is to build a machine learning model capable of accurately classifying mushrooms as either edible or poisonous based on their various physical characteristics. The goal is to achieve high predictive accuracy to assist in identifying safe mushrooms.

Approach: The challenge is formulated as a  binary classification task.I started by data loading, inspecting it, cleaning and handeling irrelevent values.The features were then one-hot encoded for the decision tree to handle, and train on.

Summary of the performance: The decision tree was a success and achieved 100% accurecy on the test sets. The confusion matrix and ROC curve even confirm this by showing no false positives or negatives.

## Data
* Type: CSV file with categorical features
* Size: 8124 rows, 23 columns
* Instances: The data was slipt into training 60%, validation 20%, and testing 20%

### Preprocessing / Clean up
* Feature Removal: The veil-type was dropped because it only had one vlaue in it, making it essentially useless.
* One-Hot Encoding: used ti convert categorical features into numerical format, making them suitable for machine learning algorithms. No rescaling was needed as all features became binary (0 or 1) after encoding.


## Data Visualization
The target variable distribution was approximately 51.8% edible and 48.2% poisonous, making the dataset well balanced.
<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20172655.png" />



<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20173354.png" />
<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20173411.png" />

### Findings
- **Grouped Bar Charts**: Visualizations for key distinguishing features such as `odor`, `spore-print-color`, `gill-color`, `bruises`, `stalk-surface-above-ring`, `stalk-surface-below-ring`, and `ring-type` were created to show their distribution across edible and poisonous classes.


### 6. Performance Comparison

| Model                  | Validation Accuracy | Test Accuracy | Test Precision | Test Recall | Test F1-Score |
|------------------------|---------------------|---------------|----------------|-------------|---------------|
| Decision Tree          | 1.00                | 100%          | 1.00           | 1.00        | 1.00          |

<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20172552.png" />
<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20172608.png" />

**Confusion Matrix**: The confusion matrix confirms that the decision tree on the test set had perfect performance, classyfing everything perfectly with no false positives or negatives.

**ROC Curve**: The ROC Curve evaluates the performance of the decision tree. This ROC curve shows that the decision tree was able to correctly classify everything into their repective class, further confirming the confusion matrix.

**Decision Tree**: The decision tree was visualized to showcase its proccess of decision making.

## Conclusion
The Decision Tree model achieved exceptional performance (100% accuracy on the test set) in classifying mushrooms as edible or poisonous. This indicates that the features provided in the dataset are highly effective discriminators.
