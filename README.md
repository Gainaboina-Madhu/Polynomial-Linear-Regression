# Polynomial-Linear-Regression
- Polynomial Linear Regression is a supervised machine learning technique that extends linear regression by modeling non-linear relationships using polynomial features.

# 📌 Overview

- Polynomial Linear Regression is an extension of Simple Linear Regression that allows us to model non-linear relationships between the independent variable(s) and the dependent variable.
- Although it’s called polynomial, it is still considered a linear regression model because it is linear in terms of the coefficients.

- This technique is widely used when data shows a curved trend that a straight line cannot properly fit.



# 1️⃣ **Simple Linear Regression fits data using a straight line:**
- Linear Regression assumes a straight-line relationship between input and output:
  
   𝑦 = 𝑚 𝑥 + 𝑐
  
- When a straight line underfits the data, Polynomial Linear Regression is used to model the curvature.

# 2️⃣ What Is Polynomial Linear Regression?

- Polynomial Linear Regression models the relationship between the dependent variable y and independent variable x as an nth-degree polynomial:

<img width="800" height="533" alt="image" src="https://github.com/user-attachments/assets/20f47298-8116-4e57-b013-2c7a235a7028" />


- Even though the equation looks non-linear, it is still called linear regression bec

- Standard linear regression optimization techniques can be applied

# Working of Polynomial Linear Regression

1️⃣ Import Required Libraries:
     - import numpy as np
     - import pandas as pd
     - import matplotlib.pyplot as plt
     - import sklearn
2️⃣ Load the Dataset
     - df = pd.read_csv('Position_Salaries.csv')
    The dataset contains:
    - Position
    - Level
    - Salary
3️⃣ Data Preprocessing
    - df = df.drop(['Position'], axis=1)


- The Position column is removed
- Only numerical features are used for regression

4️⃣ Define Independent and Dependent Variables
- X (Level) → input feature
- y (Salary) → target value

5️⃣ Visualize the Data
     - plt.scatter(x=X, y=y, color='r', marker='*')
     - plt.title('POLYNOMIAL REGRESSION')
     - plt.show()

 <img width="439" height="297" alt="image" src="https://github.com/user-attachments/assets/9a5861a8-540c-4e09-843f-16ed36b78381" />

6️⃣ Create Polynomial Features
     - from sklearn.preprocessing import PolynomialFeatures
     - poly_reg = PolynomialFeatures(degree=2)
     - poly_res = poly_reg.fit_transform(X)
 
7️⃣ Apply Linear Regression on Polynomial Features
     - from sklearn.linear_model import LinearRegression
     - reg = LinearRegression()
     - reg.fit(poly_res, y)
- Even though the relationship is curved:
- Linear Regression is still used
- That’s why it’s called Polynomial Linear Regression

8️⃣ Make Predictions
    - prediction = reg.predict(poly_res)

9️⃣ Visualize the Polynomial Regression Curve
     - plt.scatter(x=X, y=y, color='r', marker='*')
     - plt.plot(X, prediction, color='b')
     - plt.title('POLYNOMIAL REGRESSION')
     - plt.show()
     
# Conclusion:

 <img width="439" height="297" alt="image" src="https://github.com/user-attachments/assets/ca6cacd3-8713-4dad-ab54-24759dd3f577" />


- Red points → actual data

- Blue curve → polynomial regression model

# 🧠 Key Insight

- Polynomial Regression works by transforming features, not by changing the regression algorithm.

# uses of PLR:

- 1. Salary Prediction:
. Used when salary growth is not linear with experience or position level.
- 2. Trend Analysis:
. Helps model curved trends in:
- 3. Population Growth Modeling
. Population growth often follows a curved pattern, not a straight line.
- 4. Scientific & Engineering Data
- 5. Machine Learning Feature Engineering
 
  
# 📌 Summary

- Best for non-linear relationships

- Polynomial features are created

- Linear regression is applied

- Curved regression line fits data better
