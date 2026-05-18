# Ex.No: 02 LINEAR AND POLYNOMIAL TREND ESTIMATION
## Date : 02-05-2026
### AIM:
To Implement Linear and Polynomial Trend Estiamtion Using Python.

### ALGORITHM:
Import necessary libraries (NumPy, Matplotlib)

Load the dataset

Calculate the linear trend values using least square method

Calculate the polynomial trend values using least square method

End the program
### PROGRAM:
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Load dataset
data = pd.read_csv("dataset.csv")

# Select temperature column
y = data["temp_mean(c)"].values
x = np.arange(len(y))

# A. Linear Trend Estimation
coeffs_linear = np.polyfit(x, y, 1)
linear_trend = np.polyval(coeffs_linear, x)

plt.figure(figsize=(10,5))
plt.plot(x, y, label="Original Data")
plt.plot(x, linear_trend, label="Linear Trend")
plt.title("Linear Trend Estimation (Temperature)")
plt.xlabel("Time")
plt.ylabel("Temperature")
plt.legend()
plt.show()


# B. Polynomial Trend Estimation
coeffs_poly = np.polyfit(x, y, 2)
poly_trend = np.polyval(coeffs_poly, x)

plt.figure(figsize=(10,5))
plt.plot(x, y, label="Original Data")
plt.plot(x, poly_trend, label="Polynomial Trend (Degree 2)")
plt.title("Polynomial Trend Estimation (Temperature)")
plt.xlabel("Time")
plt.ylabel("Temperature")
plt.legend()
plt.show()

# Coefficients
print("Linear coefficients:", coeffs_linear)
print("Polynomial coefficients:", coeffs_poly)
```
### OUTPUT
A - LINEAR TREND ESTIMATION
<img width="988" height="531" alt="image" src="https://github.com/user-attachments/assets/6aec43c4-c52a-44f4-b411-45746b7ff160" />

B- POLYNOMIAL TREND ESTIMATION
<img width="1018" height="579" alt="image" src="https://github.com/user-attachments/assets/36cf724f-50a0-4b84-8fb2-937268cd3494" />

### RESULT:
Thus the python program for linear and Polynomial Trend Estiamtion has been executed successfully.
