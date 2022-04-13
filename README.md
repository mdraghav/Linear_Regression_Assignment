# Linear Regression Model for Prediction of Hiring of Bikes
- A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.

- In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19.


## Table of Contents
* [Objective](#Objective)
* [Business Goal](#business-goal)
* [Data Caveats](#data-caveats)
* [Model Buidling](#model-building)
* [Libraries Used](#Libraries-used)
* [Data Dictionary](#data-dictionary)
* [References](#references)
* [Inferences](#inferences)
* [Critical Features](#critical-features)
* [Data Citation](#data-citation)


<!-- You can include any other section that is pertinent to your problem -->
## Objective
- Build a multiple linear regression model for the prediction of demand for shared bikes.

## Business Goal
 - Find variables are significant in predicting the demand for shared bikes and how well those variables describe the bike demands. Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors.

- Based on the goal mentioned above, model the demand for shared bikes with the available data.

## Data Caveats

* In the dataset that some of the variables like 'weathersit' and 'season' have values as 1, 2, 3, 4 which have specific labels associated with them (as described in the data dictionary). These numeric values associated with the labels may indicate that there is some order to them - which is actually not the case. So, it is advisable to convert such feature values into categorical string values before proceeding with model building.

* The column 'yr' has two values 0 and 1 indicating the years 2018 and 2019 respectively. Since these bike-sharing systems are slowly gaining popularity, the demand for these bikes is increasing every year proving that the column 'yr' might be a good variable for prediction. So think twice before dropping it.

## Model building

 - In the dataset provided,there are three columns named 'casual', 'registered', and 'cnt'. The variable 'casual' indicates the number casual users who have made a rental. The variable 'registered' on the other hand shows the total number of registered users who have made a booking on a given day. Finally, the 'cnt' variable indicates the total number of bike rentals, including both casual and registered. The model should be built taking this 'cnt' as the target variable.

## Libraries Used
- Pandas
- Numpy
- Seaborn
- Matplotlib
- Scikit Learn
- Statsmodels

## Data Dictionary

- instant: record index
- dteday : date
- season : season (1:spring, 2:summer, 3:fall, 4:winter)
- yr : year (0: 2018, 1:2019)
- mnth : month ( 1 to 12)
- holiday : whether day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
- weekday : day of the week
- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
- weathersit :
> - 1: Clear, Few clouds, Partly cloudy, Partly cloudy
> - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
> - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
> - 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
- temp : temperature in Celsius
- atemp: feeling temperature in Celsius
- hum: humidity
- windspeed: wind speed
- casual: count of casual users
- registered: count of registered users
- cnt: count of total rental bikes including both casual and registered

## References
* https://www.rmets.org/metmatters/beaufort-scale
* http://www.city-data.com/forum/weather/1620160-your-personal-temperature-colors-descriptors.html
* https://stackoverflow.com/questions/64556501/plot-only-some-columns-with-seaborn-pairplot
* https://stackoverflow.com/questions/19071199/drop-columns-whose-name-contains-a-specific-string-from-pandas-dataframe
* https://www.geeksforgeeks.org/multicollinearity-in-data/
* https://github.com/statsmodels/statsmodels/issues/2376
* https://stackoverflow.com/questions/48522609/how-to-retrieve-model-estimates-from-statsmodels
* https://www.statsmodels.org/devel/generated/statsmodels.regression.linear_model.RegressionResults.html
* https://stackoverflow.com/questions/37508158/how-to-extract-a-particular-value-from-the-ols-summary-in-pandas
* https://gist.github.com/zhiyzuo/972b8b95e115c44d6805c929b7b4e2ca
* https://stackoverflow.com/questions/47388258/how-to-extract-the-regression-coefficient-from-statsmodels-api
* https://stackoverflow.com/questions/51734180/converting-statsmodels-summary-object-to-pandas-dataframe/52976810
* https://gist.github.com/zhiyzuo/972b8b95e115c44d6805c929b7b4e2ca
* https://stats.stackexchange.com/questions/101274/how-to-interpret-a-qq-plot
* https://stats.stackexchange.com/questions/111010/interpreting-qqplot-is-there-any-rule-of-thumb-to-decide-for-non-normality/111013#111013
* https://www.analyticsvidhya.com/blog/2021/05/know-the-best-evaluation-metrics-for-your-regression-model/

## Inferences

- Rental demand is higher when the weather is fair (clear or mildly cloudy)
- Not much effect on overall demand, however surge observed in casual rentals
on non-working days
 - Not much effect on overall demand, however surge observed in casual rentals
on Saturday and Sunday (which incidentally are also non-working days)
 - Significant increase observed in Summer, Autumn and Winter season.
Significant surge observed in casual hiring in Summer season
 - Increase in wind speed has a detrimental effect on number of bikes hired.
Noticeable dip observed in casual rider-ship when wind speeds exceed 19 KmpH
 - Temperature is directly correlated rider-ship till its quite warm (<35 deg C).
Beyond which there are hardly any rentals
 - Rentals are observed only during periods when humidity is within comfort
levels, lower and beyond which they taper off
 - Rental has shown growth YoY. However, data is sparse to draw any meaningful
inferences.
 - Rental demand is observed to increase as winter reduces and peaking towards
autumn after which it reduces as Winter approaches.
 - Earnings show an upswing in the Second and Fourth Quarter



## Critical Features
- workingday
- temp 
- hum 
- windspeed 
- registered 
- mnth (few)
- season (few)

## Data Citation

- The data for this project has been sourced from Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.
- For further information about this dataset, please contact Hadi Fanaee-T (hadi.fanaee@fe.up.pt)


## Contact
Created by [@ishankarve] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->