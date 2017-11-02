# Linear regression tutorial
In simple linear regression, we predict scores on one variable from the scores on a second variable. The variable we are predicting is called the criterion variable and is referred to as Y. The variable we are basing our predictions on is called the predictor variable and is referred to as X. 

Linear regression is an essential work horse to the machine learing tool kit. In the following, we will use Python to implement a simplie linear regression. Note: the idea here is not to turn you into an expert on linear regression, more so for you to see the structure of a Python program and to become familiar with Python syntax.

## Import dependencies 
The following import functions will bring in extra libraries into your Python session.
```python
import matplotlib.pyplot as plt
import numpy as np
from sklearn import datasets, linear_model
from sklearn.metrics import mean_squared_error, r2_score
```

## Load in the data set
This will load the data set, diabetes, into our Python session. This has the data we will use to produce our linear regression.
``` python
diabetes = datasets.load_diabetes()
```

## Select the first variable
This will take a single column from the diabetes data and set it to the variable **diabetes_X**.
``` python
diabetes_X = diabetes.data[:, np.newaxis, 2]
```

## Create the test and train set
In machine learning, creating a test and train set it vital to validate the model.
**TASK**: What is the percentage of data is test?
HINT len(diabetes_X) will display our total number of data points. 
```python
diabetes_X_train = diabetes_X[:-20]
diabetes_X_test = diabetes_X[-20:]

diabetes_y_train = diabetes.target[:-20]
diabetes_y_test = diabetes.target[-20:]
```


## Create linear regression object and run the model. 
The following code is the central piece to our regression. 
**TASK**: The x variable for the training has been left for you to fill in. Paste in the correct x variable (from above) into the code to train the model.
```python
regr = linear_model.LinearRegression()

regr.fit(<fill in correct data here>, diabetes_y_train)
```

## Make predictions using the testing set
The following will make a prediction based our test set x. 
```python
diabetes_y_pred = regr.predict(diabetes_X_test)
```

## Print the mean squared error
The MSE assesses the quality of a predictor, the lower the value the better. 
```python
print("Mean squared error: %.2f"
      % mean_squared_error(diabetes_y_test, diabetes_y_pred))
```      

## Plot what the line of best fit
It is always good to plot the output of your results. The below code will plot our results, however, it would throw an error if you try and run it. 
**TASK**: Fix the code by editing plt.plot line by setting the color to blue
```python
plt.scatter(diabetes_X_test, diabetes_y_test,  color='black')
plt.plot(diabetes_X_test, diabetes_y_pred, color='', linewidth=3)

plt.xticks(())
plt.yticks(())

plt.show()
```

