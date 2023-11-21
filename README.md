# sqlalchemy-challenge

## Instructions
Congratulations! You've decided to treat yourself to a long holiday vacation in Honolulu, Hawaii. To help with your trip planning, you decide to do a climate analysis about the area. 

## Description 

### Part 1: Analyze and Explore Climate Data 

Tools and Functions: The file provided was an SQLite file named "Hawaii". To analyze this file I used the python tool SQLAlchemy. Specifically the "create_engine()" function to connect to the database and "automap_base()" to reflect tables into classes. The two classes were: station and measurement.

Session Management: A SQLAlchemy session is created to interact with the database. It is VERY important to end this session when finished. If left open, it can lead to resource leakage, database locks, stale data and much more. 

Precipitation Analysis: First, I had to find the most recent date in the dataset. Then query the last 12 months of precipitation data. Then load the data into a Pandas DataFrame, sort by date, and plot the results. Lastly, I had to generate summary statistics for the precipitation data.

Station Analysis: First, I had to determine the total number of stations. Then identify the most active stations and list them in descending order of observation counts; for the most active station, I needed to calculate the lowest, highest, and average temperatures. Then query the last 12 months of temperature observation data (TOBS) for this station and plot the results as a histogram.

### Part 2: Design A Climate App

Flask API Development: First, I had to develop a Flask API based on the data queries I just ran. 

The Route Creation was as follows:

Homepage (/): List all available routes.

Precipitation (/api/v1.0/precipitation): Convert precipitation analysis results into a dictionary and return the JSON representation.

Stations (/api/v1.0/stations): Return a JSON list of stations.

Temperature Observations (/api/v1.0/tobs): Query and return a JSON list of temperature observations for the most active station over the 	previous year.

Date Range Queries (/api/v1.0/<start> and /api/v1.0/<start>/<end>): Return a JSON list of the minimum, average, and maximum temperatures for a given start date or date range.

## Summary
This project is a combination of data exploration and web development. I analyzed climate data using Python tools like SQLAlchemy, Pandas, and Matplotlib, and then created a Flask application to make this data accessible via a web API. The goal was to use data analysis to enhance vacation planning in Honolulu, Hawaii; using insights from historical weather patterns.

## Contributors
For this project I used: Jupyter Notebooks, GitBash operating in my Terminal, Visual Studio Code, Notepad, Google Chrome, and Chat GPT. I worked with several classmates (Kirby, Mallorie, Jonathan, and Tye) and I got a ton of help from askBCS, my favorite TA ever Javier, and the professor Ariel who helped me get the Chromedriver to finally work! 


