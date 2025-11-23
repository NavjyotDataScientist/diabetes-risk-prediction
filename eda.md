leaning missing and invalid values

Visualizing distributions

Understanding relationships

Preparing the cleaned dataset for feature engineering

📂 1. Load Dependencies & Dataset
Goals:

Import required Python libraries

Load the raw dataset from data/raw/

Create an initial copy for safe processing

🔍 2. Initial Data Inspection
Checklist:

.head() to preview first rows

.shape to confirm rows & columns

.info() for datatypes & missing value summary

.describe() for statistical summary

Check for:

wrong datatypes

inconsistent values

impossible values

unusual patterns

🪪 3. Column Name Validation
Goals:

Ensure column names are clean & standardized

Fix spacing, casing, special characters

Convert to snake_case (industry standard)

⚠️ 4. Missing Value Analysis
Goals:

Identify missing values

Visualize missingness (optional)

Decide imputation strategy:

mean

median

domain-specific replacement

drop (only if safe)

🩺 5. Biological Zero Value Fixing

(Important for the Pima Diabetes dataset)

These features cannot be zero:

Glucose

BloodPressure

SkinThickness

Insulin

BMI

Steps:

Count how many zero values exist

Replace zeros using:

median of non-zero values

Document the number of changes made

🧽 6. Outlier Detection & Treatment
Visuals:

Boxplots

Distribution plots

Techniques:

IQR method

Winsorization (optional)

Removal only if strongly required

Document each decision clearly.

📊 7. Feature Distribution Analysis

For each numeric feature:

Histogram

KDE curve

Skewness

Kurtosis

Notes on distribution shape

Goals:

Understand natural behaviour of features

Identify transformation needs

Detect patterns

🔁 8. Skewness Treatment (if required)

If a feature is heavily skewed:

Apply log transform

Or Box-Cox / Yeo-Johnson transformation

Compare before/after distributions

Document the impact

🧬 9. Relationship Analysis
Pairwise Feature Relationships:

Correlation matrix

Heatmap

Pairplot (optional)

Scatterplots for key variables

Outcome-Based Analysis:

Compare features across Outcome = 0 vs 1

Boxplots

GroupBy summaries

Statistical differences (optional)

🧹 10. Duplicate Check
Goals:

Identify duplicate rows

Remove duplicates safely

Record total duplicates removed

📁 11. Create Final Cleaned Dataset

After all cleaning steps:

Check final shape

Check data integrity

Save cleaned file to:

data/interim/diabetes_cleaned.csv

Document:

Total cleaning operations

What was changed (summary)

Ready for Feature Engineering

📝 12. Key Insights Summary

Write human-readable insights:

Most important predictors

Feature behaviour

Relationship with diabetes outcome

Any domain-specific observations

This summary will be used in the project report.

📦 13. Next Steps

In the next notebook (03_Feature_Engineering.ipynb), we will:

Create new engineered features

Scale/normalize data

Handle class imbalance

Prepare data for modeling
