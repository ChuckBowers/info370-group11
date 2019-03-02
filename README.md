# info370-group11

## Project Description

- For our final project, we are trying to answer what effect, if any, the weather has on outgoing flights. More specifically we are interested in the weather in Seattle and its effect on flights leaving SeaTac. We believe this to be an important topic as thousands of people fly through Seattle everyday, and as all of us as residents know Seattle's weather can be both variable and rainy. If we were be able to inform either the populace of Seattle or the organization of SeaTac with this information, the hope would be that individuals would be more prepared for their journeys, and that SeaTac can react accordingly.

- Flight delays can have costly consequences. It is estimated that in the U.S. alone, flight delays have a 40.7 billion dollar impact. Additionally, all of that time planes spend on the tarmac results in excess fuel being used and more emissions being released (Fleurquin). Flight delays also result in significant disruptions to aviation safety and the decreased traffic results in losses for the airlines (Gao, 68). Flight delays also cause passengers to prefer other airlines if they experience delays with a certain carrier (Tae-Hwee Lee, 277). Causes of flight delays can range from the unpreventable, severe weather (Gao, 68), to the preventable, crew mishaps and flight order rotation (Fleurquin).

- The specific question we hope to answer with this data is, given a particular day at SeaTac International Airport, can we predict the average departure delay for all flights based upon the weather? Our _null hypothesis_ would be: there is no relationship between the average daily departure delay at SeaTac and the weather at SeaTac. Conversely, our _alternative hypothesis_ would be: there is a relationship between the average daily departure delay at SeaTac and the weather at SeaTac.

- To estimate the average departure delay at SeaTac International Airport (SEA), two datasets 1) flight delay data at SEA and 2) weather data of SEA will be used. From [Kaggle](https://www.kaggle.com/fabiendaniel/predicting-flight-delays-tutorial/data), we acquired the 2015 flight delays and cancellations dataset. This dataset contains three tables including the list of airlines, airports and the actual flights. From [National Centers for Environmental Information (NCEI)](https://www.ncdc.noaa.gov/), we downloaded the weather data for the year of 2015 that is recorded by weather station at Seattle Tacoma International Airport (SEA).  

- We intend to employ linear multivariate regression on modeling. It is unlikely to use a univariate regression unless there is a single weather factor that exerts an extremely significant effect on flight delays. On the side of machine learning, we expect to use cross-validation and grid search to evaluate the flight delay.  

- There are a couple of audience groups for our project. For example, the Department of Transportation (DOT) and the airlines may issue prior delay notice and operate accordingly on the given estimated information. Moreover, There are also airport rating agencies around which would use the data for ratings on airport efficiency of responsiveness on weather conditions. However, the primary audience for our project is Seattle-based travelers. Since we are only evaluating flights departing from Seattle Tacoma International Airport, all travelers through SEA, especially frequent flyers based in the Greater Seattle Area will benefit from our project.  

- Our resource serves all travelers who travel through Seattle Tacoma International Airport (SEA), especially those based in Seattle. Before travelers heading to the airport or before passengers with connecting flight landing, with the resource we provide, they may be able to have a rough prediction on how long their flights will be delayed. Travelers could also modify the schedule of subsequent activities.  

## Technical

- Our paper will be presented in an HTML page exported using ipynb. 

- The first dataset we found relevant to our question contains information on all US domestic flights in 2015 operated by 14 American airlines. The large size of the flights dataset (500MB+) could make it difficult to load and share, by filtering out the rows that have 'SEA' as the value for origin airport, we are able to reduce the size from ~5800,000 rows to ~110,000. A potential problem for our research question is our treatment of flight cancellation. In the dataset, cancelled flights have a 'CANCELLED' value of 1, and null for the actual departure/arrival time, so there is the need to differentiate between cancelled and normal flights in the calculations. The weather dataset includes daily weather information such as wind, precipitation and snowfall. Again, treatment of null values can be a challenge in this dataset. There is a large amount of null values in several columns. We will need to make trade-offs to drop unimportant columns from our analysis. In addition, airports rely on weather data available at present to make decisions about potential flight delays in the future, so a time-lagged variable might be better at predicting flight delays. 

- We will need to get familiar with more Pandas manipulations we are not currently used to doing for the project. Because we are dealing with two separate datasets with completely different format (each row in the flight dataset represent a flight while each row in weather dataset represent a day), we will need to group the two data frames together using specific types of join that makes sense, and transform the result into the desired format (average flight delay for a given day in minutes). 

- To conduct our analysis we need to first prepare our data by handling missing values (potentially mean of adjacent rows) and normalizing it to a common scale. Then we will create new features by combining data from existing columns. In order to not overfit our data and create noise, we will select features that are co-related and remove ones with low variance. To select our best model we need to find a balance between _bias_ (under fitting our data, making our model inflexible and so it doesn’t account for all our features) and _variance_ (overfitting  our data so that our model accounts for random errors and underlying distribution of our data). To validate our model and hyperparameters are a good fit to our data we’ll use cross-validation. This will give us a better understanding of how our algorithm is performing and allow us to use all of our data for training. By splitting out data into subsets, we’ll improve our validation accuracy. Using grid search and mean absolute error as a scoring metric, we’ll find the optimum parameters for our model.

- As I mentioned above, the treatment of cancelled flights is certainly a technical challenge to our analysis approach. In terms of feature engineering, we need to ouside research to identity potential factors that we want to include, or exclude variables that introduce noise. Unlike linear relationships we dealt with in past assignments, there might be polynomial relationships we need to account for using polynomial transformations. We also need to figure out ways of scaling/offsetting the data to give us a better model performance. 

## Works Cited

- Fleurquin, Pablo et al. “Systemic delay propagation in the US airport network” Scientific reports
    vol. 3 (2013): 1159.

- Gao, Mingang. “Models Responding to Large-Area Flight Delays in Aviation Production Engineering.”
    NeuroImage, Academic Press, 2 June 2012, www.sciencedirect.com/science/article/pii/S2211381912000549.

- Tae-Hwee Lee, Taylor. “Impact of Flight Departure Delay on Airline Choice Behavior.” NeuroImage,
    Academic Press, 6 Feb. 2018, www.sciencedirect.com/science/article/pii/S2092521217300676.
