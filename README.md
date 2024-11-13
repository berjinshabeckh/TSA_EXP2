# Ex.No: 02 LINEAR AND POLYNOMIAL TREND ESTIMATION

## Name:H.Berjin Shabeck
## Reg no:212222240018
## Date:24/08/2024

### AIM:
To Implement Linear and Polynomial Trend Estiamtion Using Python for student study hours and marks.

### ALGORITHM:
Import necessary libraries (NumPy, Matplotlib)

Load the dataset

Calculate the linear trend values using least square method

Calculate the polynomial trend values using least square method

End the program
### PROGRAM
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import PolynomialFeatures

# Data
data = pd.read_csv('/content/score.csv')

# Reshape the data
X = hours.reshape(-1, 1)
y = scores

# Linear Trend Estimation
linear_model = LinearRegression()
linear_model.fit(X, y)
linear_trend = linear_model.predict(X)

# Polynomial Trend Estimation (degree 2)
poly_features = PolynomialFeatures(degree=2)
X_poly = poly_features.fit_transform(X)

poly_model = LinearRegression()
poly_model.fit(X_poly, y)
poly_trend = poly_model.predict(X_poly)

# Plotting
plt.figure(figsize=(10,6))

# Plot the original data points
plt.scatter(hours, scores, color='blue', label='Data Points')

# Plot the linear trend
plt.plot(hours, linear_trend, color='red', label='Linear Trend')

# Plot the polynomial trend
plt.plot(hours, poly_trend, color='green', label='Polynomial Trend (degree=2)')

plt.title('Linear and Polynomial Trend Estimation')
plt.xlabel('Hours Studied')
plt.ylabel('Scores Obtained')
plt.legend()
plt.grid(True)
plt.show()
```

### OUTPUT
![download](https://github.com/user-attachments/assets/4ca9ba78-bb06-49d2-9801-551c9520f0a4)


### RESULT:
Thus the python program for linear and Polynomial Trend Estiamtion has been executed successfully.
