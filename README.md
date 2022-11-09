# EDA-MTA Traffic & Citibike Capacity

For full Power Point presentation, click [here.]()

## **Abstract**

The link between the Subway and Citi Bike plays an important role in building a more resilient transportation system. Taking into account the relationship between both mode of transports, Citi Bike wants to understand what are the most active transportation hubs in NY. The goal of this project is to identify traffic hubs that are underserved by Citi Bike by analyzing MTA Traffic. 

## **Design**

One year worth of MTA Traffic data was analyzed to find busiest stations at the turnstile and station level. The analysis consisted of looking at traffic patterns in terms of day of the week and time. In order to study the relationship between MTA and Citi Bike Traffic, one year worth of Citi Bike Trips Data was also analyzed by looking at traffic patterns at the station level. 

Taking into account the findings from the Traffic Analysis, I looked at Citi Bike Stations in a 0.3 miles radius of top Stations, comparing MTA Traffic to Citi Bike Stations capacity in this defined radius. 

## **Data**

Two types of datasets were analyzed: Traffic Data and Location Data.

**Traffic Datasets:**

MTA Turnstile Dataset between June 2021 and May 2022. Each row of data represents the cumulative number of Entries and Exits per turnstile every four hours. Features of interest: Station, *C/A : Control Area, Unit:Remote Unit for station, SCP : Subunit Channel Position, Date,Time,Entries,Exits.*

Citi Bike Trips Dataset between June 2021 and May 2022. Each row of data represents a unique trip. Features of Interest: Start Station Name, End Station Name, Start Time, End Time, Ride ID.

**Location Datasets:**

MTA Stations Location Dataset. Features of Interest: Station Name,Longitude,Latitude.

Citi Bike Stations Location Dataset. Features of Interest: Station Name, Longitude, Latitude, Capacity.

## **Process**

**Database Creation** 

SQLite was used to create a database where all the dataset mentioned above were stored. After that, SQLAlchemy was used to load and analyze the data using Pandas. 

**Data cleaning**

Adjusting column names, dropping duplicates and null values, plotting distributions to drop outliers and nonsensical values. 

**Data Analysis**

MTA Turnstile Data: Aggregation of entries and exits at the turnstile and station level at given days of the week and time. 

Citi Bike Trips Data: Aggregation of start and end station’s count to determine frequency of use. Calculation of Distance (Haversine) between MTA Stations and Citi Bike Stations in a 0.3 miles radiusMTA Traffic: Citi Bike Stations Capacity in a 0.3 miles radius. 

## **Tools**

**Data Storing and Preliminary Analysis:** SQLite and SQLAlchemy.

**Data Analysis:** Pandas, Geopy.

**Data Visualization:** Matplotlib, Seaborn, Folium.
