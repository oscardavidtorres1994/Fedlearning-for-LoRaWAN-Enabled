# Federated learning hands-on activity from ISABELA

This file describes the Federated Learning hands-on activity using data from ISABELA platform. It executes the codes using the tensorflow federated library, Python and Jupyter Notebook.


## Requirements

Windows, Linux or macOS with Conda, pip and Python 3.9+ support. 

GPU support is not required.

## Datasets

- ../Data Sample/Train.csv
- ../Data Sample/Validation.csv
- ../Data Sample/Test.csv

<!-- ## Folder description

The root of the project is composed with two folders: 
- Dataset_ECUADOR_2019: Folder that contains the raw data from ISABELA.
- scripts: Folder data contains all the scripts to pre-processing and to run the federated learning codes.


The scripts folder is divided in three folders:
- [00_data_preprocessing](./scripts/00_data_preprocessing): it has the scripts to process the raw data. We do not need it for the current activity.
- [01_model_processing](./scripts/01_model_processing): it has the scripts to execute the machine learning process. *We wil work here :-)*
- [02_data_analysis](./scripts/02_data_analysis): it has some scripts to data analysis and graphs. Such codes can be used only for didactic reasons.
- [data_2019_processed](./scripts/data_2019_processed): it has the data that we will use in the activity. It is already ready. -->

## Tools installation

First, it is recommended to have conda installed in you system. If you do not want, you need to have python 3.9+ installed.

### (Optional) Miniconda installation and usage

Instructions:
- Native Windows: https://docs.conda.io/projects/conda/en/latest/user-guide/install/download.html
- MacOS: https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html
- Linux or Windows with WSL 2.0: https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html

In linux you can download and install by the follow commands:
- `curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -o Miniconda3-latest-Linux-x86_64.sh`
- `bash Miniconda3-latest-Linux-x86_64.sh`

Useful commands:
- Create a conda environment: `conda create --name trctf python=3.9`
- If you need to remove the environment: `conda remove --name trctf --all`
- Access the environment: `conda activate trctf`
- Exit the environment: `conda deactivate`

### TensorFlow Federated libraries

The basic commands are:
- `pip install --upgrade pip`
- `pip install tensorflow tensorflow-federated`

The last versions not always are compatible with all Operational Systems Environments. 
Thus, if you have some installations errors you can install previous version:

Previous versions to Linux and Windows:
- `pip install --upgrade tensorflow==2.10`
- `pip install --upgrade tensorflow-federated==0.40`

MacOS does not have access to some compression libraries used in recent machine learning libraries from tensorflow-federated. Thus, we use a previous version:
- `pip install --upgrade tensorflow-macos==2.9.2 --no-cache-dir`
- `pip install attrs==21.4.0 dp-accounting==0.4.0 matplotlib==3.6.2 pandas==1.5.1 scikit-learn==1.1.3 tensorflow-datasets==4.5.2 tensorflow-probability==0.15 --no-cache-dir`
- `pip install tensorflow-metadata==1.12`
- `pip install jax==0.3.13 jaxlib==0.3.10 tensorflow-metal==0.5.1 numpy==1.23.4 --no-cache-dir`
- `pip install farmhashpy==0.4.0 portpicker==1.5 semantic-version==2.6 tensorflow-model-optimization==0.7.3 tensorflow-privacy==0.8.4 --no-dependencies --no-cache-dir`
- `pip install tensorflow-federated==0.34  --no-deps --no-cache-dir`

If you have on macOS the error with hdf5 library you must install homebrew to install it. Instructions:
- Install HomeBrew: https://brew.sh
- Export homebrew: `echo "export PATH=/opt/homebrew/bin:$PATH" >> ~/.bash_profile && source ~/.bash_profile`
- Install hdf5: https://stackoverflow.com/questions/70587971/errorfailed-building-wheel-for-h5pyfailed-to-build-h5pyerrorcould-not-build-wh

### Install support libraries to Jupyter Notebook

Execute the follow command line: `pip install jupyter pandas scikit-learn matplotlib seaborn nltk beautifulsoup4 nest_asyncio imblearn`

<!-- ### Execute jupyter notebook

`jupyter notebook`


(Optional) You can specify the home jupyter folder --notebook-dir. Example: 

`jupyter notebook --notebook-dir=/mnt/d/Projetos/Federated-learning-hands-on-activity-from-ISABELA`

### Are you finished?

If you arrived here, you can enter the [01_model_processing](./scripts/01_model_processing) folder to read the instructions and execute the codes. -->

## Running the Notebook
1. Start Jupyter Notebook:
   ```bash
   cd "/mnt/c/Users/.../Fedlearning-for-LoRaWAN-Enabled/Autoencoder Federated Learning"
   jupyter notebook --no-browser
   ```
2. Open the provided notebook or copy link
3. Run all cells to train the autoencoder and detect anomalies.


## How It Works
-
- The autoencoder is trained in emulating each device using Train.csv data.
- After training, the devices send the data to the simulated server
- The server uses FedAvg aggregation process and sends the data to each device. 
- The global model is used to reconstructs inputs and calculates the reconstruction error.
- Optimized thresholds are calculated using Validation.csv locally. 
- Anomalies are detected based on a threshold applied to the reconstruction error.

## Results

The program will create a folder based on the number of execution, number of rounds, and number of iterations. The metrics are accuracy, precision, recall, F1-score and a confusion matrix to evaluate anomaly detection performance, saved on global_model_metrics.csv inside the folder. 
