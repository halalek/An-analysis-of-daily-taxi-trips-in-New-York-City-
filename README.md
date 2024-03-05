# An analysis of daily taxi trips in New York City
Analysis of daily taxi trips in New York City using a large set of records The analysis aims to identify patterns and trends in the data and make predictions about demand for taxis and future revenues based on these historical patterns.

# Investigation limitations
1. Programming language: Python
   
2. Work environment:Jupyter Notebook, Colab.

3.Data: Taxi rides in New York City


# Requirements
## 1. Data cleaning and integration
### a. The essence of time
i. We have historical data containing yellow taxi trips that took place between 2019
And 2022, that is, during the past four years in New York City, which was collected by a number of
Local agencies. It requires creating a Time Series for the number of trips
And the total revenue (Revenue Total) during each hour of the day for
Every agency within the data set.

ii. Before starting the construction process, you must clean the data set, i.e. you must solve
Problems of null, extreme, and contradictory values in a way you see fit.

iii. The dataset must contain at least 120 million records before a build can be done
Time series.

iv. Try to work in a distributed environment (use Docker if you can for ease Setting)

v. Perform a simple poll of the data set to make cleaning easier.

vi. Save the clean data set on the hard disk in parquet format
For use in the following stages.

## Directive: 
All data manipulation must be done using Dask due to the sheer size
For the number of records, try using Pandas only to store statistical results and small tables
the size.

### b. Set the time machine

i. Use string manipulation techniques to ensure that the final set is verified
Time series data conditions.

ii. Store the final data set in a long-format table.
On the hard disk in csv format.

## 2. Feature engineering
● Create a zone_source attribute to denote the starting zone

● Create a zone_destination attribute to denote the end zone

● Create a borough_source attribute to denote the starting municipality

● Create a borough_destination attribute to denote the end municipality

● Create a pair_location attribute that includes the start and end zone regardless

Regardless of order (consider traits as commutative) in a separated comma manner.

● Create a name_type_payment attribute to denote the payment method

● Create a vendor attribute to represent the agency name

● Create a code_rate attribute to indicate the fare calculation mechanism

● Create a class_trip attribute that contains the trip class based on iterations
pair_location within the data set as follows

In a way that classifies each stroke and eye (rare, less-common, common, more-common)
You deem it appropriate, explaining this in the notebook.

● Create a duration_trip attribute to denote the duration of the trip (in minutes)

● Convert the distance_trip attribute to kilometers instead of miles traveled.

### Directive: 
Dump the start and end hierarchy attribute within the pair_location attribute and then use
Tripping technique to create class_trip attribute.

### Note:
You may need to store a data set on the hard disk more than once
To ease calculations and reduce the size of the Graph Computation Dask
