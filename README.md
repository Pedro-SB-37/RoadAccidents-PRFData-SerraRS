# Road-accidents-and-weather-conditions-in-the-Serra-Ga-ucha-an-exploratory-analysis-using-PRF-data

## Overview
This repository contains the Colab Notebook and datasets used in the paper "Road accidents and weather conditions in the Serra Ga ´ucha: an exploratory analysis using PRF data"

## Pipeline Summary
1. **Exploratory Analysis** Initial observation of dataset characteristics
1. **Data Cleaning & Geocoding:** Coordinate extraction, boundary filtering via GeoJSON, and removal of administrative metadata.
2. **Feature Engineering:** Binary grouping of meteorological conditions (`clima_binario`), temporal feature extraction (`mes`, `hora_int`, `dia_da_semana`), and strict removal of post-incident leakage variables.
3. **Machine Learning:** Spot-checking of algorithms (Random Forest, XGBoost, LightGBM) using `StratifiedKFold` cross-validation.
4. **Explainability:** Feature importance and SHAP value analysis for model interpretation.

## Repository Structure
├── exploratory_analysis_and_machine_learning_prf.ipynb         # Full Google Colab experimental pipeline
├── serra_gaucha.geojson                                        # Spatial boundary polygon of the region
├── requirements.txt                                            # Python dependencies
├── Dados_Rodovia.csv                                           # The file used for upload in the Collab (Already had the Excel changings descripts in the Colab)
├── CSVs.zip                                                    # Other 3 CSVs are compressed in this folder
    ├── Dados_Rodovia_Bruto.csv                                 # Raw Data
    ├── Dados_Rodovia_Limpo.csv                                 # Data after data cleaning
    ├── Dados_Rodovia_Feature_Engineering.csv                   # Data after feature engineering
└── README.md                                                   # Project documentation

## Reproducibility
To reproduce the experiments, install the dependencies and execute `exploratory_analysis_and_machine_learning_prf.ipynb` sequentially.
