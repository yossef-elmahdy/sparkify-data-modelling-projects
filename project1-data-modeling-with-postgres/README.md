# Project 1: Data Modeling with PosgtreSQL 
Applying what I have learned on data modeling with Postgres and build an ETL pipeline using Python. To complete the project, you will need to define fact and dimension tables for a star schema for a particular analytic focus, and write an ETL pipeline that transfers data from files in two local directories into these tables in Postgres using Python and SQL.

## Schema for Song Play Analysis
Using the song and log datasets, you'll need to create a star schema optimized for queries on song play analysis. This includes the following tables.

### Fact Table
**`songplays`** - records in log data associated with song plays i.e. records with page NextSong 

`songplay_id`, `start_time`, `user_id`, `level`, `song_id`, `artist_id`, `session_id`, `location`, `user_agent`

### Dimension Tables
**`users`** - users in the app
`user_id`, `first_name`, `last_name`, `gender`, `level`

**`songs`** - songs in music database
`song_id`, `title`, `artist_id`, `year`, `duration`

**`artists`** - artists in music database
artist_id, name, location, latitude, longitude

**`time`** - timestamps of records in songplays broken down into specific units
`start_time`, `hour`, `day`, `week`, `month`, `year`, `weekday`

## Project Template
To get started with the project, go to the workspace on the next page, where you'll find the project template files. You can work on your project and submit your work through this workspace. Alternatively, you can download the project template files from the Resources folder if you'd like to develop your project locally.

In addition to the data files, the project workspace includes six files:

1. `test.ipynb` displays the first few rows of each table to let you check your database.
2. `create_tables.py` drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.
3. `etl.ipynb` reads and processes a single file from `song_data` and `log_data` and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables.
4. `etl.py` reads and processes files from `song_data` and `log_data` and loads them into your tables. You can fill this out based on your work in the ETL notebook.
5. `sql_queries.py` contains all your sql queries, and is imported into the last three files above.

![Song Play Star Schema ERD](https://github.com/yossef-elmahdy/sparkify-data-modelling-projects/blob/main/project1-data-modeling-with-postgres/erd.png)

You can explore the ETL pipeline python code from [here](https://github.com/yossef-elmahdy/sparkify-data-modelling-projects/blob/main/project1-data-modeling-with-postgres/etl-pipeline.ipynb)
