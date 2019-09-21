# Lyft Data Challenge

A remote challenge presented by Lyft where students analyze three CSV files containing driver and ride information in order to determine a Driver's Lifetime Value (the value of a driver to Lyft over the entire projected lifetime of a driver)

A 5 page write-up was submitted at the end of the challenge to answer the following questions:
1. What are the main factors that affect a driver's lifetime value? 
2. What is the average projected lifetime of a driver? That is, once a driver is onboarded, how long do they typically continue driving with Lyft? 
3. Do all drivers act alike? Are there specific segments of drivers that generate more value for Lyft than the average driver? 
4. What actionable recommendations are there for the business? 

The three CSV files and their following column headers are:
1. driver_ids.csv 
   - **driver_id** Unique identifier for a driver
   - **driver_onboard_date** Date on which driver was on-boarded 
2. ride_ids.csv
   - **driver_id** Unique identifier for a driver
   - r**ide_id** Unique identifier for a ride that was completed by the driver
   - **ride_distance** Ride distance in meters
   - **ride_duration Ride** duration in seconds 
   - **ride_prime_time** Prime Time applied on the ride
3. ride_timestamp.csv
   - **ride_id** Unique identifier for a ride
   - **event** the type of event *(request, accept, arrival, picked up, dropped off)*
   - **timestamp** Time of event
