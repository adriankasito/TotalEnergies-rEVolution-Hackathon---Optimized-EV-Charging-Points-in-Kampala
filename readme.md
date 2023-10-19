# Nairobi Bus Ticket Sales Prediction Project

## Technical Summary

### Framing the Problem

The primary objective of the Nairobi Bus Ticket Sales Prediction Project was to develop a predictive model that could estimate the number of tickets sold for different bus rides in Nairobi. This project aimed to provide insights into the factors affecting ticket sales, improve operational planning, and enhance the overall efficiency of the bus service.

### Data Preparation and Feature Engineering

#### Feature Selection

During the data preparation phase, several data preprocessing steps were taken, including feature selection. Variables with little variation and limited meaningful information were dropped from the dataset to improve model efficiency.

#### Creation of New Features

A significant aspect of the project involved the creation of new features that could better capture the dynamics of bus ticket sales. These new features included:

- **Distance to Nairobi**: Calculating the distance of each ride from Nairobi city center.
- **Bus Time Gap Intervals**: Determining the time intervals between bus rides.
- **Time to Reach Origin**: Estimating the time required for each bus to reach its origin.
- **Speed**: Calculating the speed of each bus during its journey.

#### Categorical Encoding Mastery

To handle categorical variables such as the day of the week and the month, one-hot encoding was applied. This technique allowed the model to effectively interpret these variables in a numerical format.

### Model Selection, Hyperparameter Tuning, and Evaluation

#### XGBoost Efficacy

After thorough investigation, it was found that the relationship between the dependent variable (ticket sales) and the independent variables was nonlinear. Consequently, traditional linear models would be inadequate for this task. The XGBoost algorithm was selected due to its ability to model nonlinear relationships effectively.

#### Hyperparameter Optimization

To ensure that the XGBoost model performed optimally, a rigorous process of hyperparameter tuning was carried out. GridSearchCV, a systematic approach for identifying the best hyperparameters (e.g., max_depth, learning_rate, and n_estimators) for the XGBoost model, was employed. The grid search was configured to minimize the negative mean absolute error (MAE), a key performance metric.

#### Rigorous Evaluation Metrics

The Mean Absolute Error (MAE) was chosen as the primary evaluation metric to assess the model's predictive accuracy. In addition to MAE, the R-squared (R2) metric was used to measure the model's capacity to explain the variance in the target variable. The model was evaluated both during training and testing phases, and the MAE and R2 values were recorded to assess its performance.

### Feature Importance

#### Feature Importance Insights

An analysis of feature importance was conducted to identify the key factors that had the most significant influence on predicting ticket sales. The results provided insights into which features played a pivotal role in influencing ticket sales. These insights could help in making informed decisions about business operations and marketing strategies.

## Lessons Learned

The Nairobi Bus Ticket Sales Prediction Project provided valuable insights and lessons, including:

1. **XGBoost Overfitting**: It was observed that the XGBoost model had a tendency to overfit the data. To address this, the ratios of the Train and Test Sets were adjusted, ensuring a more balanced and robust model.

2. **Creation of Additional Features**: To further improve model accuracy, the creation of additional features, such as hourly traveler counts and categorization of months into high, low, and medium traffic periods, was recommended. These additional features could potentially result in a lower MAE, enhancing the model's predictive capabilities.

This project demonstrated the power of data-driven decision-making and the importance of selecting appropriate machine learning models for complex, nonlinear relationships. It also highlighted the significance of feature engineering and hyperparameter tuning in achieving accurate predictions.

By implementing the lessons learned and further enhancing the model, the Nairobi Bus Ticket Sales Prediction Project has the potential to provide even more valuable insights and drive improvements in the bus service operations.

Mean Absolute Error (Train): 1.1939
Mean Absolute Error (Test): 2.9065
