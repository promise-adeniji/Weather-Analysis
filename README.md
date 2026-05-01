
Weather Analysis
📌 Project Overview
This project performs a full Exploratory Data Analysis (EDA) on an hourly weather dataset for the city of Winnipeg, Canada, covering the entire year of 2012. Using Python and Pandas, the project answers 15 analytical questions that progressively build in complexity — from basic data inspection to conditional multi-filter queries.
This project demonstrates practical proficiency in data wrangling, querying, grouping, aggregation, and descriptive statistics — core skills for any data analyst or data scientist role.

🛠️ Tech Stack

Language: Python 3.10+
Core Libraries: pandas, numpy
Environment: Jupyter Notebook
Data Format: CSV

🔍 Analyses Performed
The project answers 15 key analytical questions, organized from foundational to advanced:
🔑 Data Inspection

Loaded and explored the dataset using .head(), .shape, .dtypes, .info()
Identified all column names, data types, and record counts
Confirmed zero null values across all 8,784 entries using .isnull().sum()

🌬️ Querying & Filtering

Q1: Retrieved all 34 unique wind speed values using .unique() and .nunique()
Q2: Found 1,326 hours of exactly "Clear" weather using boolean filtering and .groupby()
Q3: Identified 474 records where Wind Speed was exactly 4 km/h
Q9: Extracted all 390 rows where Weather Condition contained "Snow" — including compound conditions like Snow Showers and Freezing Drizzle, Snow using .str.contains()
Q10: Filtered for Wind Speed > 24 km/h AND Visibility = 25 km simultaneously (308 records)

📊 Descriptive Statistics

Q6: Calculated mean visibility → 27.66 km
Q7: Computed standard deviation of atmospheric pressure → 0.844 kPa
Q8: Found variance of relative humidity → 286.25

🗂️ Aggregation & Grouping

Q11: Used .groupby('Weather Condition').mean() to compute mean values of all numeric columns per weather type — surfacing insights like Thunderstorm hours averaging 24.1°C vs. Snow averaging −4.5°C
Q12: Applied .groupby().min() and .groupby().max() to find extremes per condition, revealing temperature swings from −23.3°C (Clear) to 33.0°C (Mainly Clear)

🔎 Advanced Multi-Condition Filtering

Q14: Combined OR conditions — Clear weather or Visibility > 40 km
Q15: Applied compound AND/OR logic — (Clear AND Humidity > 50%) OR Visibility > 40 km → 2,921 matching records

🧹 Data Cleaning & Transformation

Q5: Renamed column Weather → Weather Condition using .rename() with inplace=True


💡 Key Findings

Most common condition: "Mainly Clear" with 2,106 hours (≈24% of the year)
Snow was recorded in 390 hours of exactly "Snow" — expanding to far more when compound conditions (e.g., Snow Showers, Freezing Drizzle, Snow) are included
The dataset is completely clean — no imputation or handling of nulls was required
Winnipeg's 2012 temperatures ranged from a minimum of approximately −23°C to a peak of 33°C, reflecting its extreme continental climate
Thunderstorm conditions, though rare (only 2 records), had the highest average temperature of all weather types at 24.15°C

👤 Author
Promise Adeniji

📧 [adeniji.promise6@gmail.com]
💼 [https://www.linkedin.com/in/promiseadeniji/]
