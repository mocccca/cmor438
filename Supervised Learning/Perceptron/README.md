# Perceptron 

## Overview

The perceptron is an algorithm for supervised learning of binary classifiers. A binary classifier is a function that can decide whether or not an input, represented by a vector of numbers, belongs to some specific class.


## How the Perceptron Works

1. **Initialize** weights and bias (often to zeros or small random numbers).
2. For each input vector `x`, compute the weighted sum: prediction = sign(w · x + b)
3. **Compare prediction to actual label**:
- If prediction is correct: do nothing.
- If misclassified:
  ```
  w = w + η * y * x
  b = b + η * y
  ```
  where `η` is the learning rate and `y` is the true label (+1 or -1).
4. **Repeat** for a number of epochs or until convergence.



## Dataset

### Task 1: Gender Prediction from Cabin Preferences

- **Variables:**
- `cabin_teaching_education`
- `cabin_construction_woodwork`
- **Target:**
- `gender` (mapped as `1 = male`, `-1 = female`)
- **Preprocessing:**
- Removed non-binary entries (`gender = 3`) to ensure binary classification.

### Task 2: Behavioral Work-Family Conflict Prediction

- **Variables:**
- `time_wif_composite`
- `strain_wif_composite`
- **Target:**
- `behavior_wif_composite`, binarized as:
 - `1 = low conflict` (scores between 3–9)
 - `-1 = high conflict` (scores between 10–15)



## Tasks

- Apply **Perceptron** to classify:
1. **Gender** from the most "stereotypical" cabin-related preferences.
2. **Behavioral work-family conflict** based on time and strain work-family conflict variables.



## Results & Key Insights

### 🧪 Task 1: Gender Prediction

| Metric                  | Value    |
|-------------------------|----------|
| Accuracy                | 34.5%    |
| Precision (Class 1)     | 33.9%    |
| Recall (Class 1)        | 100.0%   |
| Specificity (Class -1)  | 1.3%     |

**Insight:**  
The model heavily favored predicting class `1` (male), achieving perfect recall but failing to identify females, likely due to class imbalance or a lack of linear separability in the feature space.



### 🧪 Task 2: Behavioral Work-Family Conflict

| Metric                  | Value    |
|-------------------------|----------|
| Accuracy                | 68.6%    |
| Precision (Class 1)     | 80.3%    |
| Recall (Class 1)        | 72.6%    |
| Specificity (Class -1)  | 59.5%    |

**Insight:**  
This model performed substantially better, demonstrating good classification performance for both classes. Indicates potential for linearly separable structure between conflict levels in relation to time and strain.



## Conclusion

The Perceptron works well for some problems, but fails when the classes are not linearly separable or the data is imbalanced. Task 2 is a better fit for this model, while Task 1 may benefit from more complex or nonlinear classifiers.

