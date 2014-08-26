Precipitation Forcast
=============

A Mathematica project, Short-Term Precipitation Forcast!

This project was done in a 3-week work at Wolfram Science Summer School 2014 under supervision of Stephen Wolfram.


## Files Description

There are three Mathematica notebooks in this project and one needs Mathematica version 10 to open these files. [finalProject_Demo.nb](https://github.com/soltaniehha/precipitation/blob/master/finalProject_Demo.nb) is a demo version and only for demonstration of the project. If you wants to try the code by yourself then may want to use the other two notebooks. The code [UWeather.nb](https://github.com/soltaniehha/precipitation/blob/master/UWeather.nb) needs to be running at least for an hour in order to take and save the radar images from the Weather Underground API before you can start the real time calculation, file [finalProject_RealTime.nb](https://github.com/soltaniehha/precipitation/blob/master/finalProject_RealTime.nb).

## Project Description

Base reflectivity radar images contain information about the structure of the clouds, how dense they are and whether they carry water or hail. The unit of reflectivity is on dBZ (decibels) which is a logarithmic scale and the values normally vary from 5 dBZ to 75 dBZ. Typically light rain occurs when this reaches 20 dBZ. The purpose of this project is to track the clouds and see when they are reaching a given location on the map and whether it's going to rain or not for the next hour or so. Also a rough picture of the location and size of the clouds in the near future can be predicted. The cloud images are taken from Weather Underground API every 6 minutes for the state of Massachusetts and the information about the clouds are derived by images processing, stored as a time-dependent database for each image, and analyzed their behavior by predictive modeling. 

![Alt text](https://github.com/soltaniehha/precipitation/blob/master/files/sample.png "A snapshot of the project!")

We are able to predict the precipitation by looking at the circle area shown in the image and see if there is a rainfall happening. If we observe some precipitation most likely it's going to happen in the targeted location, which is Boston in our example. In order to check the precipitation one can use the radar data and check whether the value for reflectivity is indicating rain or not, or make a query from either Wolfram language or Weather Underground API current condition. Averaging these values might result a better prediction since each data may have a different source. For this particular example shown here the circle is drawn one hour apart based on the speed of the clouds calculated by the program.

One can use this code to download radar images every 6 minutes from Weather Underground API: [UWeather.nb](https://github.com/soltaniehha/precipitation/blob/master/UWeather.nb) This code needs to be running for at least 60 minutes, and after that running in the background, in order to have enough data for starting the actual prediction application which will do the rest in real time: [finalProject_RealTime.nb](https://github.com/soltaniehha/precipitation/blob/master/finalProject_RealTime.nb).

One needs to run a demo of the code in a given time in the past here is an example predicting Boston precipitation on July 15 2014, for 5 to 6 p.m. and comparing it with the actual radar images taken for the same time frame: [finalProject_Demo.nb](https://github.com/soltaniehha/precipitation/blob/master/finalProject_Demo.nb).
