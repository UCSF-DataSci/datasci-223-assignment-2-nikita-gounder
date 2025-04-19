## Analysis Description

# Analysis Approach
- Cleaned patient data using VScode debugger 
- Converted small inputted CSV to large CSV dataset
- Calculated med dosages for patients 
- In cohort analysis section converted this dataset into parquet format for effecient processing

# Patterns / Insights
- Higher BMI correlated with higher average glucose levels and were usually older patients
- 
- 

# Polars' Features for Efficiency
- Polars library allows for speed and efficiency through lazy evaluation to optimize query plans and faster backend processing 
- Copare to pandas it is 10-20x faster, uses 50-80% less memory, and scales to datasets 100x larger than pandas can handle
- that last part is especially useful for this assignment where the dataset is especially large and pandas probably could not have handled it