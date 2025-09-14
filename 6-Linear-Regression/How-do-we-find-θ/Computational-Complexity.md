# Computational Complexity

## Normal Equation vs. SVD vs. Gradient Descent

| Method           | Complexity         | Pros                                                                    |
| ---------------- | ------------------ | ----------------------------------------------------------------------- |
| Normal Equation  | O(n³)              | Simple, straightforward formula                                         |
| SVD              | O(n²)              | More numerically stable. Handles singular matrices (uses pseudoinverse) |
| Gradient Descent | O(n) per iteration | Scalable to huge n and huge m                                           |
