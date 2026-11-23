   1. What is Linear Regression?
Linear Regression is a supervised machine learning algorithm used to predict continuous numerical values.
It finds the relationship between input variables (features) and an output variable (target).
 Our objective is to train a machine learning model that predicts house prices based on house area and bedrooms.
 2. What is R² Score (R-Squared)?
     R² stands for Coefficient of Determination.
It tells us how well our regression model explains the variation in the target variable.
R² tells us how well the model fits the actual data.
 3. What is Adjusted R²?
    It measures how well the model explains the variation in the target variable while considering the number of independent variables (features) used in the model.
    R² generally never decreases when additional predictors are added to an ordinary least squares regression model fitted on the same data.
      Adjusted R² solves this problem by penalizing unnecessary features.
Adjusted R² Formula
Adjusted\ R^2 =
1-(1-R^2)\{n-1}{n-p-1}
 4. What is Mean Squared Error (MSE)?
MSE stands for Mean Squared Error.
It measures the average squared difference between actual values and predicted values.
MSE tells us how far our model's predictions are from the actual values, on average, after squaring the errors.
mainly caluculated error:
Error = Actual-Predicted
