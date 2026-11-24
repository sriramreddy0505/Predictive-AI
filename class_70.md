 1. What is Linear Regression?
Linear Regression is a supervised machine learning algorithm used to predict a continuous numerical value.
 2. Linear Regression Formula
The simple Linear Regression equation is:
 hat y = \theta_0+\theta_1x
 What is theta (θ)?

Theta represents the model's parameters that it must learn from training data.
- Theta zero controls where the line starts.
- Theta one controls the slope of the line.
The learning algorithm tries to find the best values of theta.
 3. Multiple Linear Regression and Theta
When we have multiple independent features, the equation becomes:
  hat y=theta_0+theta_1x_1+theta_2x_2+cdots+theta_nx_n
  4. What is the Cost Function?
The Cost Function measures how much error our model makes while predicting.
In Linear Regression, we commonly use Mean Squared Error (MSE).

J(theta_0,theta_1)=
  {1}{2m}sum_{i=1}^{m}
  \hat y_i-y_i)^2
  Where:
- (J) = Cost function.
- (m) = Number of training examples.
- (\hat y_i) = Predicted value.
- (y_i) = Actual value.
- (hat y_i-y_i) = Prediction error.
Why do we square the error?
1. Negative errors become positive.
2. Large errors receive more penalty.
3. It gives a smooth, differentiable function for optimization.
   5. What is a Derivative?
A derivative measures how quickly a function changes when its input changes.
Why do we need derivatives in Linear Regression?
- Is our cost increasing?
- Is our cost decreasing?
- Which direction should theta move?
- How can we reduce prediction error?
6. Partial Derivatives of Linear Regression
Now let's understand the most important mathematical part.
We need to calculate two partial derivatives.
Why is there an \(x_i\) in the second derivative?
Because theta one is multiplied by x in the prediction equation. When differentiating with respect to theta one, the derivative of the prediction is x.
These two derivatives tell us how to adjust the intercept and slope to reduce the cost.
  7. What is Gradient Descent?
Gradient Descent is an optimization algorithm used to find the parameter values that minimize the cost function.
 Imagine standing on a mountain and wanting to reach the lowest point in a valley.
- You check the slope.
- You move in the downhill direction.
- You check the slope again.
- You repeat until you reach a minimum.
   8. Gradient Descent Formula
  Symbol	Meaning
(\theta_j)	Current parameter
(\alpha\)	Learning rate
(\frac{\partial J}{\partial\theta_j}\)	Derivative / gradient
(-\)	Move in the opposite direction of the gradient
The learning rate determines how large each update step is.
- Too small: Learning is very slow.
- Too large: It may overshoot the minimum or diverge.
- Appropriate: It can converge efficiently.
  9. Gradient Descent: Complete Numerical Example
Let's perform Gradient Descent manually so you can understand every step.
 10. What is Iteration?
An iteration means one complete update cycle of the model parameters.
One iteration includes:
1. Calculate predictions.
2. Calculate errors.
3. Calculate cost.
4. Calculate derivatives.
5. Update theta values.
   Notice that cost keeps decreasing in this example.
This continues until the model reaches convergence.
 11. What is Convergence?
Convergence means the algorithm has reached a point where further updates produce very little improvement.
Important: Convergence does not automatically mean that predictions are accurate. It only means optimization has stopped making significant progress.
The model might have converged to a poor solution if the data or model is unsuitable.
12. What is Global Minimum?
Global Minimum is the lowest possible value of the cost function over all allowed parameter values.
Left side: Cost is high.
Middle: Cost is lowest.
Right side: Cost increases again.
 Why is Global Minimum important in Linear Regression?
For ordinary Linear Regression with the squared-error cost function, the cost is convex.
That means every local minimum is also a global minimum.
Therefore, with a suitable learning rate, Gradient Descent can find a global minimum.
Important distinction:
- Local Minimum: Lowest point in a particular nearby region.
- Global Minimum: Lowest point across the entire allowed parameter space.
   13. Low Bias and High Bias
Now let's understand Bias and Variance.
These are important concepts in Machine Learning because a model should perform well on both training data and unseen testing data.
Bias refers to error caused by overly simple assumptions made by the model.
High Bias
High Bias means the model is too simple to understand the actual relationship in the data.
Characteristics:
- Model is too simple.
- Training error is high.
- Testing error is high.
- Model underfits the data.
  Low Bias
Low Bias means the model can capture the underlying relationship more accurately.
Characteristics:
- Model captures the important patterns.
- Training error is relatively low.
- Model can make accurate predictions if variance is also controlled.
  14. Low Variance and High Variance
Variance refers to how sensitive a model is to changes in its training data.
High Variance
High Variance means the model learns too much from the training data, including noise.
Characteristics:
- Model is too complex.
- Training error is very low.
- Testing error is high.
- Model overfits the training data.
Low Variance
Low Variance means the model's predictions are relatively stable when the training dataset changes.
Characteristics:
- Less sensitivity to small changes in training data.
- More stable predictions.
- Often better generalization when bias is also low.
15. Bias–Variance Comparison
  Our target: Low Bias + Low Variance.
One important point: reducing bias can sometimes increase variance, and reducing variance can sometimes increase bias. This is called the Bias–Variance Tradeoff.
