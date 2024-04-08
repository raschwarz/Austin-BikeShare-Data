# Austin-BikeShare-Data
We inspected a data set produced by the City of Austin on BikeShare data in Austin, Texas, between the years of 2013-2017. We used two data sets, one consisting of ~650k rows, and 12 columns, each associated with a bike ‘ride’, and the other consisting of 72 rows, and 6 columns, each row being a bike station. Later you will see we merged the two data sets for prediction modeling.

We focused on the following columns:
duration_minutes: int minutes of trip duration
start_station_id: integer id of start station(data set 2)
start_time: YYYY-MM-DD HH:MM:SS
subscriber_type: membership type.g. walk up, annual, other bike share, etc
station_id: unique station id, int (data set 1)

We used a Decision Tree Classifier to classify walk-ups and annual subscribers, splitting the data into training, testing and validation sets. We also balanced the classes - and we needed up getting a model with an AUROC score of 0.87! This was our best model at predicting the subscriber type (annual or walk-up), using bike station region column, duration of ride column, and the week of the year column. 
