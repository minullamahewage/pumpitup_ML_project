# Pump It Up - ML Project
 
 Github Repo Link: https://github.com/minullamahewage/pumpitup_ML_project
 
- Driven Data Username: **moracse_170342n**
- Name: **M.H. Lamahewage**
- Index No.: **170342N**

## EDA

- Went through the train dataset and observed the features using various tools. 
- The dataset was found to be imbalanced. Weighted F1-score was used for evaluation.


| functional | non-functional | functional needs repair |
| :------: | :----------: | :------------------: |
| 32259 | 22824 | 4317 |

- Features with missing values, null values, zeros and other inconsistencies were identified.
- Features with high cardinality were identified.
- Features with high correlation/similar features were identified. 

## Preprocessing
### Handling Missing Values
- Replaced null values with the mode for categorical features.
- Replace other missing values such as unknown, None and 0 with mean for numerical features and mode for categorical features. 

### Features with high correlation
These features were found to have high correlation or were similar upon manual inspection.
- extraction_type, extraction_type_group, extraction_type_class
- payment, payment_type
- water_quality, quality_group
- quantity, quantity_group
- source, source_type, source_class
- region, region_code
- waterpoint_type, waterpoint_type_group
One of each were chosen based on several factors and the remaining features were dropped.


### Ordinal Encoding
- Categorical features which are ordered or had too many categories were encoded using the OrdinalEncoder.
- Features: "funder","installer", "subvillage", "lga", "ward", "public_meeting", "permit", "management", "payment_type", "water_quality", "date_recorded".

### OneHot Encoding
- Categorical features which aren't ordered and had a smaller number of categories were encoded using the OneHotEncoder
- Features:  "basin", "scheme_management", "extraction_type_class", "management_group", "quantity", "source_type", "waterpoint_type".

### Label Encoding
- The labels were encoded using the LabelEncoder

## Feature Selection
- Corelation of different features were inspected and leaving only one each of similar features, the rest were dropped.
- Two features were removed as all the values were the same in every row. 
- Features with too many missing values were also dropped. 

## Feature Engineering
- Added new feature "active_time" which represents the total time the pump has been active by the recorded date.

## Model Selection
- **RandomForestClassifier**
- XGBoost and RandomForest were considered and RandomForest was used due to better results.
- parameters: n_estimators=600, max_depth=40, min_samples_split=10


## Submissions

| Score  | Current Rank | # competitiors | Submission Date |
| :---: | :---: | :----: | :-----: |
| **0.8170** | 1624 | 12453 | Sept. 16, 2021 |

![alt text](https://github.com/minullamahewage/pumpitup_ML_project/blob/main/submission.png "Submission Proof")
