# Regularized Linear Models: Controlling Overfitting

## The Core Problem: Overfitting

When models become too complex (like high-degree polynomials), they start memorizing the noise in the training data instead of learning the underlying pattern. This is called overfitting - the model performs excellently on training data but poorly on new, unseen data.

## The Solution: Regularization

Regularization is the technique of **constraining** a model to make it simpler and prevent overfitting. Think of it as putting "guard rails" on your model to keep it from going too wild.

## How Regularization Works for Linear Models

For linear models, regularization works by **constraining the weights** (coefficients) of the features. The key insight is:

- Smaller weights = Simpler model = Less overfitting

## Why Constrain Weights?

1. Prevents Extreme Values: Stops any single feature from having too much influence
2. Encourages Simplicity: Prefers models with many small weights rather than a few large ones
3. Reduces Variance: Makes the model less sensitive to noise in the training data

## The 3 Main Types of Regularized Linear Models

### 1. Ridge Regression (L2 Regularization)

### 2. Lasso Regression (L1 Regularization)

### 3. Elastic Net

### 4. Early Stopping
