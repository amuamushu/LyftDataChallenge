# Lyft Data Challenge

A remote challenge presented by Lyft where students analyze three CSV files containing driver and ride information in order to determine a Driver's Lifetime Value (the value of a driver to Lyft over the entire projected lifetime of a driver)

**Table of Content**
[Tools/Techonology Used](https://github.com/amuamushu/LyftDataChallenge/blob/master/README.md#toolstechnology-used)
[How we caculated Driver Lifetime Value](https://github.com/amuamushu/LyftDataChallenge/blob/master/README.md#how-we-calculated-driver-lifetime-value)
[Contributions](https://github.com/amuamushu/LyftDataChallenge/blob/master/README.md#contributions)

### A 5 page write-up was submitted at the end of the challenge to answer the following questions:
1. What are the main factors that affect a driver's lifetime value? 
2. What is the average projected lifetime of a driver? That is, once a driver is onboarded, how long do they typically continue driving with Lyft? 
3. Do all drivers act alike? Are there specific segments of drivers that generate more value for Lyft than the average driver? 
4. What actionable recommendations are there for the business? 

### The three CSV files and their following column headers are:
1. driver_ids.csv 
   - **driver_id** Unique identifier for a driver
   - **driver_onboard_date** Date on which driver was on-boarded 
2. ride_ids.csv
   - **driver_id** Unique identifier for a driver
   - **ride_id** Unique identifier for a ride that was completed by the driver
   - **ride_distance** Ride distance in meters
   - **ride_duration Ride** duration in seconds 
   - **ride_prime_time** Prime Time applied on the ride
3. ride_timestamp.csv
   - **ride_id** Unique identifier for a ride
   - **event** the type of event *(request, accept, arrival, picked up, dropped off)*
   - **timestamp** Time of event
   
## Tools/Technology Used
1. Python Pandas package
   - used to combine the columns from the various spreadsheets and group data by identifiers such as driver id and ride id
   - used to create CSVs with new grouped columns
2. Datatime Module
   - used to convert the given timestamps to datetime objects for easy comparisions and grouping
3. Tableau
   - used to visialize the data from the inputted CSVs
4. Jupyter Notebook
   - used for data exploration 

## How we calculated Driver Lifetime Value
We created a formula, which takes into account (as a percentile):
- the driver retention period
- ratio of number of rides to total distance from all rides *(we discovered that shorter rides are more beneficial to Lyft because drivers are driving more often and the base fare ensure that Lyft receives a minimum amount regardless of how far or long the ride is)*
- sum of all prime times the driver drove in
- sum of how long the riders waited for the driver.

## Contributions

**Amy Nguyen** 
- calculated the formula for a driver's lifetime value on a table. This was done so by using Pandas to merge the CSVs and group rows on driver id.
- calculated driver rentention using the given ride_ids and timestamps CSVs. The CSVs were merged ride_id and grouped by driver_id to get the max and min ride times (the oldest and latest rides). The max and min ride time columns were then converted to datatime objects in order to subtract them and get the period in which they were driving (the difference). 

**Madeline**
- created all of the graphs and visualizations using Tableau
