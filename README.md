## Task 1: Data Understanding

Q1. Why is this dataset suitable for Linear Regression?

This dataset is suitable for Linear Regression because it contains a single numerical input feature (years of experience) and a numerical output (salary). The salary increases as years of experience increase, showing a clear linear trend. There are no complex patterns or categories involved. This makes it ideal for modeling a straight-line relationship.

Q2. What assumption does Linear Regression make?

Linear Regression assumes that there is a linear relationship between the input feature and the target variable. It assumes that changes in the input lead to proportional changes in the output. It also assumes that errors are random and evenly distributed around the regression line.


## Task 5: COMPARISON WITH SKLEARN 

Q1. Why are the values similar but not exactly identical?

The values are similar because both models are learning the same underlying relationship between years of experience and salary. However, they are not exactly identical because the scratch model uses gradient descent with a fixed learning rate and limited epochs, while sklearn uses a more optimized mathematical approach. Small numerical differences are expected due to different optimization methods and stopping conditions.

Q2. What does sklearn do differently internally?

sklearn’s Linear Regression uses a closed-form solution based on linear algebra to compute the optimal parameters directly, instead of iteratively updating them using gradient descent. It also includes better numerical stability and internal optimizations, which allows it to find a precise solution more efficiently.


## Task 6: THINKING TASK 


Q1. If we train for 10,000 epochs instead of 1,000, will the model always improve? Why or why not?

No, Training a linear regression model for 10,000 epochs will not always improve performance. In the early epochs, the model learns quickly because errors and gradients are large. As training continues, the model converges and the gradients become very small, so further epochs do not significantly reduce the loss. This leads to diminishing returns, where extra training only increases computation time without improving results. For simple datasets like the salary dataset, convergence usually happens well before 1,000 epochs, so increasing epochs does not guarantee better performance.


Q2. Why is gradient descent preferred over directly trying all possible values of w and b?

Gradient descent is preferred because trying all possible values of w and b is computationally impossible. The parameter space is continuous, meaning there are infinitely many combinations to test. Gradient descent efficiently finds the optimal values by using the gradient of the loss function to guide parameter updates toward minimum error. This makes it practical, fast, and scalable, especially for large datasets and higher-dimensional models where brute-force approaches completely fail.