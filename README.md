# Car Price Prediction

This project predicts the price of used cars using a machine learning model. It includes a complete pipeline from data preprocessing and exploratory data analysis to model training, evaluation, and deployment with a user-friendly web interface.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Model Training Pipeline](#model-training-pipeline)
- [User Interface](#user-interface)

## Features

- **Data Preprocessing**: Handles missing values, encodes categorical features, and scales numerical features.
- **Feature Engineering**: Creates new features like `car_age`, `mileage_per_year`, and `motor_efficiency` to improve model performance.
- **Exploratory Data Analysis (EDA)**: Visualizes the data to understand the distribution of car prices and the relationship between different features.
- **Advanced Modeling**:
    - Implements and tunes an **XGBoost** model.
    - Builds an **Ensemble Model** combining `XGBoost`, `RandomForest`, and `Ridge` regression for improved accuracy.
- **Outlier Detection**: Removes outliers from the dataset to prevent them from skewing the model's predictions.
- **Web Interface**: A user-friendly interface built with **Gradio** to predict car prices in real-time.

## Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook or JupyterLab

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/mgunawardhana/car_price_prediction.git](https://github.com/mgunawardhana/car_price_prediction.git)
    cd car_price_prediction
    ```

2.  **Install the required libraries:**
    ```bash
    pip install pandas numpy xgboost scikit-learn matplotlib seaborn gradio
    ```

## Usage

1.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
2.  Open the `car_price_prediction.ipynb` notebook.
3.  Place your `train.csv` and `test.csv` files in the specified path within the notebook, or modify the path to your data files.
4.  Run the cells in the notebook to train the model and launch the Gradio interface.

## Model Training Pipeline

The model is trained using the following steps:

1.  **Load Data**: The training and testing data is loaded from CSV files.
2.  **Exploratory Data Analysis**: EDA is performed to gain insights from the data.
3.  **Data Preprocessing**: The data is cleaned, and features are engineered and preprocessed.
4.  **Outlier Removal**: Outliers are removed to create a more robust model.
5.  **Model Training**: An XGBoost model and an ensemble model are trained on the preprocessed data.
6.  **Model Evaluation**: The models are evaluated using Mean Absolute Error (MAE) and R-squared (R²) metrics.
7.  **Final Prediction**: The best-performing model is used to make predictions on the test data.

## User Interface

The project includes an interactive web UI built with Gradio.

### How to use the UI:

1.  Run the `car_price_prediction.ipynb` notebook to launch the UI.
2.  Enter the car details in the input fields.
3.  Click the "Predict Price" button to get the estimated price of the car.
