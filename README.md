# README: Autoencoder for Anomaly Detection on IIoT

## Overview
This repository contains a Jupyter Notebook that implements an autoencoder for anomaly detection.   Base repository of the work “Federated Learning framework for LoRaWAN-enabled IIoT communication: A case study”

## Requirements
Ensure you have Python installed along with the following libraries:
```bash
pip install notebook numpy pandas scikit-learn tensorflow
```

## Codes

The repository has the main codes for validating data and anomaly detection models. There are three centralized model codes:
- AutoencoderCentralized
- IsolationForest
- OneClassSVM

and one decentralized model federated learning

-AutoencoderFedLearning

## Datasets
Within the folder "/Data Sample" there are 4 datasets: 

- Complete.csv
- Train.csv
- Validation.csv
- Test.csv


## How It Works
- The autoencoder is trained using Train.csv data.
- After training, it reconstructs inputs and calculates the reconstruction error.
- If you are using autoencoder a optimized thresholds are calculated using Validation.csv 
- Anomalies are detected in each type of anomaly detection model.

## Results
The model outputs metrics are calculated over Test.csv. The metrics are accuracy, precision, recall, F1-score, TNR, TPR and a confusion matrix to evaluate anomaly detection performance, saved on results.csv.

## License
This project is open-source and free to use.

