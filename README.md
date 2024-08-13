# Overview
New York is famously known for its yellow cabs. In this repository, I analyze New York City taxi data to understand traffic congestion, economic activity, and fare calculation strategies. The analysis includes calculating distances between locations, visualizing traffic congestion during different time slots, and determining average taxi income across various autonomous areas. I also reconstruct the fare and tip calculation methods to recompute and compare actual charges, excluding congestion surcharges, using mean absolute errors and variance as accuracy criteria.

And the dataset can be found in [new-york-city-taxi-trips-2019](https://www.kaggle.com/datasets/dhruvildave/new-york-city-taxi-trips-2019/data). This dataset contains all the recorded taxi rides from year 2019 which accounts to around 84.5 million trips. Due to the large volume of data, I leverage Spark SQL to accelerate processing and efficiently handle these large-scale datasets.

## I.Preprocessing
- Remove Unreasonable Values
  - Negative or zero distances or fares.
  - Passenger counts less than 1.
  - Pickup and dropoff times that don't make sense (e.g., dropoff before pickup).
- Remove Duplicate Rows
- Handle Missing Values


## II. Traffic Distance and Congestion Analysis

- Calculate the distances between various LocationIDs.
- Analyze the traffic congestion levels during different time periods.
- Provide a visual representation of the traffic congestion analysis.

## III. Taxi Income Analysis
- Compute the average taxi revenue for each autonomous city/town during different time slots (time granularity to be determined).
- Analyze and provide recommendations for taxi drivers on the best times to operate based on the revenue analysis.



## IV. Fare and Tip Calculation Modeling
- Deduce the New York City taxi fare calculation method and tip calculation method from the data.
- Recalculate the fares and tips using the derived formulas, without considering congestion fees, and compare them with the actual costs.
- Evaluate the fare calculation method based on the average of absolute errors and variance.
