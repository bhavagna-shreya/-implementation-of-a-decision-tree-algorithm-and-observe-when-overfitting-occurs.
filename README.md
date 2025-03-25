# -implementation-of-a-decision-tree-algorithm-and-observe-when-overfitting-occurs.
# Decision Tree Classifier: Overfitting vs. Underfitting

## Overview
This project demonstrates how to train and optimize a **Decision Tree Classifier** while addressing **overfitting** and **underfitting** using **hyperparameter tuning** and **Grid Search Cross-Validation**.

## Dataset
The dataset is loaded from `data.npz`, which contains:
- `X`: Feature matrix (4505 samples, 2 features)
- `y`: Target labels

## Dependencies
Make sure you have the following libraries installed:
```sh
pip install numpy matplotlib scikit-learn
```

## Code Explanation
The script follows these steps:

### 1. Load Data
- Loads `data.npz` file.
- Splits data into training and test sets (50-50 split).

### 2. Train Initial Decision Tree (Overfitting Case)
- Uses a **default** `DecisionTreeClassifier`.
- Plots decision surface.
- Typically achieves **100% training accuracy** but **low test accuracy** (overfitting).

### 3. Optimize Decision Tree to Reduce Overfitting
- Limits `max_depth`.
- Sets `min_samples_split` and `min_samples_leaf`.
- Trains and evaluates the model with better generalization.

### 4. Use Grid Search for Best Hyperparameters
- Tests multiple values for `max_depth`, `min_samples_split`, and `min_samples_leaf`.
- Selects the best model using cross-validation.

## Expected Results
| Model | Training Accuracy | Test Accuracy |
|--------|------------------|---------------|
| Default Model | ~1.00 (Overfitting) | ~0.70 |
| Tuned Model | ~0.95 | ~0.75-0.80 |
| Grid Search Model | Optimal | Best generalization |

## Running the Code
Execute the script using:
```sh
python decision_tree_classifier.py
```

## Future Improvements
- Add **feature importance analysis**.
- Try **other models (Random Forest, SVM)** for comparison.
- Visualize **cross-validation scores**.

## Author
- **Bhavagna Shreya Bandaru**


