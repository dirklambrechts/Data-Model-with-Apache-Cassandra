# Udacity Nanodegree Program - Project 2 Data Modelling Apache Cassandra

## Table of Contents
1. [Description](#description)
2. [Using the notebook](#getting_started)
	1. [Requirements to run notebook](#dependencies)
	2. [Executing Program](#execution)
	3. [ETL pipeline and schema design](#pipeline_and_schema_design)
3. [Acknowledgements](#acknowledgements)
4. [Authors](#authors)


<a name="descripton"></a>
## Description

The purpose of this project is to create a Jupyter notebook that creates an Apache Cassandra database for a startup called Sparkify which is a music streaming application. This notebook can later be used as part of python scripts to implement an etl pipeline. Currently, there is no easy way to query the data they have collected through their music streaming application and the purpose of the etl pipeline is to store the data in an Apache Cassandra database to make running queries on the easier. The etl pipeline takes data currently stored in JSON log files and stores it in a Apache Cassandra database.

The main functionality of the etl pipeline includes:
1. Extracting the data from the JSON logs
2. Arranging the data into tables within an Apache Cassanrda database

<a name="getting_started"></a>
## Using the notebook

<a name="dependencies"></a>
### Requirements to run project
* Python 3.7+
* Data manipulation: pandas
* Apache Cassandra with Python: cassandra driver already installed (pip install cassandra-driver)
* Retrieve files and path names: glob and os

<a name="execution"></a>
### Executing Program:
1. Open the notebook and run the individual cells to run the code, or alternatively, run all cells.
    
<a name="pipeline_and_schema_design"></a>
### ETL pipeline and schema design:
The ETL pipeline reads in the application log data (provided by Sparkify) contained within the JSON files and arranges the data into a three different tables based on the following queries that are required:
1. Give me the artist, song title and song's length in the music app history that was heard during  sessionId = 338, and itemInSession  = 4
2. Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182
3. Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'

The table names are as follows:
1. song_in_session
2. artist_in_session
3. user_song

<a name="acknowledgements"></a>
## Acknowledgements
[Udacity](https://www.udacity.com/) for the second project of the data engineer nanodegree.
[Sparkify] for providing the data for the project. 

<a name="authors"></a>
## Authors

* [Dirk Lambrechts](https://github.com/dirklambrechts)