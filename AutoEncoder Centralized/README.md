# README: Autoencoder for Anomaly Detection on IIoT

## Overview
This folder contains a Jupyter Notebook that implements an autoencoder for centralized anomaly detection. 

## Requirements
Ensure you have Python installed along with the following libraries:
```bash
pip install notebook numpy pandas scikit-learn tensorflow
```

## Running the Notebook
1. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Open the provided notebook.
3. Run all cells to train the autoencoder and detect anomalies.

## Datasets

- ../Data Sample/Train.csv
- ../Data Sample/Validation.csv
- ../Data Sample/Test.csv


## How It Works
- The autoencoder is trained using Train.csv data.
- After training, it reconstructs inputs and calculates the reconstruction error.
- Optimized thresholds are calculated using Validation.csv 
- Anomalies are detected based on a threshold applied to the reconstruction error.

## Results
The model outputs metrics are calculated over Test.csv. The metrics are accuracy, precision, recall, F1-score, TNR, TPR and a confusion matrix to evaluate anomaly detection performance, saved on results.csv.


## License
This project is open-source and free to use.

