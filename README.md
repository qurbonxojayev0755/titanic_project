# Project: Titanic Passenger Data Analysis
## Project Goal
The goal of this project is to explore, clean, and process Titanic passenger data, identify key factors influencing survival, and visualize the findings.
Project Steps

<b>1. Exploratory Data Analysis (EDA)</b>
 - Import data from train.csv, test.csv, and gender_submission.csv files.
 - Perform initial exploration using .head(), .info(), and .describe() to understand data structure, check for missing values, and get a basic statistical overview.

<b>2. Data Cleaning</b>
- Handling Missing Values:
   - Age: Fill missing values with the median or mean based on passenger class and gender.
   - Embarked: Fill missing values with the most frequent value.
   - Cabin: Consider using only the first letter of the cabin or removing the column if it has limited analytical value.
   - Fare: Check for missing values and fill them with the median.

 - Outlier Treatment:
   - Identify potential outliers in Age and Fare, and determine appropriate handling (e.g., capping values or excluding outliers).

<b>3. Feature Engineering</b>
 - Extract passenger titles from the Name column and create a new feature (Title) to see its impact on survival.
 - Create a FamilySize feature based on the number of relatives onboard (SibSp and Parch).
 - Add a binary feature, IsAlone, indicating whether a passenger traveled alone.

<b>4. Data Visualization</b>
- Perform analysis on survival factors using the following visualizations:
   - Survival Histogram: Display the distribution of survivors vs. non-survivors.
   - Age Distribution Histogram: Show age distribution among survivors and non-survivors.
   - Box Plot of Fare by Class and Survival: Show Fare spread across classes and survival status.
   - Bar Chart for Class and Gender (Pclass, Sex): Compare survival rates across classes for males and females.
   - Grouped Bar Chart for FamilySize and Survival: Show the impact of family size on survival.
   - Pie Chart for Embarked: Display the survival and non-survival percentages by embarkation point.
   - Scatter Plot: Display the relationship between Age and Fare, with color indicating survival status.
   - Correlation Heatmap: Create a correlation matrix for numerical variables to uncover relationships between features.

<b>5. Data Aggregation & Grouping</B>
 - Group data by features like Pclass, Sex, Embarked, and FamilySize to analyze average survival rates within each group.
 - Use grouping and sorting to analyze relationships between ticket price and class (Pclass) as well as between family size and survival.

<b>6. Report Preparation</b>
 - Prepare a concise report on the data cleaning and processing approach, visualization insights, and key factors affecting passenger survival.
Summary
The project deliverables should include:
 - Cleaned data.
 - Set of visualizations showcasing key dependencies and findings.
 - Description of steps taken and a brief analysis of the results.


