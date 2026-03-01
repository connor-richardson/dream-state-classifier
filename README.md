# Dream Affect Classification from EEG Signals using Machine Learning

Classification of dream-related emotions from EEG signals using the publicly available Dream Emotion Evaluation Dataset (DEED). Two feature extraction methods (PSD and DWT) are compared across two binary classification schemes (Emotional vs. Neutral and Positive vs. Negative) using XGBoost and Random Forest(To be implemented) classifiers, evaluated with Leave-One-Subject-Out (LOSO) cross-validation and 10-Fold CV. 

## Dataset
The DEED dataset consists of 533 6-channel EEG recordings from 38 participants during REM sleep. Files available at http://www.deeddataset.com/#/download 

## Pipelines
1. Load and segment EEG recordings into 20s windows
2. Extract PSD or DWT features
3. Remap labels into binary classification schemes (Emotional vs. Neutral Dream | Positive vs. Negative Dream)
4. Tune hyperparameters with Optuna 
5. Evaluate with LOSO cross-validation and 10-Fold CV

## Requirements
```
numpy
pandas
scipy
xgboost
scikit-learn
optuna
matplotlib
seaborn
pywavelets
```

## Usage
Open `PSD.ipynb` or `DWT.ipynb` and run cells sequentially. The DEED dataset should be placed in a folder named `DEED` in the working directory.


