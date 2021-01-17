# Analyzing Bicycle Trip Data of Pittsburgh's Healthy Ride Program

This repo stores all of the files used to analyze bikeshare trip data of Pittsburgh's Healthy Ride program. This analysis is motivated by a hypothetical business intelligence goal for the Healthy Ride organization to learn more about bicycle and station utilization in order to focus maintenance efforts on the most heavily used assets.

## Requirements
In order to replicate this analysis, the following is required:

- Installation of the following modules and libraries:
  - Pandas
  - Numpy
  - Matplotlib
  - Math
  - Scikit-learn
- Datastets:
  - [Healthy Ride Trip Data: Healthy Ride Rentals - 2020 Q3](https://data.wprdc.org/dataset/healthyride-trip-data)
  - [Healthy Ride Stations](https://data.wprdc.org/dataset/healthyride-stations)

## Analysis Replication
Those who wish to replicate this analysis should follow along with the code blocks in the [PittHealthyRides](https://github.com/KristinaMFrazier/healthyride/commit/5a2a546b28be01ffa81ff192760e5b64c89e21f3) jupyter notebook. Please make a note of where the trip and ride stations datasets are referenced in the notebook and revise these codes to match unique file paths.

Also, it is not necessary to replicate this analysis using the 2020 Q3 data. In fact, new seasonal insights may be uncovered by using another quarter, or even by aggregating multiple datasets. However, please note some changes to the datasets that Healthy Ride may have made based on new classifications of data, additional stations, etc., which may require some adjustments to the code to preserve functionality if you use earlier datasets. For example, it is only in the most recent quarters that Healthy Ride allowed for "dockless" start and end locations. Therefore, only in recent quarters are these dockless trips listed with start and end locations not at official bikeshare stations. This and other changes are documented on the [Healthy Ride data website](https://healthyridepgh.com/data/).

## Acknowledgements
All of the datasets used for this project was accessed through the [Western Pennsylvania Regional Data Center](http://www.wprdc.org/). The [Healthy Ride](https://healthyridepgh.com/) organization provided their data to WPRDC.

This project was also part of a submission in completion of Udacity's Become a Data Scientist Nanodegree.
