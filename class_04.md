      1. Cartesian Coordinate System
A Cartesian coordinate system is a mathematical system used to identify the exact position of a point using numbers.
It contains two main axes:
1. X-axis – Horizontal line.
2. Y-axis – Vertical line.
  What are coordinates?
Coordinates represent the position of a point.
  ML application: We use coordinate systems to visualize relationships between two variables, such as house size and house price.
   2. What is an Equation of a Line?
An equation of a line is a mathematical expression that represents a straight line on a graph.
The most common equation is:
boxed{y=mx+c}
 Notice that when X increases by 1, Y increases by 2.
This is how a straight-line equation works.
 3. What is an Intercept?
An intercept is the point where a line crosses an axis.
There are two important types.
  A. Y-intercept
The Y-intercept is the point where a line crosses the Y-axis.
For example:
y=2x+3
  B. X-intercept
The X-intercept is the point where a line crosses the X-axis.
To calculate it, put:

y=0
  4. Independent and Dependent Variables
These two variables are extremely important in Machine Learning.
A. Independent Variable (X)
An independent variable is the input variable.
It is the variable that we use to predict or explain another variable.
 B. Dependent Variable (Y)
A dependent variable is the output variable.
Its value depends on the independent variable in our prediction problem.
 Important: Independent and dependent variables describe their roles in a particular problem. They do not necessarily mean that X physically causes Y.
  5. What is Slope?
Slope describes the direction and steepness of a straight line.

The slope is represented by:

m
The formula is:{m={y_2-y_1}{x_2-x_1}
 6. General Form of a Linear Equation
The general form of a straight-line equation is:
      {Ax+By+C=0}
       Important difference:
Form	Equation
Slope-intercept form	   (y=mx+c\)
General form	    (Ax+By+C=0\)
Standard form	  (Ax+By=C\)
 7. What is a Line in Machine Learning?
Now let's connect mathematics with Machine Learning.
In ML, a line can represent the relationship between input and output variables.
he ML model learns a suitable relationship between X and Y from training data.

Then it can predict prices for new house sizes.
 8. What is a Hyperplane in Machine Learning?
 A hyperplane is a flat mathematical boundary that separates or divides data points in a feature space.
  Situation 1: One independent variable
When we have one feature, the decision boundary can be a point on a one-dimensional number line.
Situation 2: Two independent variables
When we have two features, the hyperplane is a straight line in a two-dimensional coordinate system.
 Situation 3: Three independent variables
When we have three features, the hyperplane becomes a plane in three-dimensional space.
 General equation of a hyperplane
{w_1x_1+w_2x_2+\cdots+w_nx_n+b=0}
  Where do we use hyperplanes?
- Logistic Regression classification
- Support Vector Machines (SVM)
- Linear classification
- Decision boundaries
Note: A hyperplane is not always the same as a regression line. A regression line predicts numerical values, whereas a classification hyperplane separates classes.
