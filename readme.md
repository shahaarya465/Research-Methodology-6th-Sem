# Flood Detection Using Rainfall-Based Machine Learning

This repository contains a rainfall-driven flood risk modeling workflow used for two related research studies. The core machine learning pipeline is shared across both studies, while interpretation and conclusions are study-specific.

## Research Studies

1. Machine Learning-Based Urban Flood Risk Assessment with Cross-City Validation: Chennai and Bengaluru
   - Training city: Chennai
   - Validation city: Bengaluru
   - Domain focus: urban flood behavior
   - Lead: Aditya Patel (23AIML046)

2. Machine Learning-Based Flood Risk Assessment in Contrasting Terrains: Chennai and Uttarkashi
   - Training city: Chennai
   - Validation city: Uttarkashi
   - Domain focus: coastal vs mountainous flood behavior
   - Lead: Aarya Shah (23AIML064)

## Repository Structure

- [datasets/chennai.csv](datasets/chennai.csv)
- [datasets/bangalore.csv](datasets/bangalore.csv)
- [datasets/uttarkashi.csv](datasets/uttarkashi.csv)
- [chennai_bangalore.ipynb](chennai_bangalore.ipynb)
- [chennai_uttarkashi.ipynb](chennai_uttarkashi.ipynb)
- [geojson/Chennai.geojson](geojson/Chennai.geojson)
- [geojson/Bangalore.geojson](geojson/Bangalore.geojson)
- [geojson/Uttarakhand.geojson](geojson/Uttarakhand.geojson)

## Common ML Pipeline

The following pipeline is kept consistent across both studies:

1. Data loading and cleaning
   - Standardize columns for date and rainfall
   - Parse date and extract year and month
   - Handle missing or invalid values

2. Feature engineering
   - Annual total rainfall
   - Monsoon rainfall (June to September)
   - Extreme rainfall event count (threshold-based)
   - Optional temporal features such as rolling statistics

3. Target label creation
   - Binary flood label at year level
   - Flood years are assigned from documented historical events

4. Model training and evaluation
   - Train on Chennai data only
   - Baseline: Logistic Regression
   - Main model: Random Forest
   - Metrics: Accuracy, Precision, Recall, F1-score

5. Cross-dataset validation
   - Case A: Chennai to Bengaluru
   - Case B: Chennai to Uttarkashi

6. Explainability
   - Random Forest feature importance
   - Relative influence of monsoon, total, and extreme rainfall factors

## Dataset Labeling Reference

- Chennai flood years: 2015, 2023
- Bengaluru flood years: 2022
- Uttarkashi flood years: 2013, 2021

## Notebook Guide

- [chennai_bangalore.ipynb](chennai_bangalore.ipynb): End-to-end workflow for the Chennai to Bengaluru study.
- [chennai_uttarkashi.ipynb](chennai_uttarkashi.ipynb): End-to-end workflow for the Chennai to Uttarkashi study.

## Expected Outputs

- Clean model-ready annual dataset with columns:
  - Year
  - Monsoon_Rainfall
  - Total_Rainfall
  - Extreme_Rain_Count
  - Flood_Label
- Classification reports for both models and both validation settings
- Visualizations:
  - Rainfall trends
  - Model performance comparison
  - Feature importance

## Scope and Constraints

- Tabular machine learning only
- No heavy GIS or satellite processing
- Beginner-friendly implementation
- Designed to run on a standard laptop

## Suggested Environment

- Python 3.10+
- Jupyter Notebook
- Recommended libraries:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - seaborn

## Citation and Academic Use

This repository is intended for academic research and coursework on rainfall-based flood risk modeling. If reused, please cite the corresponding study context and preserve authorship details.
