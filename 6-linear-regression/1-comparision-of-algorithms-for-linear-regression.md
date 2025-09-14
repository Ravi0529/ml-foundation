# Comparision of algorithms for Linear Regression

### Linear Regression is the model.

- Normal Equation, SVD and Gradient Descent are the optimization algorithms that can be used to train (fit) Linear Regression.

| Algorithm       | Large m | Out-of-core support | Large n | Hyperparams | Scaling Required | Scikit-Learn     |
| --------------- | ------- | ------------------- | ------- | ----------- | ---------------- | ---------------- |
| Normal Equation | Fast    | No                  | Slow    | 0           | No               | N/A              |
| SVD             | Fast    | No                  | Slow    | 0           | No               | LinearRegression |
| Batch GD        | Slow    | No                  | Fast    | 2           | Yes              | SGDRegressor     |
| Stochastic GD   | Fast    | Yes                 | Fast    | >=2         | Yes              | SGDRegressor     |
| Mini-batch GD   | Fast    | Yes                 | Fast    | >=2         | Yes              | SGDRegressor     |

`m = number of training examples (rows, samples)`

`n = number of features (columns, dimensions)`
