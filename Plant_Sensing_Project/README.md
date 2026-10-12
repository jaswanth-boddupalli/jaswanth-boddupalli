# Plant Sensing Proof-of-Concept Pipeline

This project provides a computational proof-of-concept for non-destructive plant trait retrieval from spectral reflectance. The pipeline is designed for applications in autonomous controlled-environment agriculture and precision phenotyping.

## Pipeline Overview

1. **Simulated Reflectance Generation:** Uses the PROSAIL radiative transfer model to simulate canopy/leaf reflectance. Latin Hypercube Sampling (LHS) is employed to generate a robust training dataset that evenly spans the parameter space.
2. **Data Preprocessing:** Adds synthetic noise to the simulated reflectance data to mimic real-world sensor inaccuracies and environmental variability.
3. **Machine Learning Inversion:** Trains machine learning models (such as Random Forest and XGBoost) to invert spectral reflectance back into physiological traits, including:
   - Chlorophyll concentration
   - Equivalent water thickness
   - Canopy structure / Leaf Area Index (LAI)
4. **Validation and Evaluation:** Computes evaluation metrics (R-squared, RMSE) and generates visualization plots comparing predicted vs. actual traits.

## Usage

This project contains a comprehensive Jupyter Notebook that outlines the entire pipeline, from data generation to model training and evaluation. Simply open the notebook and follow the sequentially executed code cells.

## Dependencies
* `numpy`, `pandas` - Data manipulation
* `scikit-learn`, `xgboost` - Machine Learning algorithms
* `prosail` - Radiative transfer modeling
* `matplotlib` - Data visualization
