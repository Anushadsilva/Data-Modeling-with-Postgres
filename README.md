DataModelingUsingPostgres

Objective:
Aim is to build an ETL pipeline using Python and design data modeling with Postgres

Introduction
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.
Applying what I've learnt on data modeling with Postgres and try building an ETL pipeline using Python
They'd like a data engineer to create a Postgres database with tables designed to optimize queries on song play analysis. My aim is to create a database schema and ETL pipeline for this project.

Project Description
Using the datasets song and log, I tried creating a star schema optimized for queries on song play analysis. This includes the below tables.

Fact Table
songplays - records in log data associated with song plays i.e. records with page NextSong
songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

time - timestamps of records in songplays broken down into specific units
start_time, hour, day, week, month, year, weekday

Dimension Tables
users - users in the app
user_id, first_name, last_name, gender, level

songs - songs in music database
song_id, title, artist_id, year, duration

artists - artists in music database
artist_id, name, location, latitude, longitude


Project :

Create Tables
Write CREATE statements in sql_queries.py to create each table.
Write DROP statements in sql_queries.py to drop each table if it exists.
Run create_tables.py to create your database and tables.
Run test.ipynb to confirm the creation of tables with the correct columns.
Build ETL Pipeline
Develop ETL processes for each table in the etl.ipynb notebook. Use it to complete etl.py, where the entire datasets will get processed.