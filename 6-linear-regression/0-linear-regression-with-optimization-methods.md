# Linear Regression

## Overview

Linear Regression is a fundamental supervised machine learning algorithm used for predicting continuous target values based on one or more input features. It models the relationship between variables by fitting a linear equation to observed data.

## Mathematical Formulation

### Basic Linear Equation

The simple linear regression model makes predictions using:

`ŷ = θ₀ + θ₁ × x₁`

Where:

- `ŷ` = predicted value (target variable)
- `θ₀` = bias term or intercept
- `θ₁` = weight/coefficient for feature x₁
- `x₁` = input feature value

### Multiple Linear Regression

For datasets with multiple features, the model extends to:

`ŷ = θ₀ + θ₁x₁ + θ₂x₂ + ⋯ + θₙxₙ`

Where:

- `n` = number of features
- `xᵢ` = i-th feature value
- `θⱼ` = j-th model parameter (θ₀ is bias, θ₁ to θₙ are feature weights)

### Vectorized Notation

The model can be expressed compactly using vector notation:

`ŷ = hθ(x) = θ · x`

Where:

- `θ` = parameter vector [θ₀, θ₁, θ₂, ..., θₙ]
- `x` = feature vector [1, x₁, x₂, ..., xₙ] (with x₀ = 1 for the bias term)
- `·` = dot product operator

### In matrix form:

`ŷ = θᵀx`

Where θᵀ is the transpose of the parameter vector.

## Cost Function: Mean Squared Error (MSE)

### Definition

The Mean Squared Error measures the average squared difference between predicted and actual values:

`MSE(θ) = (1/m) × Σ(θᵀx⁽ⁱ⁾ - y⁽ⁱ⁾)²`

Where:

- `m` = number of training examples
- `θᵀx⁽ⁱ⁾` = prediction for i-th instance
- `y⁽ⁱ⁾` = actual value for i-th instance
- `Σ` = sum from i=1 to m

### Why MSE?

- **Differentiable**: Smooth function suitable for gradient-based optimization
- **Emphasizes large errors**: Squaring penalizes larger errors more heavily
- **Consistent optimization**: Minimizing MSE yields same parameters as minimizing RMSE

## Practical Example: House Price Prediction

### Scenario

Predict house prices based on:

- `x₁`: Size (square feet)
- `x₂`: Number of bedrooms

### Model Equation

`price = θ₀ + θ₁ × size + θ₂ × bedrooms`

### Trained Parameters

Suppose we obtain:

- θ₀ = 50,000 (base price)
- θ₁ = 200 (price per square foot)
- θ₂ = 10,000 (price per bedroom)

### Prediction Example

For a 1500 sqft house with 3 bedrooms:

price = 50,000 + 200 × 1500 + 10,000 × 3
= 50,000 + 300,000 + 30,000
= 380,000

## MSE Calculation Example

### Sample Training Data

| Instance | Actual Price (y) | Predicted Price (ŷ) | Error (ŷ - y) | Squared Error |
| -------- | ---------------- | ------------------- | ------------- | ------------- |
| 1        | 300,000          | 280,000             | -20,000       | 400,000,000   |
| 2        | 500,000          | 520,000             | 20,000        | 400,000,000   |
| 3        | 400,000          | 390,000             | -10,000       | 100,000,000   |

### MSE Calculation

MSE = (400,000,000 + 400,000,000 + 100,000,000) / 3
= 900,000,000 / 3
= 300,000,000

`RMSE = √300,000,000 ≈ 17,320`

## Training Process

### Objective

The goal is to find the parameters θ = [θ₀, θ₁] that minimize the Mean Squared Error (MSE) cost function:

`θ* = argmin(MSE(θ))`

- θ₀ (intercept) and θ₁ (slope) together define the regression line.
- The objective is to determine the optimal θ that provides the best fit line for the data.
- A well-optimized θ avoids both underfitting (too simple) and overfitting (too complex).

### Optimization Methods

1. **Normal Equation**

   - Closed-form analytical solution
   - Directly computes optimal parameters
   - θ = (XᵀX)⁻¹Xᵀy
   - Efficient for small datasets

2. **Gradient Descent**
   - Iterative optimization approach
   - Gradually adjusts parameters toward minimum
   - Suitable for large datasets
   - Various variants (Batch, Stochastic, Mini-batch)

## Key Characteristics

### Advantages

- **Interpretable**: Clear relationship between features and predictions
- **Efficient**: Fast training and prediction
- **Foundation**: Basis for more complex models
- **Well-studied**: Extensive theoretical foundation

### Limitations

- **Linearity assumption**: Assumes linear feature-target relationship
- **Sensitivity to outliers**: Squared error emphasizes extreme values
- **Multicollinearity issues**: Correlated features can destabilize solutions
- **Underfitting**: May perform poorly on complex nonlinear relationships

## Applications

- Real estate price prediction
- Economic forecasting
- Demand forecasting
- Risk assessment
- Scientific modeling

## Implementation Considerations

- Feature scaling often improves performance
- Regularization (Ridge/Lasso) can prevent overfitting
- Polynomial features can capture nonlinear relationships
- Assumption checking (linearity, homoscedasticity, normality) is important

Linear regression serves as an excellent starting point for regression problems and provides fundamental insights into the relationship between variables through its interpretable parameter coefficients.
