## Commands for HIVE
create database emp1   --> creates database with name emp1


show database   --> displays all the databases


create table employees (ID int, Name string, Salary float) ROW FORMAT DELIMITED fields terminated by ',';   --> create a table inside default database with given schema
create table emp1.employees (ID int, Name string, Salary float) ROW FORMAT DELIMITED fields terminated by ',';   --> create a table inside emp1 database with given schema


use <database name>  --> to set the database

ALTER TABLE emp1.employees RENAME TO employee;   --> change table name



### Create table for Continuous dataset from this link -->  https://www.kaggle.com/datasets/jaykay12/odi-cricket-matches-19712017
create table shanu.cricket (ID int, Scorecard string, Team1 string, Team2 string, Margin string, Ground string, MatchDate string, Winner string, HostCountry string, VenueTeam1 string, VenueTeam2 string, InningsTeam1 string, InningsTeam2 string) 
ROW FORMAT DELIMITED 
FIELDS TERMINATED BY ','
LINES TERMINATED BY "\n"
STORED AS TEXTFILE;


### Load data
LOAD DATA INPATH '/user/shanujha/cricket/ContinuousDataset.csv' INTO TABLE shanu.cricket;

