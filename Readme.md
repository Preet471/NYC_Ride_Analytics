# NYC Taxi Ride Analytics Dashboard

## Overview
This project is an interactive Power BI dashboard built to analyze NYC taxi ride data. It provides insights into ride patterns, revenue trends, customer behavior, and operational performance. The goal is to understand how taxi services are used and identify key trends such as peak demand hours, popular pickup locations, and payment preferences.

## Tools Used
- Power BI
- Excel / CSV dataset
- DAX (Data Analysis Expressions)
- Data cleaning and transformation

## Process
- Collected NYC taxi ride dataset
- Performed data cleaning (handled missing values, data types)
- Created derived columns using Power BI
- Built measures using DAX
- Designed interactive dashboard with key KPIs and visuals

## Data Dictionary

## Raw Data Columns
| Column                | Meaning                                                                       |
|---------------------- |-------------------------------------------------------------------------------|
| VendorID              | Taxi company identifier (1 or 2)                                              |
| tpep_pickup_datetime  | Trip start date and time                                                      |
| tpep_dropoff_datetime | Trip end date and time                                                        |
| passenger_count       | Number of passengers in the ride                                              |
| trip_distance         | Distance travelled in miles                                                   |
| RatecodeID            | Type of rate used for the trip (standard, airport, negotiated fare, etc.)     |
| store_and_fwd_flag    | Indicates if trip data was stored before sending to server (Y = Yes, N = No)  |
| PULocationID          | Pickup location zone ID in NYC taxi zones                                     |
| DOLocationID          | Drop-off location zone ID in NYC taxi zones                                   |
| payment_type          | Payment method used (1 = Credit Card, 2 = Cash, 3 = Dispute, 4 = No Charge)   |
| fare_amount           | Base fare charged for the trip                                                |
| extra                 | Additional charges (night fee, peak hour surcharge, etc.)                     |
| mta_tax               | Fixed Metropolitan Transportation Authority tax                               |
| tip_amount            | Tip given by passenger                                                        |
| tolls_amount          | Toll charges incurred during trip                                             |
| improvement_surcharge | Small regulatory surcharge per trip                                           |
| congestion_surcharge  | Extra charge for trips in congestion zones (e.g., Manhattan)                  |
| Airport_fee           | Additional fee for airport pickups/drop-offs                                  |
| total_amount          | Final total fare including all charges                                        |

## Derived Columns (Created in Power BI)
| Column                | Meaning                                           |
| --------------------- | ------------------------------------------------- |
| Trip_Duration_Minutes | Time difference between pickup and drop-off       |
| hour                  | Extracted hour from pickup time                   |
| Time_Bucket           | Grouped time into Morning/Afternoon/Evening/Night |
| Payment_Label         | Converted payment type into readable labels       |

## Key Insights
- Peak ride demand is highest in the afternoon
- Around 81% of payments are made using credit card, making it the most preferred payment method
- JFK Airport is the top pickup zone by number of rides

## Dashboard
![Dashboard](Dashboard.png)