# Data Engineering Challenge

## The Objective

We have a list of tracking signals containing the approximate geolocation of users on internet. To help us show them the right ads, we want to know which airport they are closest to.

## Data-sets

You will be provided with two sample data sets to consume:

* `optd-airports-sample.csv.gz` - A simplified version of a data set from Open Travel Data, containing geo-coordinates of major airports:
    * IATA airport code - a three-character identifier of global airports (first column)
    * Latitude and Longitude in floating point format (second and third columns, respectively)

* `user-geo-sample.csv.gz` - Some sample input data for your application, containing:
    * A universally unique identifier (uuid) which acts as a user-id for some end-user (first column)
    * Latitude and Longitude in floating point format (second and third columns, respectively)
    * Each row of the CSV can be considered as a single user tracking event.

## Task.

Your application will need to do the following:
  
* Parse an input data-source containing events with the same fields as in the sample csv: user-id and geo-coordinates.

* Geodistance calculation: Take the users's coordinates and compare this with the set of airport coordinates to get the IATA code with the closest geodistance to the user.

* For each input event, your application is expected to output one event containing two fields: user-id and an IATA code corresponding to the closest airport.

* Your application must be scalable. In a real-world scenario, we might get hundreds or even thousands of such events per second.

## Deliverables 

The purpose of this task is to provide code which satisfies the task above whilst at the same time demonstrating your coding style as well as your design and engineering skills.

Your code should be a production-grade prototype and you should be able to defend your approach and be able to discuss any limitations/trade-offs you have made in your design.

## Environment

You have a free hand in choosing the environment in which this code is developed and demonstrated.

## Languages

Must be in Scala.

## Licensing 

* `sample_data.csv.gz`

The longitude, latitude data in this sample was taken from a data-set provided
by Maxmind inc.

This work is licensed under the Creative Commons
Attribution-ShareAlike 4.0 International License. To view a copy of
this license, visit http://creativecommons.org/licenses/by-sa/4.0/.

This database incorporates GeoNames [http://www.geonames.org]
geographical data, which is made available under the Creative Commons
Attribution 3.0 License. To view a copy of this license, visit
http://www.creativecommons.org/licenses/by/3.0/us/.

* `optd-sample-20161201.csv.gz`

Licensed under Creative Commons - for more information see 
https://github.com/opentraveldata/optd/blob/trunk/LICENSE

* All other data

All other data in this repository is Copyright travel audience GmbH. 
