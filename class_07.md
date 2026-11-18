1. What is a linear equation?
A linear equation is a mathematical equation that represents a straight line.

The most common linear equation is:
y = mx + c
re studying and want to understand the relationship between study hours and exam marks.
 2. What is slope?
Slope tells us how much Y changes when X increases by one unit.
In simple words:
Slope = Rate of change.
  3. What is intercept?
Intercept is the value of Y when X = 0.
 Real-world meaning: In our example, the model predicts 20 marks when study hours are zero. This is just an illustrative mathematical assumption, not a real guarantee.
  4. What is Linear Regression?
Linear Regression is a supervised machine learning algorithm used to predict continuous numerical values.
Examples:
- Predict house prices.
- Predict student marks.
- Predict salary.
- Predict sales.
- Predict stock prices (with important limitations).
  Instead of manually calculating everything, you train a Linear Regression model.
The model learns a relationship between study hours and marks.
  5. What is Polynomial Regression?
Polynomial Regression is a supervised machine learning algorithm used to predict continuous numerical values when the relationship between input and output is curved rather than a straight line.
In Linear Regression, we use a straight line.
In Polynomial Regression, we use a curved line to represent the relationship.
 Imagine you are studying for an examination.
Initially, when you increase study hours, your marks increase slowly. After more practice, your marks may increase faster.
This kind of relationship might be better represented by a curve.
      ex:Linear Regression:
y=2x+3
Polynomial Regression:
y=x^2+2x+3
ex of the train and test data 
X_train, X_test, y_train, y_test = train_test_split(
    X, y,
    test_size=0.25,
    random_state=42)
  6.What is overfitting in Polynomial Regression?
Suppose you use a polynomial degree of 2.
The model learns a simple curve.
Now suppose you increase the degree to 15.
The model may create a very complicated curve that follows almost every training data point.
This is called overfitting when the model learns the training data too closely, including noise, and performs poorly on unseen data.
