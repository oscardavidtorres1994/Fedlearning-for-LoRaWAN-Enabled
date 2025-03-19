# README: Autoencoder for Anomaly Detection on IIoT

## Overview
This repository contains a Jupyter Notebook implementing an autoencoder for anomaly detection. The autoencoder is a type of neural network used to learn a compressed representation of data, which helps identify unusual patterns or anomalies.

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

- Train.csv
- Validation.csv
- Test.csv


## How It Works
- The autoencoder is trained using Train.csv data.
- After training, it reconstructs inputs and calculates the reconstruction error.
- Optimized thresholds are calculated using Validation.csv 
- Anomalies are detected based on a threshold applied to the reconstruction error.

## Results
The model outputs metrics are calculated over Test.csv. The metrics are accuracy, precision, recall, F1-score, TNR, TPR and a confusion matrix to evaluate anomaly detection performance, saved on results.csv.

## License
This project is open-source and free to use.

