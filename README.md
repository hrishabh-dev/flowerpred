# Iris Prediction Flask App

A Flask web application for predicting the species of Iris flowers based on input measurements using a pre-trained machine learning model.

## Table of Contents
- [Introduction]
- [Features]
- [Technologies Used]
- [Installation]
- [Usage]
- [API Endpoints]
- [Model Description]
- [Example]
- [License]
- [Acknowledgments]

## Introduction
This application utilizes machine learning algorithms to classify Iris flower species based on features like sepal length, sepal width, petal length, and petal width. The model is built using the Iris dataset and demonstrates how to deploy machine learning models in a web application using Flask.

## Features
- User-friendly web interface for entering flower measurements.
- Real-time predictions of Iris species.
- Simple and efficient REST API for integration with other applications.
- Displays prediction results with visual representation.

## Technologies Used
- Flask: Python web framework for building the application.
- Scikit-learn: Machine learning library for model training and prediction.
- Pandas & NumPy: Data manipulation and numerical operations.
- HTML/CSS & JavaScript: Frontend for user interaction.
- Jupyter Notebook: For model development and testing (if applicable).

## Installation
To set up this application locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/iris-prediction-flask-app.git
    cd iris-prediction-flask-app
    ```

2. Create a virtual environment (optional but recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Run the app:
    ```bash
    python app.py
    ```

5. Open your browser and go to `http://127.0.0.1:5000`.

## Usage
To use the application, input the sepal length, sepal width, petal length, and petal width into the form fields on the homepage and click the "Predict" button. The application will display the predicted species of the Iris flower.

## API Endpoints
The application exposes a RESTful API for making predictions.

### Predict Endpoint
- **URL**: `/predict`
- **Method**: `POST`
- **Request Body**: 
    ```json
    {
        "sepal_length": 5.1,
        "sepal_width": 3.5,
        "petal_length": 1.4,
        "petal_width": 0.2
    }
    ```
- **Response**:
    ```json
    {
        "species": "Iris-setosa"
    }
    ```

## Model Description
The model is trained using the Iris dataset from the UCI Machine Learning Repository. It uses [insert the type of model used, e.g., Decision Tree, Random Forest, etc.], achieving [insert accuracy or performance metrics].

## Example
#### To make a prediction using the API, you can use `curl`:
```bash
curl -X POST http://127.0.0.1:5000/predict -H "Content-Type: application/json" -d '{"sepal_length": 5.1, "sepal_width": 3.5, "petal_length": 1.4, "petal_width": 0.2}'
