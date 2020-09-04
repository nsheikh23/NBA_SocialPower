# NBA_SocialPower
# Extract, Transform and Load Project

## Overview
In this project, we chose to examine NBA players and their social power based on their stats. We were able to use the resources listed below to extract the data, then we used Python Pandas to transform the data and finally uploaded it into SQLite.

## Transformations
To transform the data, a variation of operations were performed. The original data was in the csv format and needed to be imported into Python to work with, and then transformed using Pandas. Some of the operations included dropping NaN values, dropping unnecessary columns, filtering the data, sorting the data and formatting the data. A detailed transformation breakdown of each of the data extracted is below:

ELO.csv --> Sorted the Conference and ELO values in descending order, renamed columns and set Conference as the index.

Endorsements --> Transformed Salary and Endorsement object data types into floats. Then sorted the data by Endorsement value first and then Salary value in descending order. Finally cleaned up the formatting of Salary and Endorsement columns.

Twitter --> Changed the column names, then sorted the values by Favorite Count and dropped any NaN rows. Finally filtered the players with greater than 100 Favorite count and reset the index.

Wikipedia --> Dropped unnecessary columns and then grouped the data by player name and summed their pageviews. Then the data was sorted by count and filtered for players with greater than 1000 page views. Finally it was finished with some formatting.

## Resources
 1. Kaggle
 2. Basketball-Reference


