# crop-yield-prediction
 Project Overview

Accurate crop yield prediction is critical for agricultural planning, food security, and economic decision-making. Traditional statistical and process-based crop models often struggle to capture the complex, nonlinear relationships between environmental conditions and crop yield, particularly at large spatial scales.

This project investigates a deep learning–based approach for predicting crop yield using multimodal environmental data. Crop yield is treated as the sole target variable, without explicitly modelling crop physiological processes. A Multilayer Perceptron (MLP) neural network is trained on publicly available agricultural and environmental datasets from the United States.

Multimodality is achieved through feature-level (early) fusion of heterogeneous data sources, including satellite-derived vegetation indices, meteorological variables, and soil characteristics, rather than through specialised multimodal neural network architectures.

 Objectives

- Integrate heterogeneous environmental data for crop yield prediction  
- Evaluate the effectiveness of a simple deep learning model (MLP)  
- Compare model performance at **county-level** and **state-level** spatial resolutions  
- Assess prediction accuracy using standard regression metrics  

---
 **Datasets**
 The dataset is publicly available at the following link:
 source: https://zenodo.org/records/7751191


The model is trained using publicly available U.S. datasets, including:

- **Satellite Data**
  - Vegetation indices (e.g., NDVI/EVI)
- **Meteorological Data**
  - Temperature, precipitation, and other climate variables
- **Soil Data**
  - Soil texture, composition, and physical properties
- **Agricultural Yield Data**
  - County- and state-level crop yield records

All datasets are preprocessed and aligned spatially and temporally before feature fusion.

---

 Methodology
 Multimodal Fusion Strategy
- Feature-level (early) fusion
- No explicit crop growth or physiological modelling
- No specialised multimodal neural architectures
 Evaluation Metrics

Model performance is evaluated using:

- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**
- **Coefficient of Determination (R²)**

Evaluation is conducted at two spatial scales:
- County level
- State level

** Results**

| Spatial Scale | MAE  | RMSE | R²  |
|--------------|------|------|-----|
| County Level | 14.63 | 18.96 | 0.71 |
| State Level  | 16.83 | 20.65 | 0.42 |

### Key Findings
- Strong predictive performance at the county level
- Reduced accuracy at the state level, likely due to spatial aggregation
- Demonstrates that multimodal environmental data can be effectively leveraged using a relatively simple deep learning framework

