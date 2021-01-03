# COVID-19-Tracker

## Team
> * [_Matt Mead_](https://www.linkedin.com/in/mattmeadmpls/)
> * [_Emilio Bello_](https://www.linkedin.com/in/emilio-bello-09938760/)
> * [_Allan Hunt_](https://www.linkedin.com/in/allanrhunt/)

## Project Description
This info-kiosk style website interprets the infection and death rates from COVID-19 through October 2020 in choropleth map, calendar heatmap, and line graph forms to compare across the US states.  The information is pulled from an API and into a SQL database, then called through Python, Flask, and JavaScript to the website.

The project was part of the Fall 2020 University of Minnesota Data Analytics & Visualization Bootcamp and utilized environments created for that course.

## Tools Used
> * _Postgres SQL_
> * _Python_
> * _Flask Server_
> * _JavaScript_
> * _HTML & CSS_
> * _Leaflet_
> * _Jupyter notebook_

## Instructions for Data Setup & Site Launch:
1. Open config.py file, input your own Postgres password, and save.
2. Open static/js/config.js file, input your own Leaflet password, and save.
3. Launch Postgres server and create a database named "covid19-db"
4. In the covid19-db, open a Query Tool and run the 'covid_sql.sql' file
5. In a terminal window, type 'source activate NewPythonData' and then 'jupyter notebook'
6. In the 'TimeSeries' jupyter notebook click Kernel > Restart & Run All
7. Back in Postgres - go to covid19_db > Schemas > Tables
    * Right click on covid_data > Properties > Columns > In the 'state' row turn Primary key? to Yes
    * Right click on covid_hist > Properties > Columns > In the 'date' row turn Primary key? to Yes
    * Right click on covid_rolling > Properties > Columns > In the 'index' row turn Primary key? to Yes   
8. In a new Terminal Window, type 'source activate NewPythonData' and then 'python app.py' to run Flask Server
9. In a Chrome Browser window, go to http://127.0.0.1:5000/index.html

