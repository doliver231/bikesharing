# Citibike Bikesharing

## Objective

The purpose of this project is to show investors how the bikesharing model in NYC can be as successful if implemented in Des Moines, Iowa. Different factors that are being analyzed are:

* The length of time that bikes are checked out for all riders and genders
* The number of bike trips for all riders and genders for each hour of each day of the week
* The number of bike trips for each type of user and gender for each day of the week.

## Resources

* Data Source: [Citibike Data - August 2019](https://github.com/doliver231/bikesharing/blob/main/201908-citibike-tripdata.zip)
* Software/Languages: Python (Pandas), Jupyter Notebook, Tableau Public (Desktop) 2022.4.0

## Results

[Link to my Tableau Public - Story](https://public.tableau.com/views/Citi_Bike_Challenge_16741521703210/BIKESHARING?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link)

Before using Tableau to create any visualizations, we needed to convert our "Trip Duration" data to a `datetime` datatype on [Jupyter Notebook](https://github.com/doliver231/bikesharing/blob/main/NYC_CitiBike_Challenge.ipynb) using Pandas:

```py
import pandas as pd
citi_df['tripduration_datetime2'] = pd.to_datetime(citi_df['tripduration'], unit='s')
```

on Tableau, we were able to create the following visualizations with our [Citibike Data](https://github.com/doliver231/bikesharing/blob/main/201908-citibike-tripdata.zip):

![Top Starting Locations](https://github.com/doliver231/bikesharing/blob/main/Images/Top_Starting_Locations.png)

There were over 2.3 million rides for the month of August 2019. Top ride starting locations are in the most touristic and busy areas, as we see here in Manhattan.

![Checkout Times](https://github.com/doliver231/bikesharing/blob/main/Images/Checkout_Times.png)
![Checkout Times Gender](https://github.com/doliver231/bikesharing/blob/main/Images/Checkout_Times_Gender1.png)

Male users take approximately 3 times more time checking out bikes than the female users.

![Trips by Weekday Hour](https://github.com/doliver231/bikesharing/blob/main/Images/Trips_by_Weekday_Hour.png)
![Trips by Gender](https://github.com/doliver231/bikesharing/blob/main/Images/Trips_by_Gender.png)

Highest activity hours are from 7AM-9AM & 5PM-7PM on weekdays. The lowest activity are from 2AM-5AM is low, which would be the  best window for bike maintenance. Weekend ride activity are highest from 10AM-7PM, a much wider range than for weekdays.

![Usertype Trips Gender Weekday](https://github.com/doliver231/bikesharing/blob/main/Images/Usertype_Trips_Gender_Weekday.png)
![Usertype Percentages](https://github.com/doliver231/bikesharing/blob/main/Images/Usertype_percentages.png)

81% of the users were subscribers. 65% of the users were confirmed males and 25% were confirmed females.

![Average Trip Duration BirthYear](https://github.com/doliver231/bikesharing/blob/main/Images/Average_Trip_Duration_BirthYear.png)

There is a wide range of user ages; Younger users tend to use the service for longer rides.

## Conclusion

The majority of the rides were taken place on the main island of Manhattan, taken primarily by male users during morning and evening rush hours. This implies this bike service is being used as one of the major transportation modes in the city, just alongside the other means such as train, subway, and taxi. The vast majority of the usage are specifically subscribers, who are depending on this as a consistent transportation method. 

The data set showed a good amount of details specifically for August 2019. It would be beneficial to obtain visualizations of datasets for every month of the year, to get a good understanding of how successful this service is throughout the year. It would also be useful to obtain data from a city with a similar population as Des Moines that also use bike sharing services, to get a better comparison of data. I'm sure bike riding depends greatly on the current weather at the time, so comparing these factors can really give us an idea how well the service will perform in Des Moines, which has its own weather trends throughout the year.