# House-Price-Prediction
### Predicting House Price (Kaggle Competition Project)

<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/House-Image.jpg" width=600>

---

## Overview:
* This is a Kaggle Competition Project.
* **Train** and **Test** Dataset has almost same no. of columns and rows **(1460,81)**.
* Various Techniques like **Target Guided Encoding**, **logarithmic transformation technique**, **StandardScaler**. **Hyperparameter-tuning** etc. have been used.
* Algorithms like **RandomForestRegressor**, **Linear Regression**, **SVR**, **GradientBoostingRegressor** and **ANN** have been applied.

---

## Data Gathering:
* This is a Kaggle Competition Project. 

* **Dataset:** https://www.kaggle.com/c/house-prices-advanced-regression-techniques 

### Dataset:
* **Train** and **Test** Dataset have almost same no. of columns and rows **(1460,81)**.  
* **Dataset has 81 columns:**
'Id', 'MSSubClass', 'MSZoning', 'LotFrontage', 'LotArea', 'Street','Alley', 'LotShape', 'LandContour', 'Utilities', 'LotConfig','LandSlope', 'Neighborhood', 'Condition1','Condition2', 'BldgType','HouseStyle', 'OverallQual', 'OverallCond', 'YearBuilt', 'YearRemodAdd','RoofStyle', 'RoofMatl', 'Exterior1st', 'Exterior2nd', 'MasVnrType','MasVnrArea', 'ExterQual', 'ExterCond', 'Foundation', 'BsmtQual','BsmtCond', 'BsmtExposure', 'BsmtFinType1', 'BsmtFinSF1','BsmtFinType2', 'BsmtFinSF2', 'BsmtUnfSF', 'TotalBsmtSF', 'Heating','HeatingQC', 'CentralAir', 'Electrical', '1stFlrSF', '2ndFlrSF','LowQualFinSF', 'GrLivArea', 'BsmtFullBath', 'BsmtHalfBath', 'FullBath','HalfBath', 'BedroomAbvGr', 'KitchenAbvGr', 'KitchenQual','TotRmsAbvGrd', 'Functional', 'Fireplaces', 'FireplaceQu', 'GarageType','GarageYrBlt', 'GarageFinish', 'GarageCars', 'GarageArea', 'GarageQual','GarageCond', 'PavedDrive', 'WoodDeckSF', 'OpenPorchSF','EnclosedPorch', '3SsnPorch', 'ScreenPorch', 'PoolArea', 'PoolQC','Fence', 'MiscFeature', 'MiscVal', 'MoSold', 'YrSold', 'SaleType','SaleCondition', 'SalePrice'.

* You can find out the description about these columns in data_description file.

<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/Dataset.png" width=800>

---

## Feature Engineering:
* To understand it in more detail go to **[House-Price-Prediction.ipynb](https://github.com/manthanpatel98/House-Price-Prediction/blob/master/House-Price-Prediction.ipynb)**

### A. Handling Missing Values:
* Here, there are several columns that has higher NULL values.
<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/Missing.png" width=500>

* So, I have dropped those columns that have more than 10% NULL values.
* In **Categorical Columns**, I have replaced NULL value with **"Missing"** word.
* In **Numerical Columns**, I have replaced NULL values with the **Mean** of that perticular Column.

### B. Feature Encoding:
* Here, I have used **Target Guided Encoding**.
* Basically according to the categorical label group, **Mean of the 'SalePrice'** is computed and then it is given **index** which then **replaces** the value of that perticular **label group**. 

### C. Feature Transformation:
* In the Dataset, there are several columns like **'LotArea'**, **'1stFlrSF'**, **'GrLivArea'**,**'SalePrice'** that are not Gaussian Distributed.
* For that **Logarithmic Technique** of converting distribution into **Gaussian Distribution** has been used.

### D. Feature Scaling:
* For Scaling, **StandardScaler** has been applied.

---

## Feature Selection:
* In Feature Selection, initially i have used Select K best and have tried plying with number of columns.
* Here, i have taken the help of **Correlation matrix**.

---

## Applied Algorithms & Results:
### 1. RandomForestRegressor:
* **RandomForestRegressor** has been applied with **Hyperparameter-tuning**.
* **Results for RandomForestRegressor:**
<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/RFR1.png" width=500>

<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/RFR2.png" width=500>


### 2. Linear Regression:
* **Results for Linear Regression:**
<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/Lin1.png" width=500>

<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/Lin2.png" width=500>


### 3. SVR:
* **Results for SVR:**
<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/SVR1.png" width=500>

<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/SVR2.png" width=500>


### 4. GradientBoostingRegressor:
* **Results for GradientBoostingRegressor:**
<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/GBR1.png" width=500>

<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/GBR2.png" width=500>


### 4. ANN:
* **Results for ANN:**
<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/ANN1.png" width=500>

<img src="https://github.com/manthanpatel98/House-Price-Prediction/blob/master/README-Resources/ANN2.png" width=500>

---

### Algorithm & R2 Score:

| Algorithm | R2 Score |
| ---- | ---- |
| RandomForestRegressor | -0.08 |
| Linear Regression | 0.09 |
| SVR | 0.15 |
| GradientBoostingRegressor | 0.15 |
| ANN | 0.24 |

* Here, Our model is not ideally fitted but it gives good results.
* Among all Algorithms discussed, **ANN** has given better results as compare to other algorithms.

---




