## 1. Principal Component Analysis

### What is PCA?

Principal Component Analysis (PCA) is a dimensionality reduction technique that transforms correlated variables into a set of uncorrelated components, ordered by how much variance they explain in the data.

### How It Works
1. **Standardization**: Scales features to mean = 0 and variance = 1.

2. **Covariance Matrix**: Computes how variables relate to each other.

3. **Eigendecomposition**: Identifies principal components (PCs) as eigenvectors of the covariance matrix.

4. **Projection**: Transforms original data into the new PC space.

### Key Properties:

- Each PC is a linear combination of original features.
- PCs are orthogonal (uncorrelated) and ranked by explained variance.

### 2. Data & task

### Dataset

_Predictors:_

Big Five Traits: Extraversion, Agreeableness, Conscientiousness, Neuroticism, Openness.

RIASEC Traits: Realistic, Investigative, Artistic, Social, Enterprising, Conventional.

_Target: _

workaholism_composite (continuous).

### Model Development

1. **Preprocessing**:

- Standardized features using StandardScaler.

2. **PCA Implementation**:

- Test out different values of the principle components

3. **Regression Model**:

- Trained LinearRegression on both original features and PCA-transformed data.

### Results Summary

PCA Effectiveness
Metric	Original Features	PCA (6 Components)
Explained Variance	100%	81%
R² (Workaholism)	0.32	0.30
MAE	8.01	8.15

### Key Insights:

- Dimensionality Reduction: PCA retained 81% variance with 6 components (vs. 11 original features).
- Predictive Power: PCA achieved comparable performance (R² = 0.30 vs. 0.32), indicating it preserved most signal.
- Interpretability Tradeoff: PCs are harder to explain but revealed latent patterns (e.g., PC1 = "General Trait Factor").
