---
title: "Introduction & Background"
date: 2021-12-20
categories:
  - blog
tags:
  - Github Page
  - update
excerpt: "Inspiration of the project."
---

![NJ_Transit_Amtrak](https://raw.githubusercontent.com/penelope0318/Amtrak_Train_Delay/master/assets/images/us_njtransit_nec.jpeg)




## Inspiration
NJ Transit is the third-largest statewide public transportation system in the United States, operating bus, light rail, and commuter rail across New Jersey. It also has the nation's second-largest commuter rail network which has 1,231 trains, 166 rail stations and serves over 300,000 customers every day. The rail network connects the state's main business and employment centers and also helps to link the state to adjacent cities like Philadelphia and New York City 
<a href="https://www.njtransit.com/press-releases/nj-transit-named-one-years-americas-best-employers-forbes">(NJ Transit, 2021)</a>.

Despite having been improved in recent years, NJ transit rail services have long been plagued by chronic delay issues. For example, in 2018 November and December, only **35%** of the rail trips arrived within 2 minutes of the scheduled arrival time, while almost 10% of the trips delayed for more than 10 minutes, accounting for 44,470 trips, and even nearly 2,000 trips delayed from more than an hour! Such kind of large-scope train delay also potentially impact the surrounding bus services.


In order to provide better and punctual services and thus avoid potential financial and reputational harm, we believe it is vital for NJ transit operators to conduct regular delay analysis to investigate when and where did the delay typically occurs, and then develop targeted strategies to alleviate the frequency and severity of delays. Apart from the physical maintenance, if the riders or the train operators can be alerted in advance of the possible delays, they can get additional time to arrange their journey plan and the network system accordingly, thereby preventing further escalation.


![NJ_Transit_Amtrak](https://raw.githubusercontent.com/penelope0318/Amtrak_Train_Delay/master/assets/images/penn-station-delays.jpeg)
Delay in NYC Penn Station on Feb.3, 2020 <a href="https://pix11.com/news/local-news/manhattan/nearly-3-hour-delays-massive-crowds-continue-at-penn-station/">(Smith, 2020)</a>
 

## Main Dataset
There is an origin-destination train delay and cancelation data for NJ transit and Amtrak on <a href="https://www.kaggle.com/pranavbadami/nj-transit-amtrak-nec-performance?select=2018_11.csv">Kaggle</a>. We used 2018 November and December delay data to analyze the pattern of delay and then built a machine learning model to predict the future delay. 



## Content
The project will be seperated into following 2 sections:
- **Exploratory analysis**: <a href="https://penelope0318.github.io/NJ_Transit_Train_Delay/3when_delay/">when</a>, <a href="https://penelope0318.github.io/NJ_Transit_Train_Delay/2where_delay/">where</a>  did the delay usually happen? 


- **Modeling**:  <a href="https://penelope0318.github.io/NJ_Transit_Train_Delay/1model/">Methods</a> involving feature engineering, model selection, cross-validation. 

  

