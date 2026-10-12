California Housing Price Prediction

Project Overview

This project builds a machine learning model to predict median house values using the California Housing dataset. It demonstrates a complete introductory regression workflow, from data exploration and preprocessing to model training, evaluation, and hyperparameter tuning.

Objectives

- Explore and inspect the dataset using Pandas.
- Split data into training and testing sets.
- Establish a baseline using DummyRegressor.
- Train and compare Linear Regression and Random Forest models.
- Evaluate models using MAE, RMSE, and R².
- Analyze feature importance and prediction errors.
- Tune Random Forest hyperparameters using 5-fold cross-validation.

Dataset

The project uses the California Housing dataset provided by scikit-learn.

- Samples: 20,640
- Input features: 8
- Target: "MedHouseVal"
- Target units: Hundreds of thousands of US dollars.

Note: This dataset represents California housing data and should not be treated as a model for estimating property prices in Egypt.

Models and Results

Model| MAE| RMSE| R²
Dummy Baseline| 0.9061| 1.1449| -0.0002
Linear Regression| 0.5332| 0.7456| 0.5758
Random Forest (initial)| 0.3275| 0.5053| 0.8051
Random Forest (tuned)| 0.3267| 0.5041| 0.8061

The tuned Random Forest model achieved the best test results among the evaluated models.

Feature Importance

The initial Random Forest model identified "MedInc" as the most important feature, followed by "AveOccup", "Latitude", and "Longitude".

Feature importance indicates how useful features were to the model's predictions; it does not establish causal relationships.

Hyperparameter Tuning

RandomizedSearchCV was used with 5-fold cross-validation to explore Random Forest configurations.

Best parameters:

- "n_estimators": 100
- "max_depth": 25
- "min_samples_leaf": 2
- "max_features": 0.7

Best cross-validation MAE: 0.3325.

Technologies

- Python
- Pandas
- NumPy
- scikit-learn
- Google Colab
- Git and GitHub

Key Learnings

- Regression modeling and train-test splitting.
- Baseline evaluation and model comparison.
- Regression metrics: MAE, RMSE, and R².
- Feature importance and error analysis.
- Cross-validation and hyperparameter tuning.

Limitations

- The dataset is specific to California.
- The model's performance depends on the available dataset and features.
- Feature importance should not preted as causation.
- Test results do not guarantee performance on other datasets or locations.

Future Improvements

- Build a reusable prediction pipeline.
- Add automated tests and clearer project structure.
- Create a small prediction API using FastAPI.
- Experiment with additional models and validation strategies.

Author

Mohab Ashraf

This project was developed as part of my practical learning journey in Machine Learning and AI Engineering.
