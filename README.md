# info370-group11

## Project Description

- For our final project, we are trying to answer what effect, if any, the weather has on outgoing flights. More specifically we are interested in the weather in Seattle and its effect on flights leaving SeaTac. We believe this to be an important topic as thousands of people fly through Seattle everyday, and as all of us as residents know Seattle's weather can be both variable and rainy. If we were be able to inform either the populace of Seattle or the organization of SeaTac with this information, the hope would be that individuals would be more prepared for their journeys, and that SeaTac can react accordingly.

- Flight delays can have costly consequences. It is estimated that in the U.S. alone, flight delays have a 40.7 billion dollar impact. Additionally, all of that time planes spend on the tarmac results in excess fuel being used and more emissions being released (Fleurquin). Flight delays also result in significant disruptions to aviation safety and the decreased traffic results in losses for the airlines (Gao, 68). Flight delays also cause passengers to prefer other airlines if they experience delays with a certain carrier (Tae-Hwee Lee, 277). Causes of flight delays can range from the unpreventable, severe weather (Gao, 68), to the preventable, crew mishaps and flight order rotation (Fleurquin). 

- The specific question we hope to answer with this data is, given a particular day at SeaTac International Airport, can we predict the average departure delay for all flights based upon the weather? Our _null hypothesis_ would be: there is no relationship between the average daily departure delay at SeaTac and the weather at SeaTac. Conversely, our _alternative hypothesis_ would be: there is a relationship between the average daily departure delay at SeaTac and the weather at SeaTac.

- To estimate the average departure delay at SeaTac International Airport (SEA), two datasets 1) flight delay data at SEA and 2) weather data of SEA will be used. From [Kaggle](https://www.kaggle.com/fabiendaniel/predicting-flight-delays-tutorial/data), we acquired the 2015 flight delays and cancellations dataset. This dataset contains three tables including the list of airlines, airports and the actual flights. From [National Centers for Environmental Information (NCEI)](https://www.ncdc.noaa.gov/), we downloaded the weather data for the year of 2015 that is recorded by weather station at Seattle Tacoma International Airport (SEA).  

- We intend to employ linear multivariate regression on modeling. It is unlikely to use a univariate regression unless there is a single weather factor that exerts an extremely significant effect on flight delays. On the side of machine learning, we expect to use cross-validation and grid search to evaluate the flight delay.  

## Technical 

## Works Cited

- Fleurquin, Pablo et al. “Systemic delay propagation in the US airport network” Scientific reports 
    vol. 3 (2013): 1159.

- Gao, Mingang. “Models Responding to Large-Area Flight Delays in Aviation Production Engineering.” 
    NeuroImage, Academic Press, 2 June 2012, www.sciencedirect.com/science/article/pii/S2211381912000549.

- Tae-Hwee Lee, Taylor. “Impact of Flight Departure Delay on Airline Choice Behavior.” NeuroImage, 
    Academic Press, 6 Feb. 2018, www.sciencedirect.com/science/article/pii/S2092521217300676.
