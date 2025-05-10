# Neural Networks

## What is Neural Network?
A **multilayer neural network** is a machine learning model that mimics how the human brain processes information through interconnected layers:
Input Layer (8 features)
↓
[Dense Layer (32 neurons, ReLU)]
↓
[Dropout Layer (30% dropout)]
↓
[Dense Layer (16 neurons, ReLU)]
↓
Output Layer (1 continuous prediction)

### How It Learns:
1. **Forward Propagation**: Data flows through layers to make predictions
2. **Loss Calculation**: Measures error (using Mean Squared Error)
3. **Backpropagation**: Adjusts weights to minimize error
4. **Regularization**: Dropout and L2 regularization prevent overfitting


## Dataset 
The model uses these key predictors from the leisure and vocational interest dataset:

| Feature                     | Type          | Expected Relationship |
|-----------------------------|---------------|-----------------------|
| `conscientiousness_composite` | Personality   | Negative (↓ procrastination) |
| `swb_composite`              | Well-being    | Negative              |
| `depression_composite`       | Mental Health | Positive (↑ procrastination) |
| `social_media_composite`     | Behavior      | Positive              |
| `absorption_composite`       | Work Style    | Negative              |

**Target Variable**: `procrastination_composite` (range: 5-25)


## Key Insights
**Strongest Predictors**:
 - `swb_composite` (-8.66): Well-being reduces procrastination
 - `conscientiousness_composite` (-7.36): Self-discipline decreases delays
 - `absorption_composite` (-6.38): Deep focus prevents procrastination

** low R² suggesting the potential overfitting of the model
