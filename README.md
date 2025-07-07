# ms1
IPC 144 Project - Milestone 1

Name: Han-Kuan Huang
Student number: 141140244
Seneca Username:hhuang143

Project Problems:

Look at the csv files (any file ending in .csv) that was provided to you in your repo.  In this first milestone you will explore the data provided to you and what it is that you will need to work with.

See milestone 1 specs for clarification.

Problem 1 (Easy level):


a) What data file(s) (from the set of provided files consisting of Olympic statistical information) will you need to answer the problem?
A:Olympic_Athlete_Event_Results.csv
Olympic_Games.csv
Olympic_Athlete_Country.csv
b) What column(s) (from within each data file) will you need to solve the problem?
From Olympic_Games.csv: year, season, and game_id
From Olympic_Athlete_Event_Results.csv: medal, athlete_id, and game_id
From Olympic_Athlete_Country.csv: athlete_id and noc
c) Is there any missing/incomplete data for the problem?
A:some of the weight and the height are -1, is missing.
d) Other than the data in the files, what other information will you need to solve the problem?
I need the user to input three things:
The year of the Olympics 
The season: Summer or Winter
The NOC code of the country 

e) For cases where the problems involve multiple files, how do you relate the data between the files ?
Here’s how I connect the files:
First, match the year and season with the game_id in Olympic_Games.csv

Then find all the medal records from Olympic_Athlete_Event_Results.csv that match that game_id
After that, use athlete_id to find the NOC (country code) from Olympic_Athlete_Country.csv
Finally, count how many of those medals are "Gold" and match the NOC

Problem 2 (Intermediate level):

a) What data file(s) (from the set of provided files consisting of Olympic statistical information) will you need to answer the problem?
I will use these three files:
Olympic_Athlete_Bio.csv
Olympic_Athlete_Event_Results.csv
Olympic_Games.csv
b) What column(s) (from within each data file) will you need to solve the problem?
From Olympic_Athlete_Bio.csv: athlete_id, name
From Olympic_Athlete_Event_Results.csv: athlete_id, game_id, medal
From Olympic_Games.csv: game_id, year, season

c) Is there any missing/incomplete data for the problem?
Yes, some medal fields might be empty. That means the athlete didn’t win anything in that game, but we still count that they joined. If the medal is missing, we just treat it as 0 for gold/silver/bronze.
d) Other than the data in the files, what other information will you need to solve the problem?
We need the user to input one thing only: the athlete_id.
From that, we can look up the athlete’s info and medal history.

e) For cases where the problems involve multiple files, how do you relate the data between the files ?
First, use the athlete_id to find the athlete’s name from Olympic_Athlete_Bio.csv. Then, use the same athlete_id in Olympic_Athlete_Event_Results.csv to get all their event records,Use the game_id from those results to look up the year and season from Olympic_Games.csv. For each Olympic edition, we count how many medals the athlete got (separated by gold, silver, bronze)





Problem 3 (Hard  level):

a) What data file(s) (from the set of provided files consisting of Olympic statistical information) will you need to answer the problem?
 Olympic_Athlete_Event_Results.csv
 Olympic_Athlete_Country.csv
Olympic_Games.csv


b) What column(s) (from within each data file) will you need to solve the problem?
From Olympic_Athlete_Event_Results.csv: event_id, medal, game_id, athlete_id
From Olympic_Athlete_Country.csv: athlete_id, noc
From Olympic_Games.csv: game_id, year, season

c) Is there any missing/incomplete data for the problem?

d) Other than the data in the files, what other information will you need to solve the problem?
I need the user to input:
The year of the Olympics (like 2010 or 2004)
The season (Summer or Winter)

e) For cases where the problems involve multiple files, how do you relate the data between the files ?
First, use year and season to find the right game_id from Olympic_Games.csv
Then get all medal results from Olympic_Athlete_Event_Results.csv with that game_id
For team sports, use event_id to make sure we only count one medal per event
Use athlete_id to find which country (NOC) they belong to from Olympic_Athlete_Country.csv
Count how many gold, silver, bronze medals each country has
Sort by gold → silver → bronze
Show the top 10 countries in a histogram using * to represent the number of gold medals

