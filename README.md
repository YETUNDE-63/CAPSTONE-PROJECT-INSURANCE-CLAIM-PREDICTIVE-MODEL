## AINOW_DSML_CAPSTONE_INSURANCECLAIM_PREDICTIVE_MODEL_PROJECT

### Project Title: AINOW_DSML_CAPSTONE_INSURANCECLAIM_PREDICTIVE_MODEL
------------------

[Project Objective](#project-objective)

[Data Overview](#data-overview)

[Tool Used](#tool-used)

[Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Models Development](#models-development)

[Data Analysis](#data-analysis)

[Links](#links)

[Data Visualization](#data-visualization)

[Acknowledgement](#acknowledgement)

### Project Objective
-------------------
The purpose of this analysis is to determine whether a claim is likely to occur during a certain period (Claim Occurrence - Classification), and to predict the likelihood of an insurance claim for buildings (Claim Probability - Predict_proba) based on the building characteristics. 

### Data Overview
-------------------
- Dataset size: 7160 rows × 18 columns
- Features used: YearOfObservation, Insured_Period, Residential, Building_Painted, Building_Fenced, Garden, Settlement, Building Dimension, Building_Type, Date_of_Occupancy, NumberOfWindows, Date_of_Occupancy_missing, Building_Age, Log_Building_Dimension, Geo_Code_te
- Target variable: Claim (1 = claim, 0 = no claim)
- Preprocessing performed:
  - Missing values handled (e.g., NumberOfWindows)
  - Categorical features label-encoded
  - Target encoding applied to Geo_Code
  - Log transformation for building dimension
 
### Tool Used
-------------------
- python [Download Here](http://www.python.com)
  1. Import Libraries and Load Dataset
  2. For Data Cleaning & Preprocessing
  3. For Visualizayion
  4. For Model Development

### Data Cleaning and Preprocessing
-----------------------------------
- In the initial phase of this project, data cleaning and preprocessing were performed, by carrying out the following tasks :
  1. Import libraries and dataset loading
  2. Handling missing variables
  3. Categorical features label-encoded
  4. Target encoding applied to Geo_Code
  5. Log transformation for building dimension

### Exploratory Data Analysis
-----------------------------
- This is to undrestand the patterns and relationships between Features & the Target (Claim) before modelling, such as:
  1. Overall Claim Rate
  2. Claim Rate by key Categorical Features
  3. Distribution of Numeric Features vs Claim
  4. Distribution of Numeric Features (overall)
     - Numeric Features vs Claim
     - Claim Rate by Numeric Bins
     - Categorical Variable Encoding strategy

### Models Development
-----------------------------
1. Model type: Random Forest Classifier
- n_estimators: 300
- Class weighting: Balanced to mitigate class imbalance
- Train-test split: 80/20 stratified
- Threshold tuning: Optimal threshold for class 1 set at 0.25
- Model predicts both claim occurrence and claim likelihood

- Model Performance (Test Set, Threshold=0.25)
Confusion Matrix:
[[787 318]
 [174 153]]

Classification Report:
- Class 0: Precision=0.82, Recall=0.71, F1=0.76
- Class 1: Precision=0.32, Recall=0.47, F1=0.38
- Accuracy: 0.66

Interpretation: Model predicts both claim occurrence and claim likelihood. Predicted probabilities can be used to rank policies by risk.

#### Top Features (Coefficient & Effect)
|Feature|Coefficient|Effect on Risk|
|-------|-----------|--------------|
|Log_Building_Dimension|0.926|Increases Risk|
|Building_Fenced_V|0.583|Increases Risk|
|Insured_Period|0.391|Increases Risk|
|Building_Age|0.359|Increases Risk|
|Geo_Code_6088|0.249|Increases Risk|
|Garden_V|-0.425|Decreases Risk|
|Geo_Code_74010|-0.284|Decreases Risk|
|Geo_Code_19031|-0.268|Decreases Risk|
|Geo_Code_74173|-0.250|Decreases Risk|
|Geo_Code_42187|-0.245|Decreases Risk|

