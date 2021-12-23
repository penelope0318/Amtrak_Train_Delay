---
title: "Exploratory Analysis - When delay"
date: 2021-12-20
published: true
tags: [dataviz, altair, folium]
excerpt: "Exploratory Analysis of the data."
altair-loader:
  altair-chart-1: "charts/station_time_heatmap.json"
  altair-chart-2: "charts/weekday_time_alt.json"
  altair-chart-3: "charts/station_lag_alt.json"
  altair-chart-4: "charts/station_time_heatmap1.json"
hv-loader:
  hv-chart-1: "charts/hv_table.html"
toc: true
toc_sticky: true
---
![NJ_Transit_Amtrak](https://raw.githubusercontent.com/penelope0318/Amtrak_Train_Delay/master/assets/images/us_njtransit_nec.jpeg)

## 0. Data Preparation

Here is a glimpse of the original dataset from <a href="https://www.kaggle.com/pranavbadami/nj-transit-amtrak-nec-performance?select=2018_11.csv">Kaggle</a>. We selected the data in 11/2019 and 12/2019, totaling 682,163 rows. To clean the data, we dropped any rows with NA values in the `scheduled_time`, `delay_minutes`, `from_id`, `to_id` columns. Additionally, in order to focus on the issue of punctuality , we decided to drop any records labelled as `cancelation`, as this is distinct from the issue of delay in some extent. The final cleaned dataset has 436,100 records in total. To gain a geographical perspective on the delay, the dataset was combined with the stations' location data from <a href="https://github.com/pranavbadami/njtransit">Pranav Badami</a>. 
<div id="hv-chart-1"></div>


## 1. Statistic Summary 

These histograms illustrate the substantially left-skewed distribution of train delays in NJ transit's commute rail services in 2019 November and December. The bulk of the delay (97% ）events was spaned from **0 min to 20 min**, however, there is an extremely long tail in the data, which reveals that approximately 50 travels (0.016%) are suffering from more than 100 minutes delay.
![delay_distribution](https://raw.githubusercontent.com/penelope0318/Amtrak_Train_Delay/master/assets/images/delay_distribution.png)


As delays can happen for a variety of reasons, the following parts will focus on the analysis about when and where did the delay typically happen.




## 2. Analysis Delay by Time

It's known that delay is highly related to date and time, rider's travel behavior and train schedule varied according to weekday, time of the day and holidays. The following diagram plots the train volume by `scheduled arrive time` (the bars), as well as the average delay minutes by `scheduled arrive time` and `the departure weekday` (the series lines). 

It demonstrates that NJ transit rail services's rush hours are mostly around 6am-10am and 3pm-8pm. The series lines indicate that the heavy delay usually happened around 6pm-7:30pm of the day, and considering the train volume, the most severe dealy occurs on **Saturday 8pm-9pm** where trains were delayed for an average of 8 minutes. 
<div id="altair-chart-2"></div>
<br> 


However, NJ Transit operates 166 stations in total <a href="https://www.njtransit.com/press-releases/nj-transit-named-one-years-americas-best-employers-forbes">(NJ Transit, 2021)</a>., did the train usually delay in the same pattern for all stations? The answer is no. The subsequent section will analyze the delay by station.


## 3. Analysis Delay by Weather
Weather is another type of feature that would impact train punctuality by affecting the operation of the rail infrastructure, especially the extreme weather, for example, high winds, ice and snow, etc, <a href="https://public.wmo.int/en/bulletin/weather-and-climate-change-implications-surface-transportation-usa">(McGuirk, 2009)</a>. However, many weather data are not free, let alone the fact that   we need to get more than 400,000 weather data in 2019 by longitude, latitude and date one-time via API. Therefore, we decide to use the free weather station data from <a href="https://www.ncdc.noaa.gov/cdo-web/search?datasetid=GHCND"> National Centers for Environmental Information</a>, which has a variety of historical daily weather conditions.

Another issue of this weather data is that about 15% of records are NA, in order to guarantee the model have enough records, we fill the uncommon weather feature like `fog` and `precipitation` as 0, and fill normal weather condition like `temperature` and `wind` as mean. 

The following series of plots try to visualize the relationship between weather and the percentage of delay greater than 5mins; it indicates that when `fog`, `ice pellets`, `haze` and large `precipitation` occur, the percentage of delay greater than 5mins is higher than under regular weather conditions. 


![weather_bar](https://raw.githubusercontent.com/penelope0318/Amtrak_Train_Delay/master/assets/images/weather_bar.png)

![weather_line](https://raw.githubusercontent.com/penelope0318/Amtrak_Train_Delay/master/assets/images/weather_line.png)







