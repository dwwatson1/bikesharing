# NYC Citi Bike Tableau Analysis 

## Overview of the Analysis

The purpose of this analysis is convince investors that a bike-sharing program in Des Moines is a solid business proposition. Using August 2019 data from New York City's Citi Bike-Sharing Program as our case study, we will visualize user types and bike activity with Tableau to understand a future program in Iowa's largest city.

### Analysis Resources
* Tableau Dashboard: [link to dashboard](https://public.tableau.com/app/profile/david.watson5975/viz/NYCCitiBikeChallengeVisualization/NYCCitiBikeVisualizationofAugust2019Activity)
* Data Sources: citibike_data.csv (too large to add) 
* Software: Jupyter Notebook 6.1.4, Tableau Public 2021.1
* Notebooks: [NYC Citi Bike Challenge](https://github.com/dwwatson1/bikesharing/blob/main/NYC_Citibike_Challenge.ipynb)
 
## Results of the Analysis

### Converting Trip Duration Metrics in Pandas
Before beginning the analysis, we needed to convert trip duration from an integer to a datetime, so we could more effectively display a critical metric for a bikesharing program. Using pandas in Jupyter Notebook, we successfully changed the data type, so we could complete the analysis.

![pandas.PNG](https://github.com/dwwatson1/bikesharing/blob/main/images/pandas.PNG)

### Checkout Times for Users
Next, we used that converted trip duration metric to display checkout times for users. As shown in the graph, the majority of users complete their Citi Bike trips in under an hour. In fact, the most popular checkout time is 5 minutes. New Yorkers prefer quick bike trips to get to where they're going.

<img src="https://github.com/dwwatson1/bikesharing/blob/main/images/checkout_times_for_users.PNG" width="800" >

### Checkout Times by Gender
We then took the same analysis as above but added our converted gender dimension to display male, female, or unknown. Males overwhelmingly take Citi Bike trips compared to females or unknown genders. 

<img src="https://github.com/dwwatson1/bikesharing/blob/main/images/checkout_times_by_gender.PNG" width="800" >

### Trips by Weekday per Hour
We know that users are more often than not males who take trips in under an hour. Now, let's see when users are taking those rides during each day of the week. As we can see in the heatmap below, peak riding times are during the morning commute hours of 6 - 9 a.m. and 5 - 8 p.m. on weekdays. Weekends have lighter (shown in lighter orange in the heatmap) activity overall but have consistent usage during the daytime hours of 10 a.m. - 6 p.m.

<img src="https://github.com/dwwatson1/bikesharing/blob/main/images/trips_by_weekday_per_hour.PNG" width="800" >

### Trips by Gender (Weekday per Hour)
Again, we took the same trips by weekday per hour analysis and added the gender dimension to show the peak riding hours of the day by male, female, and unknown. Trips by males and females followed a similar pattern to the heatmap above where 6 - 9 a.m. and 5 - 8 p.m. on weekdays saw the highest volume and 10 a.m. - 6 p.m on the weekends. The only difference between male and female was that trips by amles were much more numerous than trips by females, as denoated by the shading gradient on the heatmap. Unkown gender trips didn't follow the weekday commute pattern as did trips by male and females, however, trips by unknown gender were highest from 10 a.m. - 6 p.m on weekends. Perhaps  unknown riders are tourists who sign up quickly when sightseeing. 

<img src="https://github.com/dwwatson1/bikesharing/blob/main/images/trips_by_gender.PNG" width="800" >

### User Trips by Gender by Weekday 
Let's investigate this assumption that trips by unknown gender riders are likely tourists. By splitting the types of Citi Bike users by customer and subscriber, we can see that the most subscribers are recording their gender when they sign up. Very few subscribers are unknown gender. Trips by customers are fairly uniform in terms of the heatmap shading, but the darkest portion is on Saturday and Sunday for trips by unknown gender users. The darkest shading for trips by male and female subscribers is on Thursday, which leads us to believe that subscribers are more likely to be commuters who don't leave the gender column blank, assuming unknown means leaving it blank.

<img src="https://github.com/dwwatson1/bikesharing/blob/main/images/user_trips_by_gender.PNG" width="800" >

### Top Starting Locations by Gender

We wanted to then find out where the top starting locations for each gender. The most popular starting trip locations are noted with darker shading and a bigger circle. The most popular starting trips for males was near Grand Central Station (biggest circle shaded in dark red). This data tells us that Citi Bike trips are likely popular among male commuters, especially ones who commute by train from NY and CT. The most popular starting location for females is a ferry terminal near the Lincoln Tunnel and near Pier 26 in Tribeca, which tells us that Citi Bike trips are also likely popular among female ferry commuters and city dwellers around Tribeca. Finally popular starting locations among unknown gender riders are scattered along the border of Central Park, which tells us that those riders are likely tourists. 

<img src="https://github.com/dwwatson1/bikesharing/blob/main/images/top_starting_locations_by_gender.PNG" width="800" >

### Top Stopping Locations by Gender

The top ending locations were almost identical to top starting locations. For males, Grand Central Station was the most popular ending station, which again, builds our case for riders that tend to be commuters. The same was the case for female riders, where some of the most popular locations were along the West Side of Manhattan (Tribeca and Lincoln Tunnel ferry terminal).

<img src="https://github.com/dwwatson1/bikesharing/blob/main/images/top_ending_locations_by_gender.PNG" width="800" >

## Analysis Summary

### Summary of Results 

As described in the section prior, Citi Bike trips were most likely to be short and completed by males. Peak ridership occured on weekdays, when commuters are most active, and around commuting hubs like major train stations (Grand Central Terminal) and ferry terminals along the West Side of Manhattan. An overwhelming majority of the trips completed were done in Manhattan, where it can be convenient to get around the borough by bike as it's a dense city, where traffic congestion can be a major problem. 

New York is a very different city than Des Moines in terms of geography and density, but from this analysis, we can understand that Citi Bikes see their heaviest usage in the densest parts of Manhattan. Des Moines could start their bikesharing program in the city center first and consider fanning out to the city limits.  

### Additional Analyses

To further this analysis, it would be helpful to create a list of the most popular starting and stopping locations. This would complement the most popular starting and stopping graphs in terms of placing landmarks on coordinates. This will be helpful to figure out where are the most popular starting and stopping locations in Des Moines in terms of their own landmarks. In addition to putting names on the most popular locations, it would be helpful to know what time of day and day of the week are the most popular at those locations. This will help maintenance crews figure out when to service bikes, especially at the heavily used Grand Central Terminal.

I would also investigate the way people sign up for Citi Bike rides for customers and subscribers. Is the sign up form as streamlined as possible or is something preventing users from selecting the gender of their choice? 
