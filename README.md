# Early Flood Level Prediction using LSTM

## Project Overview

Early Flood Level Prediction using LSTM is a deep learning project that predicts future water levels using historical water-level readings.

The project uses a Long Short-Term Memory (LSTM) neural network to learn patterns from previous water-level data and predict the water level for the next hour. It also includes a simple early flood warning mechanism that compares the predicted water level against a predefined threshold.

## Objectives

- Analyze historical water-level patterns.
- Apply deep learning techniques for time-series forecasting.
- Predict the next hour's water level using previous readings.
- Compare actual and predicted water levels.
- Generate an early warning when the predicted water level reaches a specified threshold.

## Technologies Used

- **Python** – Programming language.
- **Google Colab** – Development environment.
- **NumPy** – Numerical operations.
- **Pandas** – Dataset creation and manipulation.
- **Matplotlib** – Data visualization.
- **Scikit-learn** – Data normalization and model evaluation.
- **TensorFlow / Keras** – Building and training the LSTM model.

## Dataset Description

The project uses a synthetically generated water-level dataset containing hourly readings for 100 days (2,400 records).

The water-level data is generated using:
- Sine functions to simulate periodic variations.
- A gradual increasing trend.
- Random noise to introduce variations.

**Note:** This project currently uses simulated data for demonstration and model development, rather than real-world river water-level measurements.

## Project Workflow

1. **Library Import:** Import the required Python libraries.
2. **Dataset Creation:** Generate sample hourly water-level readings for 100 days.
3. **Data Visualization:** Plot historical water-level variations.
4. **Data Preprocessing:** Split the dataset into 80% training data and 20% testing data. Normalize the values using MinMaxScaler.
5. **Sequence Creation:** Use the previous 24 hours of readings to predict the next hour.
6. **Model Building:** Construct an LSTM neural network.
7. **Model Training:** Train the model for 10 epochs with a batch size of 32.
8. **Water-Level Prediction:** Predict water levels using the testing dataset.
9. **Visualization:** Compare actual and predicted water levels.
10. **Model Evaluation:** Calculate MAE, MSE and RMSE.
11. **Next-Hour Prediction:** Predict the water level for the next hour using the latest 24 readings.
12. **Early Flood Warning:** Compare the predicted water level against a predefined warning threshold of 3 meters.

## LSTM Model Architecture

The project uses a Sequential LSTM model consisting of:

- **First LSTM Layer:** 50 units with tanh activation and return_sequences enabled.
- **Dropout Layer:** 20% dropout to help reduce overfitting.
- **Second LSTM Layer:** 50 units with tanh activation.
- **Dense Layer:** One output neuron to predict the next water level.

**Model Configuration:**
- Optimizer: Adam
- Loss Function: Mean Squared Error
- Epochs: 10
- Batch Size: 32
- Input Sequence Length: 24 hours

## Model Evaluation

The model's prediction performance is evaluated using:

- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values.
- **Mean Squared Error (MSE):** Measures the average squared prediction error.
- **Root Mean Squared Error (RMSE):** Measures the square root of the mean squared error.

The notebook also visualizes actual and predicted water levels using a line graph.

## Early Flood Warning Mechanism

The project uses a predefined warning threshold of **3.0 meters**.

- If the predicted water level is greater than or equal to 3 meters, the system displays a high-water-level warning.
- If the predicted water level is below 3 meters, the system displays a normal status.

This demonstrates a basic threshold-based warning mechanism.

## How to Run the Project

The project can be executed using Google Colab.

1. Clone or download this GitHub repository.
2. Open [Google Colab](https://colab.research.google.com/).
3. Upload the `.ipynb` notebook.
4. Run the notebook cells sequentially.
5. View the training results, prediction graphs, evaluation metrics and early warning message.

All required libraries are available in the standard Google Colab environment.

## Future Enhancements

- Integrate real-time river water-level data.
- Use historical flood datasets for model training.
- Experiment with different LSTM architectures and hyperparameters.
- Improve prediction accuracy using larger datasets.
- Develop a real-time flood monitoring and alert system.

## Conclusion

This project demonstrates the application of Long Short-Term Memory (LSTM) networks in time-series forecasting for water-level prediction. By learning patterns from previous readings, the model predicts future water levels and uses a threshold-based mechanism to identify potentially high-water-level conditions.

It provides a basic demonstration of how deep learning techniques can contribute to early flood monitoring and warning systems.

---

**Project Type:** Academic Deep Learning Project  
**Domain:** Deep Learning | Time-Series Forecasting | Flood Monitoring
