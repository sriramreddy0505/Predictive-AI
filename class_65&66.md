  1.What are Independent Features and Dependent Features?
   A. Independent Features (X)
Independent features are the input variables that we give to the Machine Learning model to make predictions.
 Here, independent features are:
- Study Hours
- Attendance
- Previous Marks
We use these values as inputs to predict final marks.
  B. Dependent Feature (Y)
The dependent feature is the output variable that we want our model to predict.
 3. What is Correlation?
Correlation measures the strength and direction of the relationship between two numerical variables.
  1. Positive Correlation
When one variable increases, the other variable also tends to increase.
Example:
- Study hours increase.
- Exam marks tend to increase.
  2. Negative Correlation
When one variable increases, the other variable tends to decrease.
Example:
- Product price increases.
- Demand may decrease.
  3. Zero or No Linear Correlation
There is no clear linear relationship between the two variables.
Example:
- Student shoe size.
- Student exam marks.
  Important interview point: Correlation does not mean causation.
For example, study hours and exam marks may have positive correlation. But correlation alone does not prove that study hours are the only reason for higher marks.
  Why do we use correlation?
1. To understand relationships between variables.
2. To identify useful features.
3. To detect highly correlated independent features.
4. To understand data before building a model.
   One more important point: High correlation between two independent features can indicate multicollinearity in linear regression.
    Correlation with the target is useful for exploration, but it should not be the only method for selecting features.
   4. What is Train-Test Split?
This is another important Machine Learning concept.
Train-Test Split divides your dataset into two parts:
- Training data.
- Testing data.
  5. What is Fit, Transform and Fit_Transform?
  First, understand that Machine Learning models and preprocessing tools need to learn information from data.
  Sometimes we use scaling to bring numerical features onto comparable scales.
   A. What is Fit?
fit() means learning or calculating information from the given data.
 B. What is Transform?
transform() applies the learned information to convert the data.
It uses the mean and standard deviation learned during fit() to scale the values.
    C. What is Fit_Transform?
fit_transform() combines both operations.
It first learns the information and then transforms the data.
  Method        	What does it do?
fit()     	     Learns information
transform()	     Transforms data using learned information
fit_transform()	 Learns and transforms together
fit() has different meanings depending on the object. For a scaler, it learns preprocessing parameters. For Linear Regression, it learns model coefficients and intercepts.
 6. What is LinearRegression and why do we use lr?
  LinearRegression = Machine Learning algorithm/class.
  lr = Variable name that stores the model object.
    What does lr.fit() do?
  ex:lr.fit(X_train, y_train)
  This trains the Linear Regression model.
The model learns the mathematical relationship between independent and dependent variables.
 7. What is plt.scatter()?
plt.scatter() is a Matplotlib function used to create a scatter plot.
How to understand the scatter plot?
- Dots moving upward → Positive relationship.
- Dots moving downward → Negative relationship.
- Randomly distributed dots → No clear linear relationship.
  important:Linear Regression does not require fit_transform() by default.
  
