# Crop_Yied_Prediction_model_61
# Crop_Model
Documentation Defining Objective: Our project predicts crop yield using factors like crop type, year, season, state, area, production, rainfall, fertilizer, and pesticide usage, aiming to help farmers optimize resources and plan effectively.

Importing Necessary Libraries Data Acquisition: The dataset (crop_yield_data.csv) includes vital features: Crop, Year, Season, State, Area, Production, Rainfall, Fertilizer, Pesticide, and Yield (the target variable).

Data Preprocessing: It ensures that our data is cleaned, rows with missing values are removed, and only critical features are selected. WE used a preprocessing pipeline that standardizes numeric features i.e. StandardScaler and encoded we our categorical features with OneHotEncoder.

Creating a pipeline Creating a single pipeline helped us streamline workflows by automating sequential tasks such as feature selection, and model training, ensuring consistent data transformations across train, validation and test sets. They also helped us in simplifying hyperparameter.

Within the Pipeline Model Selection After rigorous walkthrough and much reasoning, we selected and implemented three models for crop yield prediction:

Linear Regression: Chosen for understanding the relationships between variables

Ridge Regression: Implemented to prevent overfitting.

Random Forest Regressor: Selected for its robustness in handling diverse agricultural data and capturing non-linear relationships.

Train-Validation-Test Split: Our data is split into 80:10:10, training set has 80%, validation size (10%), and test 10% of the sets, ensuring models are rigorously evaluated.

Hyperparameter Optimization: We did Hyperparameter tuning to ensure that models capture the data's nuances well and used following search methods RandomizedSearchCV and GridSearchCV for Random Forest and Ridge respectively

Evaluation: We applied 5-fold cross-validation with purpose of ensuring model stability, with metrics such as:

1.) Median Absolute Error (MedAE): Offers robustness against outliers.

2.) Mean Squared Error (MSE): Measures average squared errors, emphasizing larger errors.

3.) R-Squared (R²): Indicates how well the model explains variance.

4.) RMSE-: RMSE measures the square root of the average squared differences between predicted and actual values. The Random Forest Regressor, balancing these metrics, emerges as the most reliable model for accurate, real-world crop yield predictions.
