# housingpriceprediciton
DS 340W Research Project: Housing Price Prediction Model

## Setup Guide

### Installation

1. Install required dependencies:
```bash
pip install -r requirements.txt
```

2. Ensure you have the dataset file `AmesHousing.csv` in the project root directory.

### Running the Notebooks

1. **Start with data preparation**: Run `Data_Preparation.ipynb` first to generate `final.csv` (the cleaned dataset used by all models).

2. **Run model notebooks**: Execute each modeling notebook in any order. Each notebook is self-contained and loads `final.csv`.

3. **View results**: Model performance metrics are printed in each notebook's output cells after training.

### Where to Find Model Performance Metrics

Model performance metrics appear in the **output cells** of each notebook after running the training cells. Look for:

- **R² Score**: Coefficient of determination (higher is better, max 1.0)
- **Adjusted R²**: R² adjusted for number of features
- **RMSE**: Root Mean Squared Error (lower is better)
- **MAE**: Mean Absolute Error (lower is better)
- **5-fold CV Score**: Cross-validation accuracy percentage

**Example locations:**
- `Linear_Regression_Model.ipynb`: Cell 5 and Cell 12 outputs
- `Random_Forest_Model.ipynb`: Cell 4 and Cell 11 outputs
- `XGBoost_Model.ipynb`: Cell 5 and Cell 12 outputs
- `Lasso_Regression_Model.ipynb`: Cell 3 and Cell 4 outputs
- `Keras_ANN_Model.ipynb`: Cell 4 and Cell 5 outputs
- `Support_Vector_Regression_Model.ipynb`: Cell 5 and Cell 10 outputs
- `Multilayer_Perceptron_Model.ipynb`: Cell 5 and Cell 12 outputs

Each notebook also includes visualization plots (actual vs predicted prices, residual distributions) and SHAP feature importance plots at the end.

## Modeling Notebooks
- `Data_eda.ipynb`: exploratory data analysis and visualization of the Ames dataset.
- `Data_Preparation.ipynb`: full cleaning, feature engineering, and export of `final.csv`.
- `Linear_Regression_Model.ipynb`: baseline linear model plus SHAP explanations.
- `Random_Forest_Model.ipynb`: tree ensemble benchmark with SHAP feature importances.
- `XGBoost_Model.ipynb`: boosted trees with tuned hyperparameters and SHAP plots.
- `Support_Vector_Regression_Model.ipynb`: kernel-based regressor + SHAP.
- `Multilayer_Perceptron_Model.ipynb`: scikit-learn neural net experiments.
- `Lasso_Regression_Model.ipynb`: sparse linear workflow (baseline + tuned + SHAP).
- `Keras_ANN_Model.ipynb`: TensorFlow ANN comparisons (basic + advanced + SHAP).
