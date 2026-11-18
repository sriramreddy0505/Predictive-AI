  1. What is Simple Linear Regression?
Simple Linear Regression is a supervised machine learning algorithm used to predict a numerical value based on one independent variable.
In simple words:
We give the machine learning model some previous data. The model learns the relationship between two variables and predicts a new value.
 2. Mathematical formula of Simple Linear Regression
The most important formula is:
hat{Y}=b_0+b_1X
Let's understand every term.
Term	Meaning
X	Independent variable
Y	Actual dependent variable
Ŷ	Predicted Y value
b₀	Intercept
b₁	Slope (coefficient)
3. What is a DataFrame?
A DataFrame is a two-dimensional data structure provided by the Pandas library.
It stores data in rows and columns, just like an Excel spreadsheet or SQL table.
     Why do we use DataFrames in Machine Learning?
Because real-world datasets contain thousands or millions of records. DataFrames help us load, organize, clean, and prepare data before training a model.
  4. What is Scikit-learn (sklearn)?
     Why do we use sklearn?
Scikit-learn provides ready-made machine learning algorithms and tools.
   5. What is Random Seed?
A random seed is a number used to control random operations so that we can reproduce the same results again.
In machine learning, we often randomly select data for training and testing.
For example, suppose we have 100 student records.
We want:
- 80 records for training.
- 20 records for testing.
    random_state=42
  42 is just an example number. You can use:
  whatever and There is no special mathematical importance to 42.
   Why do we use random seed?
1. To get reproducible results.
2. To compare different machine learning models fairly.
3. To make experiments consistent.
4. To help debug machine learning projects.
    Important difference:
- np.random.seed(42) controls NumPy's random number generation.
- random_state=42 controls randomness inside a particular Scikit-learn function.
- ex:from sklearn.model_selection
- import train_test_splitX_train,
-  X_test, y_train, y_test = train_test_split(
-     X, y, test_size=0.2, random_state=42)
Here, random_state=42 makes the split reproducible.
    6. What is train_test_split?
train_test_split is a Scikit-learn function used to divide a dataset into training data and testing data.
Why do we need it?
Because we should not train and evaluate a machine learning model using exactly the same data.
We need separate data to check whether the model can predict values it has not seen before.
A. Training data
Training data is the data given to the machine learning algorithm to learn patterns and relationships.
If we randomly select records every time, we may get different training and testing records.
To control this randomness, we use random_state.
B. Testing data
Testing data is separate data used to check how well the trained model predicts unseen records.
C. What is test_size?
test_size determines how much data should be reserved for testing.
