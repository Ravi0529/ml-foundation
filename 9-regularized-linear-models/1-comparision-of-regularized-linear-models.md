# Regularization Techniques Comparison

| Aspect                          | Ridge Regression (L2)        | Lasso Regression (L1)             | Elastic Net                       | Early Stopping                  |
| ------------------------------- | ---------------------------- | --------------------------------- | --------------------------------- | ------------------------------- |
| **Type**                        | Parameter regularization     | Parameter regularization          | Parameter regularization          | Training process regularization |
| **Cost Function**               | `MSE + α×½∑θᵢ²`              | `MSE + α×∑\|θᵢ\|`                 | `MSE + rα∑\|θᵢ\| + (1-r)α/2×∑θᵢ²` | Stop when val error increases   |
| **Feature Selection**           | ❌ No (weights → 0, never 0) | ✅ Yes (weights = 0)              | ✅ Yes (weights = 0)              | ❌ No                           |
| **Handles Correlated Features** | ✅ Excellent                 | ❌ Poor                           | ✅ Good                           | ✅ Good                         |
| **Hyperparameters**             | `alpha`                      | `alpha`                           | `alpha`, `l1_ratio`               | `patience`                      |
| **Best For**                    | All features relevant        | Feature selection                 | General purpose                   | Iterative algorithms            |
| **Model Sparsity**              | ❌ Dense model               | ✅ Sparse model                   | ✅/❌ Adjustable sparsity         | ❌ Dense model                  |
| **Stability**                   | ✅ Very stable               | ❌ Less stable                    | ✅ Stable                         | ✅ Stable                       |
| **Computation**                 | Moderate                     | Moderate                          | Moderate                          | ⚡ Saves computation            |
| **Interpretability**            | Medium                       | ✅ High (know important features) | High                              | Medium                          |
