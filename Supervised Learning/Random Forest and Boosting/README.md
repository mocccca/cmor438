# Procrastination Prediction with Random Forest & Gradient Boosting


## Project Overview
Predicts procrastination levels (5-25 scale) using psychological/behavioral features with two ensemble methods.

### Random Forest
**Definition**: An ensemble learning method that builds a large collection of decision trees and aggregates their predictions.  
For regression tasks, the final prediction is the average of all trees’ outputs.
**Steps**:
1. Build multiple trees using random subsets of data (bootstrap sampling)
2. At each split, consider only a random subset of features
3. Average predictions from all trees (for regression)
4. Natural feature importance via split improvement tracking

### Gradient Boosting
**Definition**: An ensemble method that builds a strong predictor by sequentially combining multiple weak models (usually shallow decision trees), where each new model focuses on correcting the errors of the previous ones.
**Steps**:
1. Start with a simple prediction (e.g., mean target value)
2. Calculate residuals (actual - predicted)
3. Build a tree to predict these residuals
4. Update predictions with a learning rate (e.g., 0.1)
5. Repeat for specified number of trees

## Key Insights
1. **Random Forest outperformed Gradient Boosting**, achieving 53% variance explained (R²=0.53) versus 40%.  
2. **Well-being (swb_composite) is the strongest predictor**, explaining 22.6% of procrastination variation.  
3. **Personality traits (conscientiousness, dedication) matter more than behavior** (social media use) in predicting procrastination.  
