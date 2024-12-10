# Tool Wear Analysis: Data Preprocessing and Label Augmentation

This document provides an overview of the data preprocessing and label augmentation processes used for exploratory data analysis (EDA) and preparation of the dataset derived from:  
**"The multi sensor-based machining signal fusion to compare the relative efficacy of machine learning-based tool wear models"**  
Authored by **Pramod A., Deepak Lawrence K., and Jose Mathew**. Published in **Harvard Dataverse (2022)**.  
[DOI: 10.7910/DVN/7IAJWU](https://doi.org/10.7910/DVN/7IAJWU)

---

## Data Analysis and Preprocessing

### 1. Exploratory Data Analysis (EDA)
- **Objective**: Gain an understanding of the raw data and sensor-derived variables.
- **Process**:
  - Conducted statistical analysis of the 12 derived variables using **T-tests** to identify significant differences across label ranges.
  - Defined label ranges based on tool wear progression:
    - **Normal**: Initial tool wear phase.
    - **Prognostic**: Intermediate phase indicative of approaching abnormality.
    - **Abnormal**: Tool wear exceeding the threshold of 300, as specified by domain knowledge.
  - Assigned discrete labels (`Normal`, `Prognostic`, `Abnormal`) to corresponding intervals.

### 2. Label Augmentation
- **Purpose**: Enhance discrete tool wear values by transforming them into continuous representations for more detailed modeling.
- **Methodology**:
  - Applied **exponential fitting functions** to interpolate values between discrete points.
  - Generated continuous labels at **0.1-second intervals** to support real-time prediction.
  - Ensured smooth transitions between phases using the fitted exponential curves.

---

## Resulting Dataset
- **Processed Variables**: 12 sensor-derived features augmented with continuous labels.
- **Labels**: 
  - Continuous tool wear values generated through exponential interpolation.
  - Categorical labels (`Normal`, `Prognostic`, `Abnormal`) for classification-based tasks.

---

## Citation
```bibtex
@data{DVN/7IAJWU_2022,
  author = {Pramod A and Deepak Lawrence K and Jose Mathew},
  publisher = {Harvard Dataverse},
  title = {{The multi sensor-based machining signal fusion to compare the relative efficacy of machine learning based tool wear models}},
  UNF = {UNF:6:dXrPQBleR2MIYhnAnGNFJQ==},
  year = {2022},
  version = {V1},
  doi = {10.7910/DVN/7IAJWU},
  url = {https://doi.org/10.7910/DVN/7IAJWU}
}
