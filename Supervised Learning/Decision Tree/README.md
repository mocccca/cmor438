# Decision Tree Analysis for Psychological Predictions

## Overview
Decision trees are versatile ML models that make predictions by learning hierarchical decision rules from data. Key features:
- **Regression Trees**: Predict continuous values (e.g., depression scores) by averaging leaf node samples  
- **Classification Trees**: Predict classes (e.g., supervisor status) using majority voting in leaves  
- **Interpretability**: Rules can be visualized as a flowchart  
- **Non-parametric**: No assumptions about data distributions  

### How It Works
1. **Splitting**: Recursively partitions data using the feature/value that maximizes information gain  
   - Regression: Minimizes MSE  
   - Classification: Minimizes Gini impurity/entropy  
2. **Stopping**: Halts when max depth is reached or no significant gain  
3. **Prediction**: Traverses tree rules to reach a leaf node  


## 📊 Dataset & Tasks
### A. Regression: Predicting Depression Scores
**Features**:  
`emotional_exhaustion_composite`, `procrastination_composite`, `workaholism_composite`, `neuroticism_composite`, `general_js_composite`, `global_js_composite`  
**Target**:  
Continuous `depression_composite` (range 0-30)  

**Preprocessing**:  
- Handled missing values (`dropna()`)  
- Standardized features (Z-score normalization)  

### B. Classification: Identifying Supervisors
**Features**:  
`age`, `ocb_composite`, `ip_realistic`, `education_level` (ordinal 1-8)  
**Target**:  
Binary `org_status_3` (0=Non-supervisor, 1=Supervisor)  

**Preprocessing**:  
- Class balancing (`class_weight='balanced'`)  
- Ordinal encoding for education  



## Key Insights
### Regression Results (R² = 0.39)
- **Moderate explanatory power** - Model explains 39% of depression score variance  
- **Top predictors**:  
  1. Emotional exhaustion (Gini importance = 0.48)  
  2. Procrastination (0.31)
 
### Classification Results (Accuracy = 72%)
- **High recall for non-supervisors (1.00)** - Correctly identifies all true non-supervisors
- **Low recall for supervisors (0.36)**:  Misses 64% of actual supervisors
  1. Emotional exhaustion (Gini importance = 0.48)  
  2. Procrastination (0.31)  
