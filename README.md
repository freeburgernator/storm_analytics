# storm_analytics
### Data analysis project for C S 329E, handling storm data with a Darwin SDK from SparkCognition.

#### Problem  

We created a model which analyzed past weather events throughout the US to predict property damage possibly caused by future events. The model can be used to help insurers and homeowners make educated decisions about property damage and how to handle severe weather.      

#### Data Sets

##### /data_details/
StormEvents_details-ftp_v1.0_d{year}_c{data}.csv.gz: From the raw dataset, there is a .csv for all weather events each year from 2008 to 2018.       

##### /event_subsets/   
heavy_rain_train.csv: Contains a subset (80%) of records of all heavy rain events from 2008-2018. The data was cleaned and feature engineered. Columns with unneeded, null, or 0 values were dropped. An additional column was added for duration of each event in seconds, and a column of labels was added after binning property damage.        

heavy_rain_test.csv: Contains the remainder (20%) of the records of all heavy rain events, cleaned exactly as the dataset above.   

#### Jupyter Notebooks   

Tornado_Model.ipynb: The first data set to sort the property damage into bins. It predicts how much property damage tornado events will cause but has low accuracy and F1 scores.

Heavy_Rain_Model.ipynb: Predicting how much property damage heavy rain events will cause with binning and Darwin's supervised learning algorithm. It has unexpectedly high accuracy scores, likely due to the data being unbalanced. 
