   1.What is Ridge Regression?
Ridge Regression is a regularization technique based on Linear Regression.
It reduces the size of model coefficients by adding a penalty to the ordinary least squares error.
Imagine your model has many independent features:
- Temperature
- Humidity
- Wind speed
- Rainfall
- Pressure
- Other environmental measurements
  Sometimes the model learns very large coefficients. This can make it sensitive to small changes in training data and can cause overfitting.
      2.What is Lambda (α)?
In Scikit-learn, Ridge Regression uses the parameter alpha instead of commonly written \(\lambda\).
Important interview point: Ridge Regression generally reduces coefficients towards zero, but it does not usually make them exactly zero. Lasso Regression can make some coefficients exactly zero.
     3.Why do we use Ridge Regression?
- To reduce overfitting.
- To control large coefficients.
- To improve model generalization.
- To handle multicollinearity (high correlation between independent variables).
- To make the model less sensitive to training-data variations.
  Remember: Always consider feature scaling before Ridge Regression because the penalty depends on coefficient sizes.
     What is Cross-Validation?
  1. Understand the problem first
Suppose you have 1000 rows in a dataset.
You divide them into:
- 80% training data = 800 rows.
- 20% testing data = 200 rows.
  ex:from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
The model learns from 800 rows and evaluates its performance on 200 rows.
But there is one problem.
What if those 200 test rows are unusually easy or unusually difficult?
Your model's performance might depend too much on that one particular split.
This is why we use Cross-Validation.
 2. What is Cross-Validation?
Cross-Validation is a model evaluation technique in which we divide the training dataset into multiple parts and repeatedly train and evaluate the model.
Its main purpose is to check how well a model performs on different portions of data.
Instead of evaluating the model using only one split, you evaluate it multiple times using different training and validation portions.
 Why is it useful?
1. To evaluate model performance more reliably.
2. To identify overfitting.
3. To compare different machine learning algorithms.
4. To select suitable hyperparameters.
5. To understand how well a model generalizes to unseen data.
   1. What is K-Fold?
K-Fold Cross-Validation divides the dataset into K equal or nearly equal parts called folds.

For example, if K = 5:
- Fold 1
- Fold 2
- Fold 3
- Fold 4
- Fold 5
Each time, one fold is used for validation and the remaining four folds are used for training.
Let's understand this with an example.
Suppose we have 100 records.
K = 5.
  2.python implimentation:
  ex code:
  from sklearn.model_selection import KFold
from sklearn.model_selection import cross_val_score
from sklearn.linear_model import Ridge
from sklearn.pipeline import make_pipeline
from sklearn.preprocessing import StandardScaler

model = make_pipeline(
    StandardScaler(),
    Ridge(alpha=1.0)
)

kf = KFold(
    n_splits=5,
    shuffle=True,
    random_state=42
)

scores = cross_val_score(
    model,
    X,
    y,
    cv=kf,
    scoring="r2"
)

print("Individual scores:", scores)
print("Average score:", scores.mean())


and mainly we can understand the 
Understand these parameters:
- n_splits=5: Divide the dataset into five folds.
- shuffle=True: Shuffle the rows before splitting.
- random_state=42: Make the splitting reproducible.
- scoring="r2": Evaluate using the R² metric.
- scores.mean(): Calculate the average score.
Notice that I used StandardScaler() inside a Pipeline. This is important because scaling must be learned separately from each training fold to prevent data leakage.
   1. What is LOOCV?
LOOCV is a special type of Cross-Validation.
Instead of dividing the dataset into five or ten folds, it uses only one record for validation at a time.
All the remaining records are used for training.
   ex python implimentation:
Why did I use neg_mean_squared_error?
Scikit-learn follows a scoring convention where higher scores are better. Therefore, it returns negative MSE. We multiply the average by -1 to get the actual positive MSE.
Important: LOOCV is computationally expensive for large datasets because it trains the model once for every record.
    1. What is the Algerian Forest Fires dataset?
The Algerian Forest Fires dataset is a real-world dataset used for machine learning experiments related to forest fires.
It contains weather measurements and Fire Weather Index (FWI) measurements collected from two regions of Algeria.
- Bejaia region – Northeast Algeria.
- Sidi Bel-Abbes region – Northwest Algeria.
   2. What is the objective of this dataset?
Imagine you are working as a Data Scientist for an environmental organization.
Your organization wants to understand whether weather conditions are associated with forest fires.
You receive information such as:
- Temperature
- Relative humidity
- Wind speed
- Rainfall
- Fire Weather Index
  
