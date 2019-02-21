# ETL-Project

ETL PROJECT

Purpose:
--------

Create a data set that contains a representative sample of stocks in varying industries and of varying company sizes for analysis.

Data Sources:
-------------

Spyder ETF Large Cap Fund (csv file)
Spyder ETF Medium Cap Fund (csv file)
Spyder ETF Small Cap Fund (csv file)
IEXTrading API (json)

The Spyder ETFs were used to create a representative list of large to small cap stocks. 
IEXTrading API was used to obtain current stock prices and key statistics.

Extract:
--------
- ETF holdings for each fund were imported to pandas dataframe from csv files.
- Current stock prices and key statistics were imported to panadas dataframe using API query.

Transform:
----------

For CSV Files:
- Each CSV files was checked for null values and verified they contained the appropriate data types and column structure.
- A column was added to label each stock as a Lg, Med, or Small Cap Stock.
- Combined all 3 files to a single dataframe.

For JSON output:
- Determined dictionary structure of json output to determine the location of required data.
- Used for loop to append query result to individual lists
- Added lists to dataframe created from csv files.

Load:
-----
Exported completed table to excel file.

