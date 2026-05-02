
# Mushroom Classification: Edible vs. Poisonous

## Project Objective
The primary objective of this project is to build a machine learning model capable of accurately classifying mushrooms as either edible or poisonous based on their various physical characteristics. The goal is to achieve high predictive accuracy to assist in identifying safe mushrooms.

## Dataset
The project utilizes a dataset containing 8124 samples and 23 categorical features describing various mushroom attributes (e.g., cap shape, odor, gill color, habitat). The target variable, 'class', indicates whether a mushroom is 'e' (edible) or 'p' (poisonous). The dataset was found to be clean, with no missing values, and the classes were well-balanced.

## Key Steps and Analysis

### 1. Data Loading and Initial Exploration
- The `mushrooms.csv` dataset was loaded and inspected.
- Confirmed 8124 rows and 23 columns, with all features being categorical.
- No missing values were present, ensuring data quality.
- The target variable distribution was approximately 51.8% edible and 48.2% poisonous.

<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20172655.png" />

### 2. Exploratory Data Analysis (EDA) and Feature Engineering
- Cross-tabulations were used to analyze the distribution of each feature against the 'class' variable, identifying highly predictive features.
- **Promising Features Identified**: `odor`, `gill-color`, `spore-print-color`, `bruises`, `stalk-surface-above-ring`, `stalk-surface-below-ring`, and `ring-type` showed strong discriminatory power.
- Visualizations (grouped bar charts) were generated for these promising features to confirm their patterns and distributions across edible and poisonous classes.
- A pie chart was created to visualize the overall distribution of edible vs. poisonous mushrooms.

### 3. Data Preprocessing
- The `veil-type` column was dropped as it contained only one unique value, providing no predictive information.
- The target variable 'class' was numerically encoded: 'e' (edible) to `0` and 'p' (poisonous) to `1`.
- One-hot encoding was applied to all remaining categorical features, transforming them into a numerical format suitable for machine learning algorithms. This resulted in 95 features.
- The dataset was split into training (60%), validation (20%), and test (20%) sets using stratified sampling to maintain class balance.

### 4. Model Training and Evaluation

#### A. Logistic Regression Model
- A Logistic Regression model was initialized and trained on the preprocessed training data.
- **Validation Performance**: Achieved 99.82% accuracy with 0 false positives and only 3 false negatives.
- **Test Performance**: Achieved a perfect 100% accuracy on the unseen test set, with 0 false positives and 0 false negatives, demonstrating excellent generalization capabilities.

#### B. Decision Tree Classifier
- A Decision Tree Classifier was also trained and visualized to provide an interpretable model.
- **Test Performance**: Achieved a perfect 100% accuracy on the test set, with 0 false positives and 0 false negatives.
- The decision tree visualization clearly illustrated the decision rules used by the model.

### 5. Graphs Made Here
- **Grouped Bar Charts**: Visualizations for key distinguishing features such as `odor`, `spore-print-color`, `gill-color`, `bruises`, `stalk-surface-above-ring`, `stalk-surface-below-ring`, and `ring-type` were created to show their distribution across edible and poisonous classes.
- **Confusion Matrices**: Confusion matrices were generated for both Logistic Regression and Decision Tree models on the validation and test sets to visualize classification performance.

<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20173354.png" />
<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20173411.png" />

<img width="630" height="470" alt="Image" src="https://github.com/mnajera06/Kaggle-project/blob/main/Screenshot%202026-05-01%20172608.png" />

### 6. Performance Comparison of the Model Training
Both Logistic Regression and Decision Tree models achieved exceptional performance on this dataset. Their key performance metrics are summarized below:

| Model                  | Validation Accuracy | Test Accuracy | Test Precision | Test Recall | Test F1-Score |
|------------------------|---------------------|---------------|----------------|-------------|---------------|
| Logistic Regression    | 99.82%              | 100%          | 1.00           | 1.00        | 1.00          |
| Decision Tree          | -                   | 100%          | 1.00           | 1.00        | 1.00          |

*Note: The Decision Tree model was only explicitly evaluated on the test set for this summary, but would also show perfect or near-perfect performance on validation given its test performance.*

Both models demonstrated perfect classification on the test set, suggesting the features are highly discriminative for this task. The Decision Tree offers interpretability, while Logistic Regression provides a simple yet powerful linear classification boundary. Given the perfect scores, either model would be highly effective.

## Conclusion
Both the Logistic Regression and Decision Tree models achieved exceptional performance (100% accuracy on the test set) in classifying mushrooms as edible or poisonous. This indicates that the features provided in the dataset are highly effective discriminators. The project successfully built robust models capable of accurate mushroom classification, ready for potential deployment or further analysis.
