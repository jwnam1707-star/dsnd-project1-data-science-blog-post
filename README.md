# dsnd-project1-data-science-blog-post (Medicare-Serving Hospital Analysis)
This repository contains the first project for the Udacity Data Scientist Nanodegree program, which focuses on writing and publishing a data science blog post.

## Libraries Used
This project was completed in Python using the following libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

These libraries were used for data loading, cleaning, exploratory data analysis, visualization, and a simple logistic regression model.

## Project Motivation
This project analyzes CMS hospital datasets to understand structural differences across Medicare-serving hospitals, patient experience patterns, and the relationship between hospital characteristics and readmission risk. The analysis follows the CRISP-DM framework and is organized around the following business questions:

1. Where do Medicare-serving hospitals appear to have structural or service-access gaps?
2. How do patient experience measures vary across hospitals, and what do they tell us about hospital quality?
3. Can hospital characteristics and patient experience indicators help identify hospitals at risk of above-expected heart failure readmissions?

## Files in the Repository
- `README.md`: project overview and summary
- `main_notebook.ipynb`: main notebook version of the project
- `data/`: local folder expected by the notebook for raw CSV files (not included in this repository)

## Data
The raw CSV files are not included in this repository because of file size limitations.

To run the notebook, create a folder named `data` in the repository root and place the following files inside it:
- `Hospital_General_Information.csv`
- `HCAHPS-Hospital.csv`
- `FY_2025_Hospital_Readmissions_Reduction_Program_Hospital.csv`

These datasets can be downloaded from the CMS Provider Data Catalog:
https://data.cms.gov/provider-data/datasets

## Summary of Results
- The number of Medicare-serving hospitals varies across states, and some areas such as AS, GU, MP, RI, and VI have relatively few hospitals in the dataset.
- Veterans Administration owned or operated hospitals show higher mean overall ratings than other ownership groups in this analysis, and hospital rating also differs by hospital type and emergency-service status.
- HCAHPS star ratings are concentrated around 3 to 4 stars, while HCAHPS linear mean values are mostly distributed between about 80 and 95.
- Higher HCAHPS linear mean values are generally associated with higher overall hospital ratings, suggesting that patient experience is aligned with broader hospital quality signals.
- Readmission ratios across HRRP conditions are on average close to the CMS benchmark of 1.0, with modest variation across states, hospital types, and ownership groups.
- A simple logistic regression model was trained to predict whether a hospital has an above-expected heart failure readmission ratio (`Excess Readmission Ratio > 1`) using hospital characteristics and HCAHPS linear mean value.
- In the example prediction scenario, the model predicted class `1` with probability `0.644`, meaning the hypothetical hospital was classified as more likely to have above-expected heart failure readmissions.

For a concise and non-technical overview of the project, you can also read the accompanying Medium blog post here: [https://medium.com/@jwnam1707/what-medicare-hospital-data-revealed-about-care-gaps-patient-experience-and-readmission-risk-3b56b6d1e3b8].

## Acknowledgement
This project uses publicly available hospital data from the Centers for Medicare & Medicaid Services (CMS), including Hospital General Information, HCAHPS, and Hospital Readmissions Reduction Program datasets.
