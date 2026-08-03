# Flood Susceptibility Mapping: A Hybrid AHP and Ensemble Machine Learning Approach

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Tapanuli Tengah Regency, Indonesia

### Code Availability
This repository contains the analysis code for the paper "A Hybrid AHP and Ensemble Machine Learning Approach for Flood Susceptibility Assessment in Tapanuli Tengah Regency, Indonesia" by Sandri Erfani and Razki Alfatah Khairu Mahli.

```
tapteng-flood-susceptibility/
├── README.md                         
├── requirements.txt
├── LICENSE                            
├── CITATION.cff                       
├── .gitignore
├── data/
│   ├── README.md
│   └── samples/
│       └── dataset_training.csv       
├── model_export/
│   ├── rf_model.joblib               
│   └── model_metadata.json           
├── notebooks/
│   ├── 1_Generate-Sampling.ipynb
│   ├── 2_Extract-Dataset.ipynb
│   ├── 3_Multicollinearity-Analysis.ipynb
│   ├── 4_AHP-Calculation.ipynb
│   ├── 4b_AHP-Susceptibility-Raster.ipynb
│   ├── 5_ML-Models.ipynb
│   ├── 6_SHAP-Analysis.ipynb
│   ├── 7_Spatial-Agreement.ipynb
│   └── 8_QGIS-to-Python-Utils.ipynb
└── outputs/
    ├── ahp_pairwise_matrix.csv       
    ├── ahp_weights.csv               
    ├── feature_importance.csv        
    ├── model_metrics.csv             
    └── spatial_agreement.csv
```

### Requirements
- Python >= 3.9
- See requirements.txt for dependencies

### Notebooks
1. `1_Generate-Sampling.ipynb` - Generate flood/non-flood sample points
2. `2_Extract-Dataset.ipynb` - Extract conditioning factor values at sample locations
3. `3_Multicollinearity-Analysis.ipynb` - VIF, Pearson, and Spearman correlation analysis
4. `4_AHP-Calculation.ipynb` - Analytical Hierarchy Process weight calculation
5. `4b_AHP-Susceptibility-Raster.ipynb` - AHP weighted overlay to produce susceptibility map (raster)
6. `5_ML-Models.ipynb` - Random Forest, XGBoost, SVM training and evaluation
7. `6_SHAP-Analysis.ipynb` - SHAP interpretability analysis
8. `7_Spatial-Agreement.ipynb` - Cross-tabulation between AHP and RF maps
9. `8_QGIS-to-Python-Utils.ipynb` - Pure-Python replacements for QGIS operations

### Data
The `data/samples/dataset_training.csv` file should contain the training dataset with columns: [label, elevation, slope, distance_to_river, distance_to_coast, land_cover, soil_type, ndvi, rainfall].

Raw geospatial data (rasters, shapefiles) are publicly available from:
- DEMNAS: Badan Informasi Geospasial (BIG)
- Sentinel-2 L2A: ESA/Copernicus
- CHIRPS: UCSB Climate Hazards Group
- Soil type: FAO/IIASA Harmonized World Soil Database
- Land cover: Badan Informasi Geospasial (BIG)

### Citation
If you use this code, please cite:

```
Erfani, S., & Mahli, R. A. K. (2026). A Hybrid AHP and Ensemble Machine Learning Approach for Flood Susceptibility Assessment in Tapanuli Tengah Regency, Indonesia. [Journal Name].
```

### License
MIT License
