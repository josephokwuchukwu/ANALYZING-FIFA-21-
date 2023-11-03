# ANALYZING-FIFA-21-
30 Days DuckDB Challenge On FIFA 21 Player Dataset Analysis

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/e962fa62-681e-463b-805c-457b199a6f6a)


# DAY 1 CHALLENGE: SETTING UP MY WORKING ENVIRONMENT

**.** Created an account with MotherDuck

**.** Installed DuckDB through the installation instructions and guide provided



# WEEK 2 

# DAY 2 & 3 CHALLENGE: 

(a) I created a  DuckDB database named **TheChallenge**

(b) I imported the two datasets needed **fifa21_raw_data** and **fifa21_raw_data_v**

(c) I connected the MotherDuck for collaboration and accessibility by my teams

CREATE TABLE IF NOT EXISTS fifa21_raw_data_v AS
SELECT * 
FROM read_csv_auto("C:\Users\CHICHI\Desktop\Fifa\fifa21 raw data v2.csv") limit 10;


CREATE OR REPLACE TABLE fifa21_raw_data 
AS SELECT * 
FROM read_csv_auto(["C:\Users\CHICHI\Desktop\Fifa\fifa21_raw_data.csv"])limit 10;



