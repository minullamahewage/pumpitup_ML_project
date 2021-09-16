# Pump It Up - ML Project
- Name: M.H. Lamahewage
- Index No.: 170342N

## Preprocessing
### Handling Missing Values
- Replaced null values with mode
- Replace other missing values such as unknown, None and 0 with mean and mode

### Ordinal Encoding
- Categorical features which are ordered or had too many categories were encoded using the OrdinalEncoder

### OneHot Encoding
- Categorical features which aren't ordered and had a smaller number of categories were encoded using the OneHotEncoder

### Label Encoding
- The labels were encoded using the LabelEncoder

## Feature Selection
- Corelation of different features were inspected and leaving only one each of similar features, the rest were dropped.
- Two features were removed as all the values were the same in every row. 
- Features with too many missing values were also dropped. 

