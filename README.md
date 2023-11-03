# ANALYZING-FIFA-21
# 30 Days DuckDB Challenge On FIFA 21 Player Dataset Analysis "Unraveling the Magic of FIFA: A Data Analysis Journey"

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/e962fa62-681e-463b-805c-457b199a6f6a)

# Introduction
Welcome,

I'll be working with two datasets, Fifa_21_raw1 and Fifa_21_raw2, both featuring identical column names. These datasets contain football (soccer) player information from the FIFA 21 video game. They encompass details such as player names, nationalities, ages, positions, club affiliations, contract dates, and a wide array of performance metrics.

The #30daysduckdbchallenge has been an extraordinary journey in the realm of data analysis. It has not only honed my SQL skills but has also showcased the capabilities of DuckDB in effectively managing real-world data challenges. 

You can find all the SQL code used here, as written in **DUCKDB** ![Here](https://github.com/Chichi126/ANALYZING-FIFA-21-/commit/71309a5f76f81bfd57e22478ebb10c32328bf840)

Here's an overview of the key columns in this datasets:

- **ID**: A unique identifier for each player.
- **Name**: The player's name.
- **LongName**: The player's full name.
- **photoUrl**: URL to the player's photo.
- **playerUrl**: URL to the player's profile.
- **Nationality**: The player's nationality.
- **Age**: The player's age.
- **OVA**: Overall rating.
- **POT**: Potential rating.
- **Club**: The player's current club.
- **Contract**: Contract details.
- **Positions**: The player's preferred positions.
- **Height**: The player's height.
- **Weight**: The player's weight.
- **Preferred Foot**: The player's preferred foot (left or right).
- **BOV**: Best overall position.
- **Best Position**: The player's best position.
- **Joined**: The date the player joined their current club.
- **Loan Date End**: The end date of any loan agreement.
- **Value**: The player's market value.
- **Wage**: The player's wage.
- **Release Clause**: The release clause value.
- Various attributes and ratings related to attacking, defending, skill, movement, and goalkeeping.

This dataset is rich in information about FIFA 21 players, making it an excellent resource for various data analysis and visualization tasks, especially for fans of the game or those interested in football statistics. You can explore player performance, club affiliations, potential stars, and more.

# WEEK 1 

## DAY 1 CHALLENGE: SETTING UP MY WORKING ENVIRONMENT

**.** Created an account with MotherDuck

**.** Installed DuckDB through the installation instructions and guide provided





## DAY 2 & 3 CHALLENGE: 

(a) I created a  DuckDB database named **TheChallenge**

(b) I imported the two datasets **fifa21_raw_data** and **fifa21_raw_data_v**

(c) I connected the MotherDuck for collaboration and accessibility by my teams

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/a8187a89-af6a-4544-baac-31cf5a5a3b42)


![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/b3306d0d-419f-4a0f-af0e-1156c715d938)




# WEEK 2 

### Day 4 to 6 Challenge: Data Cleaning Process

a) Converting Height and Weight to Numerical Form: For the 'Height' column, make sure to extract the numerical value (e.g., 6'0" becomes 6). For the 'Weight' column, remove the "lbs" and convert it to a numerical format.

b) Converting 'Value', 'Wage', and 'Release Clause' to Numbers:

c) The 'Value' column has values like '€100M' (which means 100 million) and '€10K' (which means 10,000). Strip the symbols ('€', 'M', 'K') and convert the values to actual numbers accordingly.

d) The 'Wage' column also uses 'K' (e.g., '€100K'), which should be converted to thousands.

e) The 'Release Clause' column follows the same pattern with 'M' and 'K'. Handling 'Star' Characters:

f) Remove the 'star' character from columns where it appears and make sure the columns are in numerical format.

i) Converted the 'Hits" column to an integer 

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/1d43939b-aa3b-4284-8aab-dbf4d1f23ed3)



### Day 7-9 Challenge: Querying the Datasets for insights

### a) Identify players who possess high value but receive relatively low wages.

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/d09ec31b-2495-4ac0-b786-edd574fe1e0d)


### b) Determine the count of players available in the dataset for each position.

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/9385298e-41f6-402d-bc5a-15c4fee68521)


### c) Find out which club has the largest representation of players in the dataset.

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/db63f629-bbce-4b11-bdbe-398a98d9e592)


### d) List the top 10 players with the highest OVA and POT values.

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/56e43e13-5d08-4696-ba89-3f1810f35331)


### f) Find players with the highest OVA and POT within each club.

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/d47c6525-b55b-4ff8-afc2-dc960c90bb4c)

### g) Calculate the average OVA for players under 25 years old and over 30 years old in each club.

**_-> Using case statement to specify each condition_**

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/d94efb4d-b91a-4356-95c1-672eaa0eab84)


### h) List the players who are the same age within each club.

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/53f63046-479a-4e4d-a406-d2af98591725)



### i) Find the player with the highest POT for each nationality

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/50b3cafd-bf0b-4202-b415-d742d963214d)


### j) Rank players by their OVA in descending order within each club

![image](https://github.com/Chichi126/ANALYZING-FIFA-21-/assets/140970592/2c1ca7d0-781c-41c9-acfc-4d20aaf3ff21)


# CONCLUSION AND OBSERVATION

The analysis of the FIFA 21 dataset has provided valuable insights into the world of football (soccer) and the digital representation of players in the popular FIFA video game. This analysis has allowed us to draw meaningful conclusions and understand the importance and benefits of working with such datasets.

**Key Findings and Insights:**
1. **Player Profiling:** We've gained a comprehensive understanding of individual players, including their performance metrics, preferred positions, and attributes. This   
   information can be invaluable for gamers and football enthusiasts looking to make informed decisions about player selection in the game.

2. **Club and Contract Data:** The dataset sheds light on the relationships between players and their respective clubs, along with contract's details. This can be beneficial 
   for club management simulations, career mode enthusiasts, and fantasy football players.

3. **Market Value and Wage:** We've learned about the market values and wages of players. This data can be useful for evaluating player economics in the context of real-- 
   world football transfers.

4. **Nationality and Age Analysis:** The dataset allows for demographic analysis, such as the distribution of players by nationality and age, which can be insightful for 
   assessing the diversity and age composition of the player pool.

5. **Market Analysis:** Understanding player values and wages can be vital for sports marketers, sponsors, and clubs to gauge the marketability and financial implications 
   of player endorsements.



In conclusion, the FIFA 21 dataset not only enhances the gaming experience but also extends its utility to the real-world football industry, research, and education. It highlights the power of data analysis in making informed decisions and exploring the diverse aspects of the beautiful game. Whether for entertainment, research, or professional purposes, the importance and benefits of such datasets are undeniable, and they continue to play a vital role in the ever-evolving landscape of sports analytics and gaming.














