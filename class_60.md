  1. What is a function?
A function is a mathematical relationship between an input and an output.

For example:
f(x)=2x+3
The input changes, so the output also changes.
Why do we use functions in Machine Learning?
A Machine Learning model is also a mathematical function.
      2. What is a derivative of a function?
A derivative measures how quickly the output of a function changes when its input changes.
In simple words:
A derivative tells us the rate of change of a function.
The symbol for a derivative is:
{dy}{dx}

ex:Step 1: Understand the power rule
The power rule is:
{d}{dx}(x^n)=nx^{n-1}}

Meaning:
1. Bring the power \(n\) to the front.
2. Multiply it by the coefficient.
3. Reduce the power by 1.
Step 3: Understand derivatives visually
For the function \(f(x)=x^2\), the derivative tells us the slope of the curve at a particular point.
Look at the moving point in the visualization. As the second point approaches the first point, the secant slope approaches the tangent slope.
The tangent slope is the derivative.
 3. How to find maximum and minimum of a function?
    A. Maximum value
A maximum is the highest point of a function within the region being considered.
Example:
f(x)=-x^2+4x+5
This is a downward-opening parabola. It has a maximum point.
B. Minimum value
A minimum is the lowest point of a function within the region being considered.
Example:
f(x)=x^2-4x+3
This is an upward-opening parabola. It has a minimum point.
 How do we find maximum and minimum using derivatives?
There are three important steps.
1. Find the first derivative.
2. Set the first derivative equal to zero.
3. Use the second derivative to identify maximum or minimum.
    Example 1: Find the maximum
Given:
f(x)=-x^2+4x+5
 Maximum occurs at (x=2).
Maximum value is 9.
Maximum point is ((2,9)).
 Example 2: Find the minimum
Given:
f(x)=x^2-4x+3
 Minimum occurs at (x=2).
Minimum value is -1.
Minimum point is ((2,-1)).
Remember: A point where the first derivative is zero is called a stationary point. It is not automatically a maximum or minimum.
       5. What is the Chain Rule?
The Chain Rule is used to differentiate a function that contains another function inside it.
In simple words:
When one function is inside another function, we use the Chain Rule to calculate its derivative.
    The formula is:
{dy}{dx}={dy}{du}{du}{dx}
Why is Chain Rule important in Machine Learning?
Machine Learning models contain multiple mathematical operations.

For example:
x rightarrow z rightarrow hat y rightarrow Loss
Each operation depends on the previous operation.
To calculate how the loss changes when a model parameter changes, we need the Chain Rule.
This is the mathematical foundation of Backpropagation in Neural Networks.
        6. What is Gradient Descent?
Now let's connect all these mathematical concepts to Machine Learning.
Gradient Descent is an optimization algorithm used to find the minimum value of a loss function.
In simple words:
Gradient Descent helps a Machine Learning model reduce its prediction errors by adjusting its parameters.
ex: if suppose model make errors na The model has made an error.
We want to reduce that error by adjusting the model's parameters.
This is where Gradient Descent helps.
