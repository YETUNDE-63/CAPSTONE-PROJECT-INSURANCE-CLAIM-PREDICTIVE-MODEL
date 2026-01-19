## AINOW_DSML_CAPSTONE_INSURANCECLAIM_PREDICTIVE_MODEL_PROJECT

### Project Title: AINOW_DSML_CAPSTONE_INSURANCECLAIM_PREDICTIVE_MODEL
------------------

[Project Objective](#project-objective)

[Data Overview](#data-overview)

[Tools Used](#tools-used)

[Data Cleaning and Preparations](#data-cleaning-and-preparations)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Key Insights](#key-insights)

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

