# README: Isolation Forest for Anomaly Detection on IIoT

## Overview
This folder contains a Jupyter Notebook that implements an  anomaly detection using Isolation Forest. 

## Requirements
Ensure you have Python installed along with the following libraries:
```bash
pip install notebook numpy pandas scikit-learn
```


## Datasets
Within the folder "/Data Sample" there are 4 datasets: 

- ../Data Sample/Train.csv
- ../Data Sample/Validation.csv
- ../Data Sample/Test.csv


## How It Works

-he Isolation Forest model is trained using Train.csv data.
-The model assigns anomaly scores to each instance.
-Anomalies are detected by selecting instances with the highest anomaly scores, based on an automatically determined threshold.

## Results
The model outputs metrics are calculated over Test.csv. The metrics are accuracy, precision, recall, F1-score, TNR, TPR and a confusion matrix to evaluate anomaly detection performance, saved on results.csv.

## License
This project is open-source and free to use.

