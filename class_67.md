   1.OLS = Ordinary Least Squares
OLS is a statistical method used to find the best-fitting regression line by minimizing the sum of squared differences between actual values and predicted values.
mainly it can be work on the:
Imagine you want to reach a mountain's lowest point.
- You are standing at the top.
- You take one step down.
- You calculate whether you are getting closer to the lowest point.
- You continue taking steps.
- Finally, you reach a point where the error is minimized.
  2.SGD = Stochastic Gradient Descent
SGD is an optimization algorithm used to find the best model parameters by gradually reducing the prediction error.
  How does it work?
Imagine you want to reach a mountain's lowest point.
- You are standing at the top.
- You take one step down.
- You calculate whether you are getting closer to the lowest point.
- You continue taking steps.
- Finally, you reach a point where the error is minimized.
  3. What is fit()?
fit() means training the machine learning model.
In simple words, the model learns patterns from the training dataset.
  Let's understand each part:
- lr: Your machine learning model.
- fit(): Training method.
- X_train: Independent features.
- y_train: Dependent target.
  4.What is Prediction?
Prediction means using the trained model to estimate the output for new or unseen data.
In Scikit-learn, we use predict().
  5. What is StandardScaler?
StandardScaler is a preprocessing technique used to standardize numerical features.
It transforms features so that they have:
- Mean approximately equal to 0.
- Standard deviation approximately equal to 1.
  Some machine learning algorithms, particularly SGD, KNN and SVM, can perform poorly when features have very different scales.
   Why fit_transform on training data?
Because the scaler calculates the mean and standard deviation from training data and transforms it.
Why only transform on testing data?
Because we must use the same training mean and standard deviation for test data.
    6. What are Min and Max?
Min and Max are used to identify the smallest and largest values in a dataset.
- min() = Minimum value.
- max() = Maximum value.
   What is MinMaxScaler?
MinMaxScaler is another feature scaling technique.
It normally converts values into a range between 0 and 1.
 7. What are Metrics?
Metrics are used to evaluate machine learning model performance.
In regression, we commonly use:
1. MAE
2. MSE
3. RMSE
4. R² Score
   A. MAE (Mean Absolute Error)
MAE calculates the average absolute difference between actual and predicted values.
B. MSE (Mean Squared Error)
MSE calculates the average squared error.
C. RMSE (Root Mean Squared Error)
RMSE is the square root of MSE.
D. R² Score
R² measures how well the model explains the variation in the target variable.
E. Adjusted R²
Adjusted R² considers the number of independent features in your model.
8. What is Test Performance?
Test performance means evaluating how well your trained model performs on data that it has never seen during training.
After training, you give it the remaining 200 records and compare its predictions with actual salaries.
This tells you how well your model generalizes to unseen data.

