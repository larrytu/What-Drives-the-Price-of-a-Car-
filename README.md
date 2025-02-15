# What-Drives-the-Price-of-a-Car-

# Report

## 1. Introduction

**Project Purpose:**  
The data problem is to create a model using a 426K dataset of used cars information with price as the target variable. The dataset includes features such as the make, model, year, mileage/odometer, fuel, and condition which could influence the market value. By analyzing these predictors, we aim to quantify their impact on the market price and create a model that can accurately estimate their value. This approach helps identify key factors driving the cost of used cars.

---

## 2. Methodology

### Data Cleaning & Preparation
- Missing data was handled by performing median and mode imputations.
- Pipelines were created for scaling and encoding the data, using `StandardScaler` and `OneHotEncoder`.

### Model Selection
- Two models were used: **Linear Regression** and **RandomForestRegressor**.

### Train/Test Split
- An 80/20 train/test split was performed.
- **X** includes all features excluding `price`, and **y** is the target (`price`).

---

## 3. Model Evaluation

**Performance Metrics:**

| Model             | MSE                  | RMSE                | MAE                 |
|-------------------|----------------------|---------------------|---------------------|
| LinearRegression  | 7.393341729739356    | 2.719070011923076   | 1.6457987934940967  |
| RandomForest      | 3.911067398361335    | 1.977641878187589   | 0.868464645252388   |

---

## 4. Results

Based on the metrics above, the **RandomForest** model shows a lower MSE, RMSE, and MAE compared to the **LinearRegression** model, indicating more accurate predictions. Feature importance analysis in the RandomForest model revealed that **miles per year** is the most significant predictor, suggesting that higher mileage typically lowers the market price. The second most important features were the **condition** of the car and the **model year**.

---

## 5. Conclusion

The **RandomForest** model performed best with lower error metrics overall. The most important features (mileage, condition, and model year) align with expectations for what drives used car pricing. Future improvements could include experimenting with additional model types or hyperparameter tuning to further enhance accuracy.
