# MSc Dissertation Prototype: AI for Stormwater Harvesting in Agriculture

Code for my MSc Data Analytics dissertation at the National College of Ireland (2025): *Stormwater Harvesting in Agriculture for Sustainable Growth: Integrating Generative AI and Machine Learning Models.*

> **Looking for the latest version?** This prototype was the starting point for a more rigorous follow-up study using real Copernicus climate data, chronological validation and uncertainty analysis: **[stormwater-ml-decision-system](https://github.com/srushti28003/stormwater-ml-decision-system)**.

## What it does

An exploratory, multi-model prototype that brings several agricultural water-management tasks into one Python class:

| Component | Approach |
|---|---|
| Weather sequence model | LSTM (TensorFlow/Keras) |
| Agricultural-condition classifier | Random Forest |
| Storm-risk predictor | Regularised logistic regression / decision tree |
| Irrigation-need estimator | Regression on weather and soil nutrients |
| Crop-type classifier | Supervised classifier across 22 crops |
| Recommendations | Rule-based advice combining the model outputs |

## Data

`Crop_recommendationV2.csv`: an extended version of the public Crop Recommendation dataset, with 2,200 rows and 23 agronomic and weather features (N, P, K, temperature, humidity, pH, rainfall, soil moisture and others).

## What I learned

Building this prototype showed me how easily models can look accurate when targets are derived from the same features used as inputs, and why random train/test splits can overstate performance on time-dependent data. Those lessons shaped the follow-up study, which uses real reanalysis data, chronological splits, time-series cross-validation, a persistence baseline and bootstrap confidence intervals.

## Files

| File | Description |
|---|---|
| `msc_dissertation_prototype.ipynb` | Full prototype notebook (developed in Google Colab) |
| `Crop_recommendationV2.csv` | Input dataset |

## Running it

Open the notebook in Google Colab, upload `Crop_recommendationV2.csv` to `/content/`, and run the cells in order. Requires numpy, pandas, scikit-learn, tensorflow, matplotlib and seaborn.

## Author

**Srushti Jadhav** · [LinkedIn](https://www.linkedin.com/in/srushti-jadhav60/)
