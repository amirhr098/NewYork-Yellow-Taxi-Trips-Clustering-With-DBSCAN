# NewYork Yellow Taxi Trip Duration & Distance Clustering Project


This project utilizes DBSCAN clustering algorithm from scikit-learn library to cluster the trip duration and distance data.


Original Data: https://www.kaggle.com/c/nyc-taxi-trip-duration (Only used 'train.csv'.)


The data is read from a csv file and then two columns, "trip_duration" and "distance", are extracted and used as the feature set for clustering. The script then loops over different values of "eps" and "min_samples" hyperparameters to determine the best combination that results in maximum calinski harabasz score.

## Requirements
     
+ Pandas
     
+ Numpy
     
+ Sklearn
     
## Data

The data contains 1458644 rows and 11 columns with information such as pickup and dropoff times, passenger count, pickup and dropoff locations, and trip duration.


## Feature Extraction

The "distance" feature is calculated as the Euclidean distance between the pickup and dropoff locations.


## DBSCAN Clustering

DBSCAN is run with "eps" and "min_samples" hyperparameters, the values of which are looped over to determine the best combination. The "eps" parameter controls the maximum distance between two samples for them to be considered as part of the same neighborhood, while "min_samples" sets the minimum number of samples required to form a dense region.

The best parameters found for DBSCAN in this script are eps = 1.95 and min_samples = 300, with a calinski harabasz score of 2745.44.

<pre>{'algorithm': 'auto',
 'eps': 1.95,
 'leaf_size': 30,
 'metric': 'euclidean',
 'metric_params': None,
 'min_samples': 300,
 'n_jobs': None,
 'p': None}</pre>
 
## Results

The results of the script are the best combination of hyperparameters that result in maximum calinski harabasz score. This score is a measure of the quality of clustering and the higher the score, the better the clustering.


## Help
  
Feel free to send better clustering value for me:)

E-mail: amirhr098@yahoo.com

SocialMedia: @Amirhr098
