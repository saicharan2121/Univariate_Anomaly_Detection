# Univariate_Anomaly_Detection
Detect anomalies in time series data using One-Class SVM. This project performs univariate anomaly detection, identifying outliers in data like tweet mentions or inventory levels. 


This project focuses on univariate anomaly detection, a task that involves identifying rare events or observations that deviate significantly from the majority of the data within a single stream of values.

It's particularly useful for identifying unusual patterns or spikes/drops in time series data.

Key aspects of this project include:

• Objective: To effectively identify anomalies within a time series. For instance, detecting unusual spikes in the number of Twitter mentions for a company like Apple.
• Data Source: The project utilises real-life data, specifically the number of Twitter mentions for Apple, obtained from Kaggle. The data includes timestamps and the corresponding mention counts.
• Anomaly Detection Algorithm: The core of this project employs the One-Class Support Vector Machine (One-Class SVM) algorithm.
    ◦ How it Works: Unlike traditional SVMs that separate different classes, One-Class SVM is designed to learn a boundary that tightly encloses the majority of "normal" data points when only one class of data is available. Any new data point that falls outside this learned boundary is classified as an anomaly.
    ◦ Parameter Tuning: The nu (or new) parameter is crucial for One-Class SVM. It represents an upper bound on the fraction of training errors and can be conceptualised as the assumed percentage of anomalies within the dataset. In this project, nu was set to 0.2, indicating an expectation of approximately 20% anomalies in the data.
    ◦ Output: The model's predictions classify observations as either 1 for a normal point or -1 for an anomaly.
• Implementation: The algorithm is implemented using the scikit-learn library in Python.
• Demonstration: The entire project, including data loading, preprocessing, model training, prediction, and visualisation, is contained within a Google Colab notebook. This format allows for easy access and reproducibility.
