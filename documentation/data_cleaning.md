# Data Cleaning

## Overview
Data cleaning involves preparing the dataset for analysis by addressing inconsistencies, handling missing values, and transforming data into a suitable format. 

## Steps Taken

### 1. **Handling Missing Values**
- **Genres and Themes:** Split these columns if they contain multiple values separated by commas. Entries with missing genre or theme information were either filled based on similar entries or marked as "Unknown."
- **Scores:** Ensured that all score entries were valid floating-point numbers. Missing or erroneous scores were handled by imputing average scores or removing entries if data was critically missing.

### 2. **Data Transformation**
- **Genres Column:** Converted the `Genres` column from a comma-separated list to a multi-value format to facilitate analysis. Created a new table for genres with a many-to-many relationship with the main anime table.
- **Themes Column:** Similar transformation as genres.
- **Aired and Premiered Columns:** Split these columns into separate `Start Date` and `End Date` for better date-based analysis.

### 3. **Standardization**
- **Rating Column:** Standardized all rating values to a consistent format. Converted ratings to a uniform scale where necessary.
- **Duration Column:** Converted duration values to a consistent time format (e.g., minutes).

### 4. **Data Verification**
- **Consistency Check:** Verified that all numeric columns (e.g., `Episodes`, `Popularity`, `Score`) contained valid data types and ranges.
- **Duplicates:** Removed duplicate entries based on the `Name` and `Japanese` title columns to ensure unique records.

## Summary
The data was cleaned to ensure accuracy and consistency, making it ready for effective analysis and visualization in Power BI.
