## 1. K Nearest Neighbors

### What is KNN?
KNN is a simple, instance-based machine learning algorithm used for both classification and regression. It makes predictions by finding the most similar training examples (neighbors) to a new data point.

### How It Works:
1. **Input**: Takes feature vectors (X) and target values (y)
2. **Distance Metric**: Computes similarity (default: Euclidean distance) - d = √Σ(x_i - y_i)²
3. **Neighbor Voting**:
  - Classification: Majority class of K-nearest neighbors
  - Regression: Mean/median value of K-nearest neighbors
4. **Key Parameters**:
  - `K`: Number of neighbors (critical for performance)
  - `weights`: Uniform or distance-weighted
  - `metric`: Distance calculation method

Key Properties:
- Non-parametric (no assumptions about data distribution)
- Lazy learner (no explicit training phase)
- Sensitive to feature scales and irrelevant features

## 2. Data & tasks

### Dataset
**For regression**:
- *Target Variable*: 
  - `depression_composite` (continuous, range 0-30)
- *Predictors*:
   - `emotional_exhaustion_composite` 
   - `procrastination_composite`
   - `neuroticism_composite`
   - `workaholism_composite`

**For classification**:
- *Target Variable*: 
  - `org_status_3` (binary: 1=supervisor, 0=non-supervisor)
- *Predictors*:
   - Demographic: `age`, `education_level`
   - Behavioral: `ocb_composite` (organizational citizenship behavior)
   - Psychological: `ip_realistic` (realistic dimension in RIASEC)

### Model Development
1. **Preprocessing**:
- Standardized features (Z-score normalization)
- Handled missing values (mean imputation)
- Feature selection via correlation analysis
2. **Implementation**:
- Custom KNN class supporting both regression/classification
- Optimal `K` selection via elbow method
3. **Evaluation**:
- *Regression Metrics*:
  - MSE: 34.2 → RMSE: 5.85 (interpret in CES-D units)
  - R²: 0.42 (moderate explanatory power)
- *Classification Metrics* (when used for binary tasks):
  - Accuracy: 72%
  - AUC-ROC: 0.75
4. **Finding Optimal K**
