
# Airline On-Time Performance Data
## by João Victor Moreira de Figueiredo

Reporting carriers are required to (or voluntarily) report on-time data for flights they operate: on-time arrival and departure data for non-stop domestic flights by month and year, by carrier and by origin and destination airport. Includes scheduled and actual departure and arrival times, canceled and diverted flights, taxi-out and taxi-in times, causes of delay and cancellation, air time, and non-stop distance.

This project explore twelve months of flights, starting at May 2019 to April 2020.

Link to original source:
 <https://www.transtats.bts.gov/DL_SelectFields.asp?Table_ID=236>

Fields are selected based on this page:
<http://stat-computing.org/dataexpo/2009/the-data.html>

## Dataset and supplementary data

1. [Download dataset files](https://1drv.ms/u/s!ArfbtT2XOWRwhNV1m_wLJotkXAa76A?e=xlxbwe)
12 files that make up the dataset. Instructions are in jupyter notebook 'exploration_template' file.

2. [Download supplementary data](https://1drv.ms/u/s!ArfbtT2XOWRwhNYCeQd9zXfDooPaBw?e=3PdmNT)
You need to download supp data only if the source webpage is not online. Instructions are in jupyter notebook 'exploration_template' file.

### Table of contents

**Time Period**<br/>
YEAR<br/>
MONTH<br/>
DAY_OF_MONTH<br/>
DAY_OF_WEEK<br/>
**Airline**<br/>
OP_UNIQUE_CARRIER - Unique Carrier Code. When the same code has been used by multiple carriers, a numeric suffix is used for earlier users, for example, PA, PA(1), PA(2). Use this field for analysis across a range of years.<br/>
TAIL_NUM - Tail number<br/>
OP_CARRIER_FL_NUM - Flight Number<br/>
**Origin**<br/>
ORIGIN - Origin Airport<br/>
**Destination**<br/>
DEST - Destination Airport<br/>
**Departure Performance**<br/>
CRS_DEP_TIME - CRS Departure Time (local time: hhmm)<br/>
DEP_TIME - Actual Departure Time (local time: hhmm)<br/>
DEP_DELAY - Difference in minutes between scheduled and actual departure time. Early departures show negative numbers.<br/>
TAXI_OUT - Taxi Out Time, in Minutes<br/>
**Arrival Performance**<br/>
TAXI_IN - Taxi In Time, in Minutes<br/>
CRS_ARR_TIME - CRS Arrival Time (local time: hhmm)<br/>
ARR_TIME - Actual Arrival Time (local time: hhmm)<br/>
ARR_DELAY - Difference in minutes between scheduled and actual arrival time. Early arrivals show negative numbers.<br/>
**Cancellations and Diversions**<br/>
CANCELLED - Cancelled Flight Indicator (1=Yes)<br/>
CANCELLATION_CODE - Specifies The Reason For Cancellation<br/>
DIVERTED - Diverted Flight Indicator (1=Yes)<br/>
**Flight Summaries**<br/>
CRS_ELAPSED_TIME - CRS Elapsed Time of Flight, in Minutes<br/>
ACTUAL_ELAPSED_TIME - Elapsed Time of Flight, in Minutes<br/>
AIR_TIME - Flight Time, in Minutes<br/>
DISTANCE - Distance between airports (miles)<br/>
**Cause of Delay**<br/>
CARRIER_DELAY - Carrier Delay, in Minutes<br/>
WEATHER_DELAY - Weather Delay, in Minutes<br/>
NAS_DELAY - National Air System Delay, in Minutes<br/>
SECURITY_DELAY - Security Delay, in Minutes<br/>
LATE_AIRCRAFT_DELAY - Late Aircraft Delay, in Minutes<br/>

## Summary of Findings

**Origin and Destination**
All origin state positions are equal to destination state positions.
State of California are the most common origin and destination while Trust Territory of the Pacific Islands is the less common.

**Top 10 most common flight stretches**
Stretch California to California is the most common
Florida state is in 5 of the 10 most common stretches, while it is only the third for flights of origin and destination.

**Delays**
A small portion of the flights are concentrated in more than 8 hours of delay, with most reasons being the delay of the aircraft.

**Air time**
The majority of flights are quickly, approximately 1 hour and 30 minutes.
Strong relationship between Air time and Distance, that means how much high distance, air time is higher too.
Hawaiian Airlines is the last one in relation to the total number of flights made, but in terms of air time, it is in fifth place and has the longest air time registered in relation to the others.

**Distance**
Flight distances are mostly up to 1,000 miles.

**Carrier names** (will be used in the presentation)
Southwest Airlines Co is the most common carrier, while Hawaiian Airlines Inc is the less common.

**Cancelled flights** (will be used in the presentation)
The reason most common is "Security" while "National Air System is the less common.
In four first months of 2020 year, the total of cancelled flights has already exceeded eight months of 2019 year.
The spike in cancellation for "Security" and "Carrier" reasons starting at almost the same time (Feb 2020), two days after a declaration of outbreak of COVID-19 to be a Public Health Emergency of International Concern (On 30 January 2020)

**Days of Week** (will be used in the presentation)
Most flights are in friday while on saturday it has less demands.

## Key Insights for Presentation

**Days of Week**
The y-axis was formatted to represent the millions as the letter M ,percentages were placed for each bar representing each day of week and the number of the day of the week has been transformed into names of the days of the week.

**Carrier names**
The x-axis was formatted to represent the millions as the letter M and percentages were placed for each bar representing each carrier.

**Cancelled flights**
The x-axis was formatted in month / year and each line represents a reason for cancellation.
A log scale was also applied to improve the layout of the lines