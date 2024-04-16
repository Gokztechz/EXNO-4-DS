# EXNO:4-DS
# AIM:
To read the given data and perform Feature Scaling and Feature Selection process and save the
data to a file.

# ALGORITHM:
STEP 1:Read the given Data.
STEP 2:Clean the Data Set using Data Cleaning Process.
STEP 3:Apply Feature Scaling for the feature in the data set.
STEP 4:Apply Feature Selection for the feature in the data set.
STEP 5:Save the data to the file.

# FEATURE SCALING:
1. Standard Scaler: It is also called Z-score normalization. It calculates the z-score of each value and replaces the value with the calculated Z-score. The features are then rescaled with x̄ =0 and σ=1
2. MinMaxScaler: It is also referred to as Normalization. The features are scaled between 0 and 1. Here, the mean value remains same as in Standardization, that is,0.
3. Maximum absolute scaling: Maximum absolute scaling scales the data to its maximum value; that is,it divides every observation by the maximum value of the variable.The result of the preceding transformation is a distribution in which the values vary approximately within the range of -1 to 1.
4. RobustScaler: RobustScaler transforms the feature vector by subtracting the median and then dividing by the interquartile range (75% value — 25% value).

# FEATURE SELECTION:
Feature selection is to find the best set of features that allows one to build useful models. Selecting the best features helps the model to perform well.
The feature selection techniques used are:
1.Filter Method
2.Wrapper Method
3.Embedded Method

# CODING AND OUTPUT:
```
import pandas as pd
from scipy import stats
import numpy as np
import seaborn as sns
```
```
df=pd.read_csv("/content/bmi (1).csv")
df1=pd.read_csv("/content/bmi (1).csv")
df2=pd.read_csv("/content/bmi (1).csv")
df3=pd.read_csv("/content/bmi (1).csv")
df4=pd.read_csv("/content/bmi (1).csv")
```
```
df.head()
```
![Screenshot 2024-04-16 160612](https://github.com/Anusharonselva/EXNO-4-DS/assets/119405600/b679364c-c039-40bf-8969-2ce47e4cee22)
```
df.dropna()
```
![Screenshot 2024-04-16 160729](https://github.com/Anusharonselva/EXNO-4-DS/assets/119405600/21e2db4c-16f2-408f-9436-083db5f334ba)
```
max_vals = np.max(np.abs(df[['Height','Weight']]))
max_vals
```
![Screenshot 2024-04-16 160814](https://github.com/Anusharonselva/EXNO-4-DS/assets/119405600/0be461e2-d30f-4344-b946-ba1890a06fd8)
```
from sklearn.preprocessing import StandardScaler
sc=StandardScaler()
df1[['Height','Weight']]=sc.fit_transform(df1[['Height','Weight']])
df1.head(10)
```
![Screenshot 2024-04-16 160849](https://github.com/Anusharonselva/EXNO-4-DS/assets/119405600/7237e9e5-ae88-494a-a907-5ff2da9316b2)
```
from sklearn.preprocessing import MinMaxScaler
```
```
scaler = MinMaxScaler()
df[['Height','Weihgt']]=scaler.fit_transform(df[['Height','Weight']])
df.head(10)
```
![Screenshot 2024-04-16 160943](https://github.com/Anusharonselva/EXNO-4-DS/assets/119405600/ff65fe24-96bd-408b-83a9-6b193b352f86)
```
from sklearn.preprocessing import Normalizer
scaler = Normalizer()
df2[['Height','Weight']]=scaler.fit_transform(df2[['Height','Weight']])
df2
```
![Screenshot 2024-04-16 161036](https://github.com/Anusharonselva/EXNO-4-DS/assets/119405600/7eaea797-2848-402b-a1f9-e5b192a0bbcc)
```

# RESULT:
       # INCLUDE YOUR RESULT HERE
