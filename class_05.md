 Part 1: What is a Hyperplane?
First, understand what a plane is.
A hyperplane is a flat geometric surface that divides a space into two parts.
The meaning of a hyperplane depends on the number of dimensions.
Dimensions	Geometric object	Equation
1D	Point	(x=a)
2D	Straight line	(y=mx+c)
3D	Flat plane	(ax+by+cz+d=0)
4D or higher	Hyperplane	(w_1x_1+\cdots+w_nx_n+b=0)
 1.1 Hyperplane in 2D
2D means two-dimensional space.
We have two independent variables:
- X-axis
- Y-axis
Why is a 2D line called a hyperplane?
Because a hyperplane in 2D has one dimension less than the space itself.
- Space dimension = 2
- Line dimension = 1
Therefore, the line is a 2D hyperplane.
 1.2 Hyperplane in 3D
Now let's move from 2D to 3D.
3D means three-dimensional space.
We have three independent variables:
- X-axis
- Y-axis
- Z-axis
A multiple linear regression model looks like:
hat y=w_1x_1+w_2x_2+w_3x_3+b
  Important: With three input features, the model's equation has three-dimensional input space. Its prediction equation is a hyperplane in that 3D feature space.
   3.function
   3.1 Types of functions
Function	Formula	Example
Constant	(f(x)=5)	Always 5
Linear	(f(x)=2x+3)	Straight line
Quadratic	(f(x)=x^2)	Parabola
Polynomial	(f(x)=x^3+2x^2+x)	Polynomial curve
Exponential	(f(x)=2^x)	Exponential growth
 Part 4: What is a Derivative?
A derivative tells us how quickly a function changes when its input changes.
  4.1 Derivation of a function
Let's derive the formula for the derivative from first principles.

Suppose:
f(x)=x^2

The derivative definition is:
f'(x)=\lim_{h\to0}{f(x+h)-f(x)}{h}
 The derivative of \(x^2\) is \(2x\).
This process is called differentiation from first principles.
  Part 5: What is the Sum Rule?
The sum rule is one of the basic differentiation rules.

Definition: When two or more functions are added, differentiate each function separately and add their derivatives.

Mathematical formula:
{
{d}{dx}[f(x)+g(x)]
=f'(x)+g'(x)
}
Part 6: What is the Chain Rule?
The chain rule is another important differentiation rule.
Definition: The chain rule is used when one function is inside another function.
In simple words:
When one function depends on another function, differentiate the outer function first and multiply it by the derivative of the inner function.
  Here, the output depends on the previous calculation.
When the neural network makes a prediction, it calculates the error using a loss function.
To reduce this error, the model must understand how changing its weights affects the loss.
The chain rule helps calculate those derivatives.
This process is used in Backpropagation.
The overall learning process:
1. Forward propagation: Make a prediction.
2. Calculate loss: Measure prediction error.
3. Backpropagation: Calculate gradients using the chain rule.
4. Update weights: Improve the model.
5. Repeat: Continue learning.
   
