          1. What is Scikit-learn (sklearn)?
Scikit-learn is a popular Python library used for Machine Learning.
It provides ready-made algorithms that help us build Machine Learning models without implementing every mathematical calculation from scratch.
ex house:
Scikit-learn provides algorithms to learn the relationship between these inputs and the house price.
 Important: Scikit-learn is the library. Linear Regression, Random Forest, KNN, and Decision Tree are algorithms available through that library.
      2. What is Random House Price Data?
For learning purposes, we can create our own house price dataset using randomly generated values.
 The model learns how house area and bedrooms are related to house prices.
 Random data is useful for learning code, but it is not actual real-estate market data.
   3. What is Random Seed?
Random seed is a value used to control random number generation.
In Python, we can use NumPy to generate random numbers.
 Why do we use random_state=42?
Suppose you run a program today and generate random data.
Tomorrow, you run the same program again.
Without a fixed seed, you may get different random values.
With a fixed seed, you get the same sequence of random values when the same code and conditions are used.
 This is called Reproducibility.
Reproducibility means getting the same results again when you repeat an experiment under the same conditions.
   ex:np.random.seed(42)
print(np.random.randint(1, 100, 5))
Run this code multiple times from the beginning. You will get the same five numbers.
  why is 42 used?
42 is simply a commonly used example. You can use 10, 25, 100, or another integer.
The important thing is to keep the seed fixed when you want repeatable results.
     4.What is train_test_split()?
train_test_split() is a function available in Scikit-learn.
It divides our dataset into training and testing datasets.
 now understand its perametars
   X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
  Why do we use random_state=42 here?
  The function randomly selects which records go into training and testing.
By setting random_state=42, we get the same split each time we execute the code with the same dataset.
      5. What is Linear Regression?
Linear Regression is a Supervised Machine Learning algorithm.
It is mainly used to predict continuous numerical values.
Examples:
- House price prediction
- Salary prediction
- Sales prediction
- Temperature prediction
  6. What is Initializing a Linear Regression Model?
Initializing means creating an object of the Linear Regression algorithm before training it.
ex:model = LinearRegression()
Let's understand this code:
- LinearRegression is the algorithm provided by Scikit-learn.
- model is the variable.
- = assigns the created object to the variable.
- () creates an instance of the Linear Regression class.
Important: At this stage, the model has not learned anything from your house price dataset.
It is only initialized and ready for training.
   7. What is Training a Linear Regression Model?
Training means teaching the model using our training dataset.
We use the .fit() method.
model.fit(X_train, y_train)
model: Our initialized Linear Regression model.
.fit(): The method that trains the model.
X_train: Input training features.
y_train: Actual training target values.
