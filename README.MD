# Analyzing Bicycle Trip Data of Pittsburgh's Healthy Ride Program

This repo stores all of the files used to analyze bikeshare trip data of Pittsburgh's Healthy Ride program.

## Project Motivation and Question(s) of Interest
This analysis is motivated by a hypothetical business intelligence goal for the Healthy Ride organization to learn more about bicycle and station utilization in order to focus maintenance efforts on the most heavily used assets.

This notebook seeks to answer multiple questions of interest related to station and bike utilization descriptive statistics, infers relationships between trip duration and user type and day of week variables, and attempts to model trip duration based on these variables. These questions are:

- **Station Utilization:**
    - What are the most frequent start and end stations?
    - What are the most frequent trip routes?
- **Bicycle Utilization:**
    - What is the total trip duration of each bike? Are some bikes used more often than others?
- **Trip duration trends:**
    - Is there a significant difference in trip duration between subscribers and customers?
    - Is there a significant difference in trip duration between trips taken during the week and those taken during the weekend?
    - Given this dataset, can trip duration be adequately modeled using data on user type, trip type, and whether or not a trip takes place during the week or weekend?

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

## Repo File Structure & File Descriptions

- data/
  - healthy-ride-rentals-q3-2020.csv (trip data)
  - healthy-ride-station-locations-2020-q3.csv (bicycle station data)
- gitignore
- PittHealthyRides.ipynb (main analysis notebook )
- README.MD

## Results Summary
The following insights were discovered as a result of this analysis:

- **Station Utilization:**
  - The top five station to station routes are all routes that are near central business districts, and they are all trips with destinations matching the origin.
- **Bicycle Utilization:**
  - The majority of all trips are made by customers.
  - The distribution of mean trip duration by bicycle is right-skewed, with the median of average trip durations between 5,674 seconds - this is roughly 95 minutes - approximately 1.5 hours.
- **Trip duration trends:**
  - On average customers have a much lower trip mean trip duration than subscribers. From this sample, we can estimate that the mean trip duration of customers is between 1,433 and 1,601 seconds(23.8 and 26.7 minutes). Whereas the mean trip duration of subscribers ins between 7,586 and 7,987 seconds (126.4 and 133.1 minutes ).
  - The sampling distributions of mean trip durations of weekday and weekend trips are non-overlapping, showing that trips during the weekend tend to be longer.
  - Only 3.8% of trip duration can be explained by user type, trip type, and day of the week. To be able to adequately model trip duration, it may be more ideal to have more information about the characteristics of the ride and rider (such as whether or not the trip is part of a tour group; if a trip were used for commuting to work, etc.). But unfortunately, this trip-level data was not available in the dataset.

A summary of the most actionable insights is documented in [this article](https://kristinamfrazier.medium.com/analyzing-bicycle-trip-data-of-pittsburghs-healthy-ride-program-a2729b313110).

## Acknowledgements
All of the datasets used for this project was accessed through the [Western Pennsylvania Regional Data Center](http://www.wprdc.org/). The [Healthy Ride](https://healthyridepgh.com/) organization provided their data to WPRDC.

This project was also part of a submission in completion of Udacity's Become a Data Scientist Nanodegree.
