# README: OneClass SVM for Anomaly Detection on IIoT

## Overview
This folder contains a Jupyter Notebook that implements One-Class SVM for centralized anomaly detection.

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

-The One-Class SVM model is trained using Train.csv data.
-The model learns a decision function for novelty detection.
-Anomalies are detected by classifying instances that fall outside the learned decision boundary.

## Results
The model outputs metrics are calculated over Test.csv. The metrics are accuracy, precision, recall, F1-score, TNR, TPR and a confusion matrix to evaluate anomaly detection performance, saved on results.csv.

## License
This project is open-source and free to use.

