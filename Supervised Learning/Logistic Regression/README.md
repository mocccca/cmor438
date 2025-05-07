## 1. Logistic Regression

### What is Logistic Regression?
Logistic regression is a statistical model for binary classification that predicts the probability of an outcome using a logistic function. Unlike linear regression which outputs continuous values, logistic regression outputs values between 0 and 1, interpreted as class probabilities.

### How It Works:
1. **Input**: Takes numerical/categorical features (X)
2. **Sigmoid Function**: Maps linear combinations of inputs to probabilities: p = 1 / (1 + e^(-(w·x + b)))
3. **Decision Boundary**: Classifies as 1 if p ≥ 0.5, else 0
4. **Optimization**: Uses maximum likelihood estimation to find optimal weights (w) and bias (b)

### Key Properties:
- Handles binary outcomes (e.g., Yes/No)
- Provides interpretable coefficients (log-odds)
- Requires feature scaling for optimal performance

### 2. Data & task

### Dataset
We analyzed workplace survey data with:
- **Target Variable**:
  - `org_status_3` (binary: 1=supervisor, 0=non-supervisor)
- **Predictors**:
  - Demographic: `age`, `education_level`  
  - Behavioral: `ocb_composite` (organizational citizenship behavior)
  - Psychological: `ip_realistic` (realistic dimension in RIASEC)

### Model Development

1. **Preprocessing**:
- Recode categorical variables - mapped education levels to ordinal codes (1-8 → 0-7)
- Standardized features (mean=0, std=1)

2. **Model**: Implemented logistic regression with:
- L2 regularization
- sklearn's `LogisticRegression` class

3. **Evaluation**:
- Accuracy: 72% 
- Confusion matrix analysis
- ROC-AUC: 0.83 (moderate discrimination power)

### Key Findings
- Strongest predictors: OCB scores and realistic work interests
- Education level showed non-linear effects
- Model identified 72% of supervision cases correctly
