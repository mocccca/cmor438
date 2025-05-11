# Linear Regression

## Overview

Linear Regression is one of the most widely used statistical and machine learning techniques for modeling the relationship between a dependent variable (target) and one or more independent variables (predictors). It assumes that this relationship can be described with a straight line (or a hyperplane in higher dimensions).

In its simplest form: y = β₀ + β₁x₁ + ε

Where:
- `y` is the predicted value (dependent variable)
- `x₁` is the predictor (independent variable)
- `β₀` is the intercept
- `β₁` is the coefficient
- `ε` is the error term

In multiple linear regression, this generalizes to: y = β₀ + β₁x₁ + β₂x₂ + ... + βₙxₙ + ε




## How it works?

1. **Select Variables**: Choose the predictors (X) and the outcome variable (y).
2. **Fit the Model**: Use Ordinary Least Squares (OLS) to estimate the coefficients (βs) that minimize the residual sum of squares.
3. **Make Predictions**: Plug the values of X into the learned equation to get predicted y.
4. **Evaluate Performance**:
   - R²: Proportion of variance explained
   - Adjusted R²: Adjusted for number of predictors
   - MAE, RMSE: Measure prediction error
5. **Refine Model**: Remove redundant variables or add relevant ones to improve accuracy and interpretability.



## Dataset & Task

**Goal**: Predict depression scores using psychological and job-related predictors.


### Variables used
**Predictors**
'emotional_exhaution_composite',
'procrastination_composite',
'workaholism_composite',
'neuroticism_composite',
'general_js_composite',
'global_js_composite'

**Target**
'depression_composite'

## Key Insights

- **Workaholism and neuroticism improved predictions** beyond emotional exhaustion and procrastination.
  - Aligns with psychological theory (e.g., neuroticism = core risk factor for depression).
- **Job satisfaction variables were redundant** and did not add explanatory value.
  - Their removal **improved model efficiency** and reduced overfitting risk.
- **Linear regression was effective**, explaining over 56% of variance in depression with just 4 predictors.

