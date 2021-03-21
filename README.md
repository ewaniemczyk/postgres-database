## Data Modeling with Postgres

### I. Business discription

This is postgres database created by Sparkify to analyze the data collected on songs and user activity on the new music streaming app.

### II. Technical discription

Data is collected from JSON files of two types: song and logs. Those data is placed in 5 tables of star schema with one fact table and four dimension tables.

The solution contains ETL process & pipeline.

***Fact Table***
songplays - records in log data associated with song plays i.e. records with page NextSong

songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

***Dimension Tables***

1. users - users in the app
user_id, first_name, last_name, gender, level

2. songs - songs in music database
song_id, title, artist_id, year, duration

3. artists - artists in music database
artist_id, name, location, latitude, longitude

4. time - timestamps of records in songplays broken down into specific units
start_time, hour, day, week, month, year, weekday


### III.How to run Python scripts

1.run file before_run.ipynb - it will create database, tables
2.run file etl.ipynb - it will develop the ETL process
