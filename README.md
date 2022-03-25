# Data Engineering Challenge

## Context

We have a list of tracking signals containing the approximate geo-location of users on internet. 
To help us show the right ads to the right users, we want to know the nearest airport for each user.

## Datasets

You are provided with two sample datasets:

* `optd-airports-sample.csv.gz` - A simplified version of a data set from Open Travel Data, containing geo-coordinates 
of major airports:
    * IATA airport code - a three-character identifier of global airports (first column)
    * Latitude and Longitude in floating point format (second and third columns, respectively)

* `user-geo-sample.csv.gz` - Some sample input data for your application, containing:
    * A universally unique identifier (uuid) which acts as a user-id for some end-user (first column)
    * Latitude and Longitude in floating point format (second and third columns, respectively)
    * Each row of the CSV can be considered as a single user tracking event.

## Requirements

Your application will need to do the following:
  
* Parse an input data-source containing events with the same fields as in the sample csv: user-id and geo-coordinates.

* Geo-distance calculation: Take the users' coordinates and compare this with the set of airport coordinates to get the
  IATA code with the closest geo-distance to the user.

* For each user input event, your application is expected to output one event containing two fields: 
  user-id and an IATA code corresponding to the closest airport.

* Your application must be scalable. 
  In a real-world scenario, we might receive hundreds or even thousands of events per second.

## Deliverable 

The goal of this challenge is to provide an implementation which satisfies the requirements from above whilst demonstrating your coding style as well as your software design and engineering skills.

Your solution should be a high-quality prototype, showing your ability to write readable and maintainable code. You should be able to discuss any limitations of your implementation and trade-offs that you have made during development.

We recommend you clone this repository and keep track of any decisions in a readme file whilst working on your solution. Please provide the source code of the final solution together with the readme in a zip (archive) file.

## Environment & Language

You have a free hand in choosing the programming language, framework, and environment in which the code is developed and demonstrated. For any further questions, feel free to reach out to your contact at travelaudience.

## Licensing 

* `user-geo-sample.csv.gz`

The longitude, latitude data in this sample was taken from a dataset provided by Maxmind inc.
This work is licensed under the [Creative CommonsAttribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

This database incorporates [GeoNames](http://www.geonames.org) geographical data, which is made available under the 
[Creative Commons Attribution 3.0 License](http://www.creativecommons.org/licenses/by/3.0/us/).

* `optd-airports-sample.csv.gz`

Licensed under Creative Commons. For more information check [here](https://github.com/opentraveldata/opentraveldata#licensing).
