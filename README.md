# NBA_SocialPower
# Extract, Transform and Load Project

## Overview
In this project, we chose to examine NBA players and their social power based on their stats during the 2016-2017 season. We were able to use the resources listed below to extract the data, then we used Python Pandas to transform the data and finally uploaded it into SQLite.

## Transformations
To transform the data, a variation of operations were performed. The original data was in the csv format and needed to be imported into Python to work with, and then transformed using Pandas. Some of the operations included dropping NaN values, dropping unnecessary columns, filtering the data, sorting the data and formatting the data. A detailed transformation breakdown of each of the data extracted is below:

Attendance.csv and Team_valuation.csv --> Merged the two files to one, created a new column "Team Ticker" but also dropped unnecessary column.Then formatted the TOTAL AND AVG colums values. Lastly set team as index and sorted the table in descending order based on Team_value.

Player_impact_estimation.csv and NBAstats.csv --> Imported both files into Jupyter. Then dropped a vast number of columns from each csv (each csv had 30 columns). In regards to the NBAstats.csv I dropped any rows with null values, and then I sorted the rows by MP or minutes played. I then took the Player_impact_estimation.csv and sorted by the MIN column or minutes played. Then changed the name of the rows to match the names of the NBAstats.csv. Finally, inner merged the two files on the player column. There were two identical MP columns so I deleted one of them, and then sorted the merged df by MP or minutes played.

ELO.csv --> Sorted the Conference and ELO values in descending order, renamed columns and set Conference as the index.

Endorsements --> Transformed Salary and Endorsement object data types into floats. Then sorted the data by Endorsement value first and then Salary value in descending order. Finally cleaned up the formatting of Salary and Endorsement columns.

Twitter --> Changed the column names, then sorted the values by Favorite Count and dropped any NaN rows. Finally filtered the players with greater than 100 Favorite count and reset the index.

Wikipedia --> Dropped unnecessary columns and then grouped the data by player name and summed their pageviews. Then the data was sorted by count and filtered for players with greater than 1000 page views. Finally it was finished with some formatting.

Attendance.csv and Team_valuation.csv --> Merged the two files to one, created a new column "Team Ticker" but also dropped unnecessary column.Then formatted the TOTAL AND AVG colums values. Lastly set team as index and sorted the table in descending order based on Team_value.

## Problems faced
Thanks to teamwork, we did not really face any significant challenges. The main challenge faced was during the loading of our data to sqlite, however we were able to figure it out.


## Resources
 1. Kaggle
 2. Basketball-Reference


