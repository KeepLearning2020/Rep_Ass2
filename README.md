# Storm Data Analysis
This repository is for Coursera, Reproducible Research: Peer Assessment 2, about U.S. Storm Data Analysis

## Introduction to the Project

The purpose of this project is to find out answers to two questions about the impact of severe weather events in the United States based on the data set from the U.S. National Oceanic and Atmospheric Administration's (NOAA) storm Database.

1. which types of events (EVTYPE) are most harmful with respect to population health
2. which types of events have the greatest economic consequences

The dataset is provided by Cousera weblink, it can be downloaded via the website.

## Files in the repository

There are three files in this repo: 

- The README.md gives the brief introduction about the implementation.

- The Rmd script StormDataAnalysis.Rmd is created for data cleaning and analysis.

- The StormDataAnalysis.html is the output result from previous Rmd file. It is also published under Rpubs as https://rpubs.com/KeepLearning/644090.

- The figure StormDataAnalysis.png records the top event types with biggest impact to population health and economy consequences separately.

## Details in Rmd script

The data from 2000 to 2011 are used for analysis in the project. The harm to population health is measured in terms of number of fatalities and injuries. The impact on economy is measured by damage to crops and property.

According to the analysis result, the following events are top ones that impact the population health:
- tornado
- excessive heat
- lightning
- hurriane
- TSTM(Thunderstorm) Wind
- Thunderstorm

Following events have caused highest impact on economy:
- hurricane
- storm surge
- tornado
- hail
- flood
- flash flood

This report could be of interest to government or municipal managers who might be responsible for preparing for severe weather events and will need to prioritize resources for different types of events.


## Details in Rmd script

Details implemented in run_analysis.R:

*Preparation*
- Download the raw data from provided weblink, through download.file.
- Unzip the download file, through unzip. 
- Read data from downloaded compressed package. 

*Data handling*
- Filter out the variables used for further calculation.
- FIlter out data for the perios with enough data. The data from 2000 to 2011 are selected.
- Optimize Event type values to classify similar events with same name.
- Convert the exponent varabile for crops and property to numeral.
- Calculate damage to economy by summing property damage and crops damage.
- Calculate impact to population health by counting number of both fatalities and injuries.
