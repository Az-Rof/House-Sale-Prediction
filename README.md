# House Sale Prediction
A comprehensive machine learning project to predict house prices using the King County Housing Dataset from Kaggle. This project applies data preprocessing, feature engineering, model training, evaluation, and visualization using the Gradient Boosting Regressor model.

## 📌 Project Overview
This project focuses on building a predictive model that estimates house prices based on various features such as square footage, number of bedrooms, number of bathrooms, building grade, location, and more.
The workflow includes:
* Loading and preparing the dataset
* Feature extraction & preprocessing
* Training a machine learning model
* Evaluating model performance
* Visualizing predictions and feature importance
* Demonstrating real prediction examples

## 📂 Dataset
The dataset used is the King County House Sales Dataset, containing 21,613 rows and 21 columns.
It includes features like:
- bedrooms, bathrooms
- sqft_living, sqft_lot
- floors, waterfront, view, condition
- grade
- sqft_above, sqft_basement
- yr_built, yr_renovated
- zipcode, lat, long
- price (target column)
The dataset is automatically downloaded via kagglehub.

## 🧹 Data Preparation
Key preprocessing steps:
- Convert date to datetime format
- Extract sale_year and sale_month
- Drop unnecessary columns (id, date)
- Split data into training and testing sets
- After preprocessing, the model uses 20 numerical features.

## 🤖 Model Used
Gradient Boosting Regressor
Chosen because of its strong performance on regression tasks and ability to model complex non-linear relationships.
Model parameters:
GradientBoostingRegressor(
    n_estimators=100,
    learning_rate=0.1,
    max_depth=5,
    subsample=0.8,
    random_state=42
)

## 📊 Model Performance
After training and testing, the model achieves:
| Metric	| Score|
|------- | ---------|
| R² Score (Accuracy)	| 86.37% |
| RMSE |	143,547 |
| MAE	| 71,768 |
The model performs well and generalizes effectively.

## ⭐ Feature Importance
Top 5 most influential features:
- sqft_living – Living area size
- grade – Construction and design quality
- lat – Geographical latitude
- long – Geographical longitude
- yr_built – Year built
This confirms that location, size, and quality are the dominant factors influencing house prices.

## 📈 Visualizations
The notebook generates the following:
- Predicted vs Actual plot
- Residual plot
- Feature importance bar chart
- Error distribution
- Actual vs Predicted price distribution
- Metrics summary panel

## 🧪 Sample Prediction
A real example prediction is included in the notebook, showing:
- Model-predicted price
- Actual price
- Difference & error percentage
This demonstrates how the model behaves on unseen data.
