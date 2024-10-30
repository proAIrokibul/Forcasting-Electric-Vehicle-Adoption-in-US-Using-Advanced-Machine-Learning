# Forecasting Electric Vehicle Adoption in the U.S. Using Advanced Machine Learning

## Dataset Overview
The dataset utilized in this project comprises a comprehensive collection of attributes related to electric vehicles (EVs) registered in the United States. With a total of **205,439** entries, the dataset features the following key attributes:

- **VIN**: A unique identifier assigned to each vehicle, ensuring precise tracking and differentiation.
- **County, City, State**: Geographic identifiers indicating the location of vehicle registration.
- **Model Year**: The year in which the vehicle model was manufactured, providing context for technological advancements and market trends.
- **Make and Model**: Details regarding the manufacturer and specific model of the vehicle, essential for understanding brand influence on pricing.
- **Electric Vehicle Type**: Classification of the EV, which may influence consumer preferences and regulatory incentives.
- **Clean Alternative Fuel Vehicle (CAFV) Eligibility**: A binary indicator that signifies eligibility for programs supporting alternative fuel vehicles, impacting purchasing decisions.
- **Electric Range**: The maximum distance the vehicle can travel on a single charge, a critical factor for consumers when considering EVs.
- **Base MSRP**: The manufacturer's suggested retail price, serving as the target variable for prediction and essential for understanding market pricing.
- **Legislative District, Electric Utility, 2020 Census Tract**: Additional contextual variables that may impact EV adoption rates and pricing strategies.

Before analysis and modeling, the dataset underwent a thorough cleaning and preprocessing phase to address missing values, manage categorical variables, and ensure appropriate data types, thus optimizing it for further analysis.

## Methodology
The project adopts a structured approach to explore the relationship between electric vehicle attributes and their Base MSRP. The methodology includes the following steps:

1. **Data Preprocessing**:
   - **Handling Missing Values**: Rows with significant gaps in critical features were excluded to maintain data integrity.
   - **Encoding Categorical Variables**: Categorical variables were transformed using **OneHotEncoding**, converting them into a numerical format suitable for modeling.
   - **Data Splitting**: The dataset was partitioned into training and testing sets to enable effective performance evaluation of the selected models.

2. **Model Selection**:
   Three regression algorithms were selected for this analysis:
   - **Linear Regression**: A straightforward model employed as a baseline for performance comparison, providing a fundamental understanding of the data.
   - **Random Forest Regressor**: An ensemble method leveraging multiple decision trees to enhance prediction accuracy by capturing complex relationships within the data.
   - **Gradient Boosting Regressor**: Another ensemble technique that constructs models sequentially to optimize predictive performance, focusing on errors made by prior models.

3. **Model Evaluation**:
   The performance of each model was assessed using two critical metrics:
   - **Mean Squared Error (MSE)**: This metric quantifies the average squared difference between predicted and actual values, with lower values indicating superior performance.
   - **R-squared (R²)**: This statistic reflects the proportion of variance in the target variable explained by the features, with values closer to 1 indicating a better model fit.

## Model Performance
The results of the model evaluations are summarized as follows:

### Linear Regression
- **Mean Absolute Error (MAE)**: 1832.53  
- **Mean Squared Error (MSE)**: 57,811,216.70  
- **Root Mean Squared Error (RMSE)**: 7603.37  
- **R-squared (R²)**: 0.0023  

Despite its foundational nature, the linear regression model struggled to accurately predict Base MSRP, reflecting that the assumption of a linear relationship may not be appropriate for this dataset.

### Random Forest Regressor
- **Mean Absolute Error (MAE)**: 20.28  
- **Mean Squared Error (MSE)**: 791,551.15  
- **Root Mean Squared Error (RMSE)**: 889.69  
- **R-squared (R²)**: 0.9863  

The Random Forest Regressor excelled in capturing intricate relationships within the dataset, providing accurate predictions and demonstrating robustness against overfitting.

### Gradient Boosting Regressor
- **Mean Absolute Error (MAE)**: 519.94  
- **Mean Squared Error (MSE)**: 6,647,668.83  
- **Root Mean Squared Error (RMSE)**: 2578.31  
- **R-squared (R²)**: 0.8853  

Although slightly less accurate than the Random Forest Regressor, the Gradient Boosting model still performed admirably, effectively balancing prediction accuracy with interpretability.

## Conclusion
The analysis highlights the significant potential of advanced machine learning models in predicting the Base MSRP of electric vehicles based on various influential features. Among the models tested, the Random Forest Regressor emerged as the most effective, showcasing its capability to generalize well to new data. Future work may involve exploring further feature engineering, hyperparameter tuning, and implementing robust model validation techniques to enhance predictive performance. By doing so, this analysis could contribute to better understanding consumer behavior and market dynamics in the rapidly evolving electric vehicle sector.
