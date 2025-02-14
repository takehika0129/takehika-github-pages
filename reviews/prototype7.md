---
title: "Build a Simple Regression Model in Python (2025/02/15)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no7-simple-regression-model)](https://github.com/takehika0129/no7-simple-regression-model)

# **Concept**
This project focuses on building a simple regression model using the **California Housing dataset** to predict house prices.


# **Features**
- **📊 Data Preprocessing**: The dataset is preprocessed using `pandas` and standardized using `StandardScaler` to ensure better model performance.
- **🔢 Model Comparison**: Implements both `LinearRegression` and `RandomForestRegressor` to observe differences in predictive accuracy.
- **📈 Performance Evaluation**: Uses `mean_squared_error` and `r2_score` to assess how well each model fits the data.
- **🎨 Visualization**: Scatter plots by `matplotlib` compare actual vs predicted values for both models.


# **Challenges & Solutions**  
- **Choosing the Right Model**: Initially, `LinearRegression` showed poor performance due to non-linearity in the dataset. Introducing `RandomForestRegressor` improved accuracy by capturing complex patterns.
- **Interpreting Results**: To ensure fair comparison, both models were evaluated on `mean_squared_error` and `r2_score`, making it clear that Random Forest outperforms Linear Regression.

  
# **Future Improvements**
- **Hyperparameter Tuning**: Optimizing the Random Forest model parameters to enhance predictive accuracy.

---
[Back to All Prototypes](../index.md)
