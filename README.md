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

![Checkout Times](https://github.com/doliver231/bikesharing/blob/main/Images/Checkout_Times.png)



![Checkout Times Gender](https://github.com/doliver231/bikesharing/blob/main/Images/Checkout_Times_Gender.png)



![Top Starting Locations](https://github.com/doliver231/bikesharing/blob/main/Images/Top_Starting_Locations.png)



![Trips by Weekday Hour](https://github.com/doliver231/bikesharing/blob/main/Images/Trips_by_Weekday_Hour.png)



![Trips by Gender](https://github.com/doliver231/bikesharing/blob/main/Images/Trips_by_Gender.png)



![Usertype Trips Gender Weekday](https://github.com/doliver231/bikesharing/blob/main/Images/Usertype_Trips_Gender_Weekday.png)



![Average Trip Duration BirthYear](https://github.com/doliver231/bikesharing/blob/main/Images/Average_Trip_Duration_BirthYear.png)

There were over 2.3 million rides for the month of August 2019.
81% of the users were subscribers. 65% of the users were confirmed males and 25% were confirmed females.
There is a wide range of the age of the users. Younger users tend to use the service for longer rides.
Top ride starting locations are in the most touristic and busy areas, as we see here in Manhattan.
Highest activity hours are from 5:00 PM to 7:00 PM and require the most resources mobilized.
The activity from 2:00 AM to 5:00 AM is low so this would be the window for bike maintenance.
Bikes are mostly checked out for 4 to 6 hours.
Male users take approximately 3 times more rides than the female users.
Most weekday rides are around 7:00 AM to 9 AM and 5:00 PM to 7:00 PM.
Weekend rides are highest from 10:00 AM to 7:00 PM.
Those rides are mostly taken by male users.

## Conclusion

The data shows high activity of the bike sharing service in New York during the month of August 2019.
The far majority of the rides were in the very busy Manhattan Island, taken by male users during morning and evening rush hours. This implies that Citi Bike services are used as an alternative to public transportation by commuting workers.
Additional analysis would be beneficial by :

comparing data for different months to determine trends across the year,
including weather data to find the correlation between the weather and the rides.

Based upon the visualizations above, we can see that the vast majority of usage comes from Subscribers that are Male using bikes during weekday commutes in the morning and evening.

Additional visualizations could include showing which Stations correspond to the most amount of bike rentals. Also a visualization showing the age of the average customer compared to how long they rent a bike could be helpful.

The following link is for the prepared Tableau Story, which includes the above visualizations as interactive.