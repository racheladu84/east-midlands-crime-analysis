# East Midlands Crime Analysis with PySpark

Analysis of 2 years of UK street-level crime data (2023-2024) from Derbyshire, Leicestershire and Nottinghamshire, built with Apache Spark. The project covers data cleaning, Spark SQL analysis and visualisation of trends across three police forces.

**[View the notebook with outputs](crime-dataset.ipynb)**


## Highlights

- Processed 72 monthly CSV files (24 months x 3 forces) into a single Spark DataFrame using one wildcard read.
- Cleaned the data: standardised county names, renamed columns, profiled missing values and removed duplicate records.
- Used **Spark SQL** to measure total crime by county, monthly trends and crime type rankings.
- Built line, bar and pie charts to compare the counties (all in the notebook).

## Key Findings

- **Nottinghamshire** records the highest monthly crime levels of the three counties throughout the period.
- **Leicestershire** is the most stable, with the smallest swings from month to month.
- **Derbyshire** is the most variable, with its lowest month in November 2024.
- Crime tends to rise through spring and early summer, with more mixed patterns later in the year.
- Violence and sexual offences** is the most common crime type in all three counties.

## Tech Stack

- Python 
- PySpark (DataFrames, Spark SQL) 
- Pandas 
- NumPy 
- Matplotlib 
- Kaggle Notebooks

## Skills Demonstrated

- Big data processing with Apache Spark
- Data cleaning and quality checks (nulls, duplicates, schema inference)
- Feature engineering with `withColumn`, `when` and `substring`
- Analytical SQL with `GROUP BY` and ordering
- Data visualisation and communicating insights

## Approach

1. **Load and clean:** read all CSVs at once, mapped police force names to a `County` column, standardised column names, checked missing values and dropped duplicates.
2. **Analyse:** used Spark SQL for total crimes per county, monthly trends and crime type rankings.
3. **Visualise:** made a monthly trend line plot, a crime type bar chart and a pie chart for each county. The full set of charts is in the notebook.

## Data

UK police street-level crime data (January 2023 to December 2024) for Derbyshire, Leicestershire and Nottinghamshire, provided as part of a university module. The raw files (about 160 MB) are not included in this repo. All results are saved in the notebook outputs, so the project can be reviewed without running it.

## Limitations

- Covers recorded crime only.
- Raw counts are not adjusted for population, so they are not crime rates.
- Identical rows with no Crime ID (mostly anti-social behaviour) were treated as duplicates, which may slightly undercount those records.
- Some fields have missing values, for example Crime ID, Last outcome category and location details.

## Author 
Rachel Adu
