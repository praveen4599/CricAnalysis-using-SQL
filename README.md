# CricAnalysis-using-SQL
My Custom data analysis using SQL

Our DBMS project is based on Cricket Analysis. It provides various information about the various teams participating in the World Cup, in which all the major countries participate. It also provides us with information about the various players participating in the tournament. The database contains details of players, coaches and umpires among others. All the useful information about the entire World Cup can be found here.

# Entities:

1)Teamis an entity type which has many attributes like Team Name which uses the data type varchar. Every team has been given aTeam ID which is the primary key which is of data type varchar. Team Ranking, Number of Batsmen and Number of Bowlers are of the data type number. There is another attribute -Wicketkeeper which is of multivalued type and accepts varchar data type. Primary key cannot have null value.

2)Playersis an entity type which has an attribute –Player Name which is of the data type varchar. It has a primary key, Player ID, which cannot have null value.It has a foreign key, Team ID which is theprimary key of the entity, Team. There is a complex attribute, Number of matches played, which comprises of Number of Test Matches, Number of T20 Matches, Number of World Cup Matches and Number of ODIs.

3)Batsmanis an entity type which has the attributes –Number of sixes hit, Number of Fours hit, the batting average, and the totalruns scored. All of these attributes are of the data type number.

4)Bowler is an entity type which has the attribute –type of batsman with varchar data type. It also includes number of wickets and economy which are of the data type number.

5)Umpire is an entitytypewhich has the attributes name and country of origin of data type varchar. The primary key of this is Umpire Id which is of varchar data type. It also has an attribute Number of matches of data type number.

6)Coach is an entity type with a foreign key, Team ID, which is  a primary key of entity type, Team. It has a primary key, Coach ID, of data type varchar. It also has another attribute of data type varchar, Name.

7)Captain is an entity type with a primary key, Captain ID of data type varchar. It has two foreign keys, 
i) Player id from table Players and 
ii) Team ID from table Team. Number of years of captaincy and Number of wins are also attributes of this table of data type number.

8)Matches is an entity type with a primary key, match ID, of varchar data type.It has attributes like Team1Name, Team2 Name, Stadium, Winner Team and Loser Team of data type varchar. Match date is an attribute which uses the datatype date. Match time is an attribute which is of the data type time.

# Relationships:

Cricket player plays in team (N-1):
A cricket player can play in only one team but a team can have many players in it but a team must have players in it. So, the relationship becomes (N-1).

Coach manages team(1-N):
Coach can manage a single team, but each team can have many coaches (like batting coach, fielding coach, bowling coach). But it is compulsory for a team to have a coach. So, the relationship is 1-N.

Team plays match(M-N):
Team can play many matches and a match can be played by two teams. So, the relationship is M-N. 

Matches are umpired by Umpire(M-N):
An umpire can umpire in many matches and a match can have two umpires. So, the relationship is M-N.

Team headed by a Captain (1-1):
A team has 1 captain and a captain is from single team only. So the relationship is 1-1.

