



# London Bike Sharing

We are analyzing London Bike Sharing data to try predict the future bike shares, pinpoint the factors influencing new bike shares the most, analyze the bike share trends of seasons, temperatures and months of the year. Improving and optimizing strategies for promoting New Bike Sharing is the main goal. This project's dataset comes from 3 sources:

Https://cycling.data.tfl.gov.uk/ 'Contains OS data © Crown copyright and database rights 2016' and Geomni UK Map data © and database rights [2019] 'Powered by TfL Open Data'
freemeteo.com - weather data
https://www.gov.uk/bank-holidays
From 1/1/2015 to 31/12/2016 
Dataset Link: https://www.kaggle.com/datasets/hmavrodiev/london-bike-sharing-dataset


# Cycling Trends: The Effect of Weather, Holidays, and Weekdays -Dashboard

### Dashboard Links : https://public.tableau.com/app/profile/shruti.ghatay/viz/CyclingTrendsTheEffectofWeatherHolidaysandWeekdays_/CyclingTrendsTheEffectofWeatherHolidaysandWeekdays#1

### https://public.tableau.com/app/profile/shruti.ghatay/viz/WeatherandSeasonalImpactsonBikeSharinginLondon/WeatherandSeasonalImpactsonBikeSharing
 

### Data Cleaning 
1. Changed the Boolean field 'is holiday' values from 1 - holiday / 0 - non holiday to Yes - holiday / No - non holiday.
2. Changed the Boolean field  'is weekend' from 1 - weekend / 0 - Weekday to Yes - weekend / No - Weekday.
3. Changed season field from 0; 1; 2; 3 to spring, summer, fall, winter.


## Problem Statement

This dashboards help TFL UK understand their consumers better. It helps the transport system know during which time of the year or under what weather conditions do the commuters prefer using bikes to commute. Through different bike sharing trends, they get to know the commuters' preference, & thus they can improve their services by providing commuters with assistance in using bikes suring certain seasons or weather conditions. It also lets them know the average bike shares during holidays vs. non-Holidays, Weekdays vs. Weekends, and Two-Week Moving Average thus, since by using this dashboard they have identified this problem, they can further work on factors responsible for these unwanted delays.

Since, the average number of New Bike shares is higher during Weekdays and Non-Holidays, we can draw the following conclusion that commuters who prefer to commute using bikes are mostly working class or students. 

### Steps followed for Dashboard creation:
- Step 1 : Load data into Tableau Desktop, dataset is a CSV file.
- Step 2 : It was observed that in none of the columns errors & empty values were present.
- Step 3 : In the Format view, under the shading tab, workbook background was selected.

## Dashboard 1 - Cycling Trends: The Effect of Weather, Holidays, and Weekdays.
### Steps followed:

### Chart - Average Bike share trend during weekdays vs. weekends

- Step 1: Dragged 'Is Weekend' field to columns.
- Step 2: Dragged 'Count of New Bike Shares' field to rows. Changed the Measure to 'Average'. 
- Step 3: By Default Tableau selected 'Bar' as the chart type. Since the chart type is accurate, no changes were made.
- Step 4: Dragged 'Is Weekend' field to color and selected the color of choice.
- Step 5: Dragged 'Count of New Bike Shares' field to Label and changed the Measure to 'Average'.
- Step 6: Gave the chart a suitable title. 

### Chart - Average Bike share trend during Holidays vs. Non-Holidays

- Step 1: Dragged 'Is Holiday' field to columns.
- Step 2: Dragged 'Count of New Bike Shares' field to rows. Changed the Measure to 'Average'. 
- Step 3: By Default Tableau selected 'Bar' as the chart type. Since the chart type is accurate, no changes were made.
- Step 4: Dragged 'Is Holiday' field to color and selected the color of choice.
- Step 5: Dragged 'Count of New Bike Shares' field to Label and changed the Measure to 'Average'.
- Step 6: Gave the chart a suitable title.

### Chart - Influence of weather code on Bike shares

- Step 1: Dragged 'Weather code' field to columns.
- Step 2: Dragged 'Count of New Bike Shares' field to rows.
- Step 3: By default Tableau selected the chart type as 'Bar'. Chnaged the chart type to Pie to better annotate the contents of the chart.
- Step 4: Increased the size of the chart using ctrl + shift+ B command.
- Step 5: Created annotations for the various segments of the Pie chart according to the following category description:
1 = Clear ; mostly clear but have some values with haze/fog/patches of fog/ fog in vicinity 2 = scattered clouds / few clouds 3 = Broken clouds 4 = Cloudy 7 = Rain/ light Rain shower/ Light rain 10 = rain with thunderstorm 26 = snowfall 94 = Freezing Fog.


## Dashboard 2 - Weather and Seasonal Impacts on Bike Sharing

### Chart - 2-Week Moving Average of Bike shares

- Step 1: Dragged the continous week of the 'Timestamp' field to columns by right clicking on 'Timestamp' field and selecting the continous week from the 'Drop field' window.
- Step 2: Dragged 'Count of New Bike Shares' field to rows.
- Step 3: Add table calculation by right-clicking the 'Count of New Bike Shares' field in rows. Set calculation type to Moving calculation and Average where the previous value = 2 and next value = 1. Meaning it will take into account the previous two values (weeks) and 1 week in the future including the current week.
- Step 4: Saved the moving average calculation created to the workbook [Saved as - Window_AVG(Sum(Count of New Bike Shares) -2,1)] and created two parameters - Week Before Date and Week After Date.
- Step 5: For the Week before Date Parameter, the data type was changed to Integer and the Allowable value to 'Range' (Min - 0, Max - 52, step size - 1).
- Step 6: Followed the same steps for the Weeks After Date parameter.
- Step 7: Changed the 'Moving Average' formula by replacing '-2' with Week before Date Parameter and '1' with Week After Date Parameter to decrease the rigidity and make room for customization.
- Step 8: Right clicked on the parameters and selected 'show parameter' to display the parameters on the chart to customize the number of weeks to be taken into consideration for the moving average calculation.
- Step 9: Dragged Count of New Bike Shares' field to rows and selected dual-axis by right-clicking the 'Count of New Bike Shares' field in rows for comparision.
- Step 10: Synchronized the right axis and hid it from the chart for a better visual.
- Step 11: Dragged Month(Timestamp) to filters to customize the months to be taken into consideration for moving average calculation.

Snap of new parameters created ,

![parameters ss](https://github.com/Sghatay99/London-Bike-Sharing-Tableau-Project/assets/161419911/29fff2f1-04be-4346-ae08-065d9654155d)

Snap of parameters as shown on chart ,

![parameters as shown on chart](https://github.com/Sghatay99/London-Bike-Sharing-Tableau-Project/assets/161419911/d28f444d-dbd2-4347-85d0-5deb195aeede)


### Chart - 3 - Average count of Bike Shares by Season

- Step 1: Dragged Season to columns.
- Step 2: Dragged 'count of new bike shares' to Rows. Changed the measure to Average.
- Step 3: Dragged Season to color and selected color of choice.
- Step 4: Dragged Average of count of new bike shares' to Label.

### Chart - 4 - Bike shares during Maximum Temperatures

- Step 1: Dragged the continous Month of the 'Timestamp' field to columns by right clicking on 'Timestamp' field and selecting the continous Month from the 'Drop field' window. 
- Step 2: Dragged 'count of new bike shares' to Rows.
- Step 3: Dragged 'Temp in C' field to filters. Selected 'Maximum' from filter field pop-up window, clicked on next.
- Step 4: Set the maximum range values to 10 - 34. Right clicked on filters field and selected 'show filter' to make the chart interactive.
- Step 5: Dragged Max of 'Temp in C' to color and selecte the color of choice.

Snap of Maximum Temperature filter created 

![Max temp filter on chart](https://github.com/Sghatay99/London-Bike-Sharing-Tableau-Project/assets/161419911/7735160f-5dfb-4d42-97ba-f8345b45de6a)

### Chart - 5 - Bike shares during Minimum Temperatures

- Step 1: Dragged the continous Month of the 'Timestamp' field to columns by right clicking on 'Timestamp' field and selecting the continous Month from the 'Drop field' window. 
- Step 2: Dragged 'count of new bike shares' to Rows.
- Step 3: Dragged 'Temp in C' field to filters. Selected 'Minimum' from filter field pop-up window, clicked on next.
- Step 4: Set the minimum range values to -1.50 - 12.50. Right clicked on filters field and selected 'show filter' to make the chart interactive.
- Step 5: Dragged Max of 'Temp in C' to color and selecte the color of choice.

Snap of Minimum Temperature filter created  

![Min temp filter on chart](https://github.com/Sghatay99/London-Bike-Sharing-Tableau-Project/assets/161419911/ce5b71c9-3fb6-49fe-b5b3-a4c4e13534de)

 
 # Report Snapshot (TABLEAU DESKTOP)

 
![Dashboard 1](https://github.com/Sghatay99/London-Bike-Sharing-Tableau-Project/assets/161419911/02bd0d52-a8f0-456e-8132-c527c3ee0fda)



![Dashboard 2](https://github.com/Sghatay99/London-Bike-Sharing-Tableau-Project/assets/161419911/726ba2b5-a838-42fa-a212-a08120b243ca)

# Insights

Two Dashboards were created on Tableau Desktop & it was then published to Tableau Public Server.

Following inferences can be drawn from dashboard - 1;

### [1] The Average number of new Bike Shares during Weekdays and Weekends

   Average Number of new Bike shares for value 'is weekend' = 'no' (Weekday) = 1209.3 

  Average Number of new Bike shares for value 'is weekend' = 'yes' (Weekend) = 977.4


           Thus, higher number of average new bike shares during Weekdays.
           
### [2] The Average number of new Bike Shares during Holidays and Non-Holidays

 Average Number of new Bike shares for value 'is Holiday' = 'no' (Non-Holiday) = 1151.5

  Average Number of new Bike shares for value 'is Holiday' = 'yes' (Holiday) = 769.5


          Thus, higher number of average new bike shares during Non-Holidays.
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  
  ### [3] Weather code Influence 
  
      a) Count of new bike shares in weather code 1 (Clear sky) - 7,146,847 (35.90%)
      b) Count of new bike shares in weather code 2 (Scattered/few clouds) - 6,035,580 (30.32%)
      c) Count of new bike shares in weather code 3 (Broken clouds) - 4,243,887 (21.32%)
      d) Count of new bike shares in weather code 4 (Cloudy) - 929,978 (4.67%)
      e) Count of new bike shares in weather code 7 (Light rain) - 1,526,461 (7.67%)
      f) Count of new bike shares in weather code 10 (Rain with Thrunderstorm) - 8,168 (0.04%)
      g) Count of new bike shares in weather code 26 (Snowfall) - 15,051 (0.08%)

      The above numbers indicate that commuters prefer commuting through bikes when the weather is clear (for obvious reasons).


Following inferences can be drawn from dashboard - 2;

 ### [4] Moving Average of Bike shares

When only the months October, November and December were taken into consideration, the moving average was pretty much the same when the weeks before date was set to a higher number. Meaning, higher the number of prior weeks taken into consideration, the flatter the line chart.


 ### [5] Bike shares by Season

        a) Average count of new bike shares during Fall = 1179.0
        b) Average count of new bike shares during Spring = 1103.8
        c) Average count of new bike shares during Summer = 1464.5
        d) Average count of new bike shares during Winter = 821.7
 
         Thus, maximum number of new bike shares were during Summer.
         Average delay will change if different visual filters will be applied.
 
 ### [6] Bike shares during Maximum Temperatures
 
Most new Bike shares happened during the months with highest maximum temperatures, June - August every year, indicating that Summer (max temp 29 - 34) is the most prefered season and winter is the least preferred season for bike share.
 
         Count of New bike shares will change if different visual filters will be applied.
         
### [7] Bike shares during Minimum Temperatures

Most new Bike shares happened during the months with highest minimum temperatures, June - August every year, indicating that Summer (min temp 9 - 13) is the most prefered season for bike share.

        Count of New bike shares will change if different visual filters will be applied.




