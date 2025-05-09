# TM-Ti3C2T2-for-ORR-OER

## Folder: **Descriptor&DFT-calculate**
This folder contains the following key files:

### Descriptors.csv
This file includes the descriptor values for all systems. The data sources are:

The PubChem 2025 database:
Kim, S., Chen, J., Cheng, T., et al. (2025). PubChem 2025 update. Nucleic Acids Res., 53(D1), D1516–D1525.

Our own DFT (Density Functional Theory) calculations.

### SeparateByGroup.ipynb
A Python notebook that randomly splits the dataset into training and prediction sets.
Dependencies: Requires the pandas library.

### DFT_Data.csv
This repository contains DFT-calculated properties of various single-atom catalysts (SACs) supported on Ti₃C₂T₂ substrates. The dataset includes the following key properties for each structure:

CBM: Conduction Band Minimum (in eV)

VBM: Valence Band Maximum (in eV)

WF: Work function (in eV)

E<sub>c</sub>: Cohesive energy of the single atom in SAC (in eV)
E_c = – (E_M-bulk / N – E_M-single)

E<sub>b</sub>: Binding energy of the single atom on the substrate (in eV)
E_b = – (E_MTi3C2T2 – E_M-single – E_Ti3C2T2)

E<sub>form</sub>: Formation energy of the SAC (in eV)
E_form = E_MTi3C2T2 – E_Ti3C2T2 – E_M-bulk / N

## Folder: **CNN**
This folder contains the model of CNN.

### Eb.ipynb, Ec.ipynb, and Ef.ipynb
Three Jupyter notebooks—Eb.ipynb, Ec.ipynb, and Ef.ipynb—which correspond to the training of CNN models for predicting binding energy, cohesive energy, and formation energy, respectively. Each notebook includes:

Model training parameters

Evaluation metrics such as MRSE, MEA, and R²

Performance comparison between CNN predictions and DFT results on both training and test datasets

SHAP analysis for interpreting model predictions

### Eb.h5, Ec.h5

The files Eb.h5, Ec.h5, and Ef.h5 are the trained CNN models corresponding to the three energy types above.

## Folder: **ML**
This folder shows various methods for predicting Binding Energy (Eb), Cohesive Energy (Ec), and Formation Energy (Eform).

Linear Regression (LR), Decision Trees (DT), Random Forests (RF), Gradient Boosting Regression (GBR), AdaBoost, XGBoost, LightGBM, Extremely Randomized Trees (ExtraTrees), K-Nearest Neighbors (KNN), Support Vector Regression (SVR), Multi-layer Perceptrons (MLP)
