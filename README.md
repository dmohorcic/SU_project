# SU project - Time Series Forecasting

This repository contains the work of my Machine Learning course project. I focused on different models for Time Series Forecasting.

## Environment

Environment can be created using:
```
conda create -n suTSF python=3.8
conda activate suTSF
```
Before running next commands install [Pytorch](https://pytorch.org/) with cuda for your system (cuda is required for SCINet model). After installing Pytorch the following packages need to be installed:
```
conda install nb_conda seaborn
conda install numpy pandas
conda install scikit-learn tensorboard -c conda-forge
conda install pytorch-forecasting
conda install statsmodels -c conda-forge
```
If the previous instalation fails, the whole conda environment is located in `environment.yml` file. The environment can be created and run with:
```
conda env create -f environment.yml
conda activate suTSF
```
It is discouraged to create conda environment from file due to some CUDA specific packages.

`start jupyter notebook` must be run from the root of this repository.

## Data

This repository uses five different datasets: electricity, traffic, solar, exchange, and ETTh1.
Electricity dataset can be downloaded [here](https://archive.ics.uci.edu/ml/datasets/ElectricityLoadDiagrams20112014). Traffic, exchange, solar, and ETTh1 datasets can be downloaded [here](https://drive.google.com/drive/folders/1Gv1MXjLo5bLGep4bsqDyaNMI2oQC9GH2?usp=sharing). They must be placed inside `data` folder in the root of this directory.

For SCINet the data from the second link must be placed inside `SCINet/datasets/` using the same folder structure as the one in the link.

## Structure

We have code for four different models. Each model is in its own folder:

1. ARIMA (part of statsmodels package)
2. TRMF ([TRMF on GitHub](https://github.com/SemenovAlex/trmf))
3. DeepAR (part of pytorch-forecasting package)
4. SCINet ([SCINet on GitHub](https://github.com/cure-lab/SCINet))

Inside first three folders is a Jupyter Notebook called `<model>_test.ipynb` which has the code for reproducibility. The SCINet model is run with provided commands in author's README.md file.

`*.xlsx` files contain the results of my tests and experiments.