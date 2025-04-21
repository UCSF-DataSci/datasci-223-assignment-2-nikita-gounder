## Analysis Description

# Analysis Approach
- Cleaned patient data using VScode debugger 
- Converted small inputted CSV to large CSV dataset
- Calculated med dosages for patients 
- In cohort analysis section converted this dataset into parquet format for effecient processing

# Patterns / Insights
- Higher BMI correlated with higher average glucose levels and were usually older patients
- There were also the most obese patient with an average age of 33.8 and avg_glucose of 126.03
- Age, average glucose, and count increase with BMI increase

Cohort Analysis Summary:
┌─────────────┬─────────────┬───────────────┬───────────┐
│ bmi_range   ┆ avg_glucose ┆ patient_count ┆ avg_age   │
│ ---         ┆ ---         ┆ ---           ┆ ---       │
│ cat         ┆ f64         ┆ u32           ┆ f64       │
╞═════════════╪═════════════╪═══════════════╪═══════════╡
│ Underweight ┆ 95.195115   ┆ 26041         ┆ 23.980646 │
│ Obese       ┆ 126.032016  ┆ 3066409       ┆ 33.82713  │
│ Normal      ┆ 108.004737  ┆ 664064        ┆ 31.888848 │
│ Overweight  ┆ 116.373363  ┆ 1165360       ┆ 32.880893 │

# Polars' Features for Efficiency
- Polars library allows for speed and efficiency through lazy evaluation to optimize query plans and faster backend processing 
- Copare to pandas it is 10-20x faster, uses 50-80% less memory, and scales to datasets 100x larger than pandas can handle
- that last part is especially useful for this assignment where the dataset is especially large and pandas probably could not have handled it
