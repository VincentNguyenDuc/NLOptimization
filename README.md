# NLOptimization

Numerical methods for Nonlinear Regression Optimization

## Gauss-Newton Method

- Gauss-Newton Method can be utilised to solve Nonlinear Least-squares problem. However, the algorithm may diverged if the initial point is not suitable.
- One way to guarantee its convergence is to perform a **line search** to find a good learning rate (between 0 and 1) instead instead of using unit learning rate

### Damped Gauss-Newton Method

- We can add a stepsize into the descent direction of GN method, allowing the tuning of learning rate.
- However, the stepsize is still fixed and require tunning.

### Line Search

#### Naive Approach

- We can implement a simple line search is to ensure that the value of the objective function at the next position is smaller than the current position: f(x + some_direction) < f(x)
- However, this approach may jump over a local minimum.

#### Exact Linesearch

- We can let the stepsize change based on Armijo conditions

#### Inexact Linesearch

- Calculating the exact stepsize based on Armijo condition may be inefficient
- We can use Wolfe conditions to efficiently compute an acceptable step size that sufficiently reduce the objective function

### Automatic Differentiation

#### Jacobian

- The GN method requires the evaluation of Jacobian of function vectors
- However, it may be complex to derive the Jacobian matrix from the original function

#### AutoDiff

- Allow us to evaluate without compute by hand
- However, it will require additional computation at each iteration

### Testing

#### Dataset

#### Fitting