---
title: "Introduction & Background"
date: 2021-12-20
categories:
  - blog
tags:
  - Github Page
  - update
---

![NJ_Transit_Amtrak](https://raw.githubusercontent.com/penelope0318/Amtrak_Train_Delay/master/assets/images/us_njtransit_nec.jpeg)




## Inspiration
NJ Transit is the largest statewide public transportation system in the United States, operating bus, light rail, and commuter rail across New Jersey. Its nation's second-largest commuter rail network has 162 rail stations and serves over 300,000 customers every day. The rail network connects the state's main business and employment centers and also helps to link the state to adjacent cities like Philadelphia and New York City. 

Despite having been improved in recent years, NJ transit rail services have long been plagued by chronic delay issues. For example, in 2018 November and December, only 35% of the rail trips arrived within 2 minutes of the scheduled arrival time, while almost 10% of the trips were delayed more than 10 minutes, accounting for 44,470 trips, and even almost 2,000 trips delayed from more than an hour! Such kind of large-scope train delay also potentially impact the surrounding bus services.

In order to provide better and punctual services and thus avoid potential financial and reputational harm, we believe it is vital for NJ transit operators to conduct regular delay analysis to investigate when and where did the delay typically occurs, and then develop targeted strategies to alleviate the frequency and severity of delays.


![NJ_Transit_Amtrak](https://raw.githubusercontent.com/penelope0318/Amtrak_Train_Delay/master/assets/images/penn-station-delays.jpeg)
Delay in NYC Penn Station on Feb.3, 2020 <a href="https://pix11.com/news/local-news/manhattan/nearly-3-hour-delays-massive-crowds-continue-at-penn-station/">(Smith, 2020)</a>
 

## Delay Dataset
There is an original-destination train delay and cancelation data for NJ transit and Amtrak on <a href="https://www.kaggle.com/pranavbadami/nj-transit-amtrak-nec-performance?select=2018_11.csv">Kaggle</a>. This project intends to use 2018 November and December data to analysis the pattern of delay and then build a machine leaning model to predict future delay. 



- why we want analysis and predict
  - current problems (when & where & why)
  - benefit for riders (services quality) and transportation planner (profit)
- Data source (show original data)
  - use 2019/11 and 2019/12 data to do the analysis and modleing 

## Content
The project will be seperated into following 2 sections:
- Exploratory analysis: when, where, which (stops & lines) did the delay happen? 
- Modeling: feature engineering, model selection, cross-validation. 

  

