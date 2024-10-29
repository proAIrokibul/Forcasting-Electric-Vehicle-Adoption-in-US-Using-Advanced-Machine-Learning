# Forcasting-Electric-Vehicle-Adoption-in-US-Using-Advanced-Machine-Learning
## Dataset Overview
The dataset used in this project consists of various attributes related to electric vehicles (EVs) registered in the USA. It contains a total of **205,439** entries, with features including:

- **VIN**: Unique identifier for each vehicle
- **County, City, State**: Geographic location of registration
- **Model Year**: Year the vehicle model was manufactured
- **Make and Model**: Manufacturer and model of the vehicle
- **Electric Vehicle Type**: Classification of the EV
- **Clean Alternative Fuel Vehicle (CAFV) Eligibility**: Indicates eligibility for alternative fuel vehicle programs
- **Electric Range**: Maximum distance the vehicle can travel on a single charge
- **Base MSRP**: Manufacturer's suggested retail price, which is the target variable for prediction
- **Legislative District, Electric Utility, 2020 Census Tract**: Additional contextual information

The dataset was cleaned and preprocessed to handle missing values, categorical variables, and data types, ensuring its readiness for analysis and modeling.

## Methodology
The project follows a systematic approach to model the relationship between the features of electric vehicles and their base MSRP. The methodology is outlined as follows:

1. **Data Preprocessing**:
   - Handled missing values by excluding rows with significant gaps in critical features.
   - Categorical variables were transformed using **OneHotEncoding** to convert them into numerical format, facilitating the modeling process.
   - The dataset was split into training and testing sets to evaluate the performance of the models effectively.

2. **Model Selection**:
   Three regression algorithms were chosen for this analysis:
   - **Linear Regression**: A simple model to establish a baseline for performance.
   - **Random Forest Regressor**: An ensemble method that improves prediction accuracy through multiple decision trees.
   - **Gradient Boosting Regressor**: Another ensemble technique that builds models sequentially to optimize predictive performance.

3. **Model Evaluation**:
   Each model was assessed using two key metrics:
   - **Mean Squared Error (MSE)**: Measures the average squared difference between predicted and actual values. Lower values indicate better performance.
   - **R-squared**: Indicates the proportion of variance in the target variable that can be explained by the features. Values closer to 1 signify a better fit.

## Model Performance
The performance of the models is summarized as follows:

### 1. Linear Regression
- **Mean Squared Error (MSE):** 57,811,216.70
- **R-squared:** 0.0023  
Despite being a fundamental regression approach, this model struggled to accurately predict the Base MSRP, indicating that the linear relationship assumption may not hold for this dataset.

### 2. Random Forest Regressor
- **Mean Squared Error (MSE):** 791,551.15
- **R-squared:** 0.9863  
This model excelled in capturing complex relationships within the data, providing accurate predictions and demonstrating its robustness against overfitting.

### 3. Gradient Boosting Regressor
- **Mean Squared Error (MSE):** 6,647,668.83
- **R-squared:** 0.8853  
While slightly less accurate than the Random Forest Regressor, the Gradient Boosting model still performed admirably, balancing prediction accuracy and interpretability.

## Conclusion
The analysis underscores the potential of machine learning models in predicting the Base MSRP of electric vehicles based on various features. The Random Forest Regressor emerged as the most effective model, showcasing its ability to generalize well to new data. Future work may explore further feature engineering, hyperparameter tuning, and model validation techniques to enhance predictive performance.
