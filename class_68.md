1. Understanding plt.scatter()
plt.scatter() is used to visualize the relationship between two variables.
 What does scatter plot do?
It displays individual data points as dots.
- X-axis = Study hours.
- Y-axis = Exam marks.
- Each dot = One student's observation.
  2. Linear Regression
Linear Regression is a supervised machine learning algorithm used to predict continuous numerical values.
Examples:
- House price prediction.
- Employee salary prediction.
- Student marks prediction.
- Sales prediction.
  Linear Regression tries to find the best straight line that represents the relationship between input and output.
  1. train_test_split()
It divides your dataset into two parts.
- Training data: Used to teach the model.
- Testing data: Used to check how well the model predicts unseen data.
  3. What is Polynomial Regression?
Polynomial Regression is another supervised machine learning algorithm.
It is useful when the relationship between X and Y is curved instead of a straight line.
For example:
- Temperature vs electricity consumption.
- Speed vs fuel consumption.
- Experience vs productivity in some situations.
- Advertising cost vs sales in some situations.
  What is the difference?
Linear Regression learns a straight-line relationship.
Polynomial Regression creates additional features such as X² and X³, allowing Linear Regression to learn a curved relationship.
  4. Generate nonlinear sample data
Our earlier sample data was mostly linear. To properly compare linear and polynomial models, let's generate a curved dataset.
It performs two operations:
1. fit() learns the feature structure and settings.
2. transform() converts the original input into polynomial features.
For test data, use only:
X_test_poly = poly.transform(X_test)
Why? Because the transformation must be based on the training data, not learned again from the testing data.
   5.What is flatten() in Python?
This is an important concept when working with NumPy, Machine Learning and Deep Learning.
flatten() converts a multidimensional array into a one-dimensional array.
ex:using FLtten()
flat_arr = arr.flatten()
print(flat_arr)
print(flat_arr.shape)
output:
[10 20 30 40 50 60]
(6,)
