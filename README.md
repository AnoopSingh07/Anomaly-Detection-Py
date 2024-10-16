
# Anomaly Detection in Data Streams

## Project Title:
Efficient Data Stream Anomaly Detection

## Repository Link:
[https://github.com/AnoopSingh07/Anomaly-Detection-Py.git](https://github.com/AnoopSingh07/Anomaly-Detection-Py.git)

## Project Description:
This project implements an anomaly detection system for continuous data streams using Python. The aim is to identify anomalies such as exceptionally high or low values, or deviations from a normal pattern, in real-time sequences of floating-point numbers. These streams could represent various metrics, such as financial transactions, sensor data, or system performance metrics. The system can be useful in applications like fraud detection, health monitoring, and network security.

## Objectives:
- **Algorithm Selection**: Identify and implement suitable algorithms for anomaly detection in a data stream.
- **Data Stream Simulation**: Design a function to simulate real-time data with seasonal patterns, random noise, and anomalies.
- **Anomaly Detection**: Use Z-score, moving average, and seasonal anomaly detection methods.
- **Optimization**: Ensure the algorithms work efficiently for continuous data streams.
- **Visualization**: Create real-time visualizations to display both the data stream and detected anomalies.

## Algorithms Used:
1. **Z-Score Anomaly Detection**: 
   - This technique identifies anomalies based on how far a data point is from the mean of its preceding values, measured in terms of standard deviations (Z-Score). 
   - An anomaly is detected if the Z-Score exceeds a given threshold, which in our case is set to 2.
   - **Effectiveness**: Suitable for identifying outliers based on statistical properties (mean and std) in the data stream.

2. **Moving Average Anomaly Detection**:
   - A simple technique where the moving average is calculated over a window of recent data points. If the current data point significantly deviates from the moving average, it is flagged as an anomaly.
   - **Effectiveness**: Suitable for detecting shifts in the underlying trend or sudden spikes in the data stream.

3. **Seasonal Anomaly Detection**:
   - This technique detects anomalies based on seasonal patterns in the data. In our case, a sine wave is used to simulate periodic seasonal patterns in the data stream.
   - **Effectiveness**: Useful for detecting anomalies that occur during specific time periods, such as seasonal changes.

## How to Run the Code:
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/AnoopSingh07/Anomaly-Detection-Py.git
   ```
   
2. **Navigate to the Project Folder**:
   ```bash
   cd Anomaly-Detection-Py
   ```

3. **Install Required Libraries**:
   - The code uses external libraries like `numpy`, `matplotlib`. You can install them using `pip`:
     ```bash
     pip install -r requirements.txt
     ```

4. **Run the Code**:
   - If you are using Jupyter Notebook or Google Colab, you can directly run the cells in the notebook.
   - To execute the Python script:
     ```bash
     python anomaly_detection.py
     ```

## Files:
- `anomaly_detection.py`: Main Python script that implements anomaly detection.
- `README.md`: This file, which contains the project description and instructions.
- `requirements.txt`: List of dependencies required to run the project.

## Example Output:
The output will include 3 plots:
1. **Data Stream with Z-Score Anomalies**: Displays the original data stream with anomalies detected using the Z-Score method.
2. **Data Stream with Seasonal and Moving Average Anomalies**: Shows the data stream with anomalies detected using both seasonal and moving average methods.
3. **Data Stream Without Anomalies**: Shows the clean data stream without any anomalies.

