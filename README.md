# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import **Pandas** and the required module from **Scikit-learn**.
<br>

### Step2
Read the `carsemission.csv` dataset.
Select `Weight` and `Volume` as independent variables
<br>

### Step3
 Select `CO2` as the dependent variable.
 Create and train a Multivariate Linear Regression model.
<br>

### Step4
Select CO2 as the dependent variable.Create and train a Multivariate Linear Regression model.
<br>

### Step5
Display the predicted CO₂ emission.
<br>

## Program:
```
# Dataset Setup - Run this cell before starting the experiment
#developed by 
#POOJA SHREE K
#26018233
import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)



```








## Output:
<img width="842" height="702" alt="Screenshot 2026-11-25 091038" src="https://github.com/user-attachments/assets/20d5b383-a19a-43f3-acb5-53b7f67267be" />



## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
