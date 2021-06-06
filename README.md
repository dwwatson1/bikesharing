# NYC Citi Bike Tableau Analysis 

## Overview of the Analysis

The purpose of this analysis is convince investors that a bike-sharing program in Des Moines is a solid business proposition. Using August 2019 data from New York City's Citi Bike-Sharing Program as our case study, we will visualize user types and bike activity with Tableau to understand a future program in Iowa's largest city.

### Analysis Resources
* Data Sources: [NYC Citi Bike Visualization of August 2019 Activity](https://public.tableau.com/app/profile/david.watson5975/viz/NYCCitiBikeChallengeVisualization/NYCCitiBikeVisualizationofAugust2019Activity), citibike_data.csv (too large to add) 
* Software: Jupyter Notebook 6.1.4, Tableau Public 2021.1
* Notebooks: [NYC Citi Bike Challenge](https://github.com/dwwatson1/bikesharing/blob/main/NYC_Citibike_Challenge.ipynb)
 
## Results of the Analysis

Before beginning the analysis, we needed to convert trip duration from an integer to a datetime, so we could more effectively display a critical metric for a bikesharing program. Using pandas in Jupyter Notebook, we successfully changed the data type, so we could complete the analysis.

![pandas.PNG](https://github.com/dwwatson1/bikesharing/blob/main/images/pandas.PNG)

Next, we used that converted trip duration metric to display checkout times for users. As shown in the graph, the majority of users complete their Citi Bike trips in under an hour. In fact, the most popular checkout time is 5 minutes. New Yorkers prefer quick bike trips to get to where they're going.

<img src="https://github.com/dwwatson1/bikesharing/blob/main/images/checkout_times_for_users.PNG" width="800" >

We then took the same analysis as above but added our converted gender dimension to display Male, Female, or unknown. Males overwhelmingly take Citi Bike trips compared to females or unknown genders. 

<img src="https://github.com/dwwatson1/bikesharing/blob/main/images/checkout_times_by_gender.PNG" width="800" >

We know that users are more often than not males who take trips in under an hour. Now, let's see when users are taking those rides during each day of the week. As we can see in the heatmap below, peak riding times are during the morning commute hours of 6 - 9 a.m. and 5 - 8 p.m. on weekdays. Weekends have lighter (shown in lighter orange in the heatmap) activity overall but have consistent usage during the daytime hours of 10 a.m. - 6 p.m.

![trips_by_weekday_per_hour.PNG](https://github.com/dwwatson1/bikesharing/blob/main/images/trips_by_weekday_per_hour.PNG)



### Overview of Results 

