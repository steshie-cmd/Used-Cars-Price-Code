Project Title: Used Car Price Prediction Using XGBoost and SHAP
Description

This project implements a machine learning model to predict the prices of used cars based on various features such as mileage, engine size, model year, and fuel type. The model is built using XGBoost, a powerful gradient boosting technique. Additionally, SHAP (Shapley Additive Explanations) is used to explain the importance of each feature in the price predictions, providing insights into how the model works.

The final model is saved as a pickle file, and the SHAP values (feature importances) are extracted for analysis and visualization. The predictions and SHAP values can be used to create an interactive dashboard in Power BI.
Table of Contents

    Installation

    Usage

    Project Structure

    Results

    Contributing

    License

Installation

To run the code in this project, you'll need to install the required libraries. You can set up a virtual environment and install dependencies using pip.

    Clone the repository:

git clone https://github.com/your-username/used-car-price-prediction.git
cd used-car-price-prediction

Set up a virtual environment (optional but recommended):

python -m venv venv
source venv/bin/activate   # For macOS/Linux
venv\Scripts\activate      # For Windows

Install required libraries:

    pip install -r requirements.txt

Dependencies:

    pandas: For data manipulation.

    numpy: For numerical operations.

    xgboost: For building the predictive model.

    scikit-learn: For preprocessing and model evaluation.

    shap: For model explanation and feature importance.

    matplotlib: For visualizations.

To install the necessary libraries manually:

pip install pandas numpy xgboost scikit-learn shap matplotlib

Usage

    Prepare your dataset: Ensure that your dataset is in CSV format and contains relevant columns like price, mileage, engine size, and model year.

    Run the Python script:

        The script first loads and cleans the dataset by handling missing values and removing outliers.

        It then trains an XGBoost model to predict car prices.

        After training, SHAP values are computed to explain the feature importance in the price predictions.

        Finally, the trained model is saved as a pickle file, and SHAP values are exported to a CSV file.

    python car_price_prediction.py

    Generate SHAP explanations:

        Once you have the SHAP values, you can visualize the importance of each feature and gain insights into how the model works.

        You can use SHAP's summary plot and other visualization techniques.

    Upload the model to Power BI:

        Import the pickle file into Power BI for predictions or analysis.

        Use the SHAP values CSV file in Power BI to create feature importance visualizations.

Example Output:

    R²: 0.42

    RMSE: 4559.87 euros

    MAE: 3718.41 euros

    SHAP Summary Plot: Visual representation of feature importance.

Project Structure

used-car-price-prediction/
├── car_price_prediction.py      # Main Python script for data processing, model training, and SHAP value extraction.
├── xgb_model.pkl                # Pickle file containing the trained XGBoost model.
├── requirements.txt             # List of required Python libraries.
└── README.md                    # Project overview and instructions.

Results

The model was able to predict car prices with an R² of 0.42, indicating that the model explains about 42% of the variance in the car prices. The RMSE was 4559.87 euros, and the MAE was 3718.41 euros, providing a sense of prediction accuracy.

SHAP values were extracted to explain the feature importance:

    Mileage and Model Year were found to be the most significant features influencing car price predictions.

    The SHAP summary plot and other visualizations help explain how each feature impacts the model's decision.
