# Database Setup Part 1
The analysis utilizes a SQLite database, hawaii.sqlite, containing two tables: measurement and station. SQLAlchemy's automap_base feature is used to reflect the tables into classes and start a session to query the database.

## Climate Analysis and Exploration
To begin the analysis, the most recent date in the dataset is found. A query is then designed to retrieve the last 12 months of precipitation data, plot the results, and perform a summary statistics calculation.

## Precipitation Analysis
The query results are saved to a Pandas DataFrame and plotted using Matplotlib.
Summary statistics are calculated for the precipitation data.
## Station Analysis
Total number of stations is calculated.
A query identifies the most active stations, i.e., stations with the highest number of observations.
Temperature observations for the most active station for the last 12 months are queried and plotted as a histogram.

# Climate Analysis API Part 2

## Overview
The Climate Analysis API is a Flask-based web service designed to provide access to historical weather and climate data. Built using Python, SQLAlchemy, and Flask, this API serves data from the hawaii.sqlite database, offering insights into temperature trends, precipitation, and station information.
## API Endpoints

### `/api/v1.0/precipitation`
Returns JSON data about precipitation.

### `/api/v1.0/stations`
Lists all weather observation stations.

### `/api/v1.0/tobs`
Shows temperature observations for the last year from the most active station.

### `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`
Returns temperature statistics (min, avg, max) starting from <start> date or between <start> and <end> dates. Dates should be provided in YYYY-MM-DD format.
## Example Requests
- Precipitation data: `http://localhost:5000/api/v1.0/precipitation`
- Station list: `http://localhost:5000/api/v1.0/stations`
- Temperature observations: `http://localhost:5000/api/v1.0/tobs`
- Temperature stats from a start date: `http://localhost:5000/api/v1.0/2017-01-01`
- Temperature stats for a date range: `http://localhost:5000/api/v1.0/2017-01-01/2017-01-07`


