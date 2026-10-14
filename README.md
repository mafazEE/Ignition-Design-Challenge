# Introduction
This is SCADA/HMI application that was independently developed to meet the specified requirements of the 'Ignition Design Challenge' Doco at https://training.inductiveautomation.com/ignition-design-challenge/

Discussions on tag structure configuration will be provided soon
# Background
The Doco highlights a fictional company called RioOso owning a cold brew coffee factory with 20 identical brewing station sensor/actuator instances, the goal is to develope an HMI/SCADA that reads the process and discrete variables, as well as control them, create a user-based alarm notification system and real-time and historical trending and generate a report automatically on a specified schedule. 

# Software Used
Ignition SCADA/HMI Platform

Ignition Driver Module

Ignition Historian Module

Ignition Alarm notification Module

Ignition Reporting Module

PostgreSQL Server

PGAdmin

Papercut SMTP email emulator

# Application Demo
## Level 0 Overview Display 
![image alt](https://github.com/mafazEE/Ignition-Design-Challenge/blob/5cbeb311f665de099dff0d563ff85d32e5ec9eda/Level%200%20Brewing%20Stations%20Overview%20DisplayM.png)
The display consists of:

* 20 Station instances reflecting station-corresponding process variables of:

  - Brewing temperature Reading
  - Coffee brew type Reading
  - Machine status Write Control

* Docked Navigation bar pointing to Real-time and Historical Alarm List of all coffee brewing stations
* Docked navigation bar pointing to automatically generated report of station 3 to meet environmental health and safety regulations

## Level 1 Brewing Station Detail and Control Pop-up Display
![image alt](https://github.com/mafazEE/Ignition-Design-Challenge/blob/90024aa2d3adc87c15e00197e647f88296c9f573/Pop-up%20details%20and%20controls%20display.png)

The display consists of:
* Trending consisting of:
  - Temperature Plot of:
    - Water Temperature variable
    - High and Low Setpoints
  - Machine Mode Status Plot

* Controls consisting of:
  -  Adjusting setpoints High and low Temprature using *numerical input*
  -  Adjusting coffee brew type parameter using *cascading dropdown* to facilitate user input of 50 coffee brew types

* Real-time Alarm consisting of:
    - High and low setpoint Deviated Temperature variable
    - CLEANING MODE of coffee brewing machine
  
* An instance of the station overview

* Docked Navigation bar pointing to Real-time and Historical Alarm List of all coffee brewing stations
* Docked navigation bar pointing to automatically generated report of station 3 to meet environmental health and safety regulations

## Real-time and Historical Alarm List Display
![image alt](https://github.com/mafazEE/Ignition-Design-Challenge/blob/90024aa2d3adc87c15e00197e647f88296c9f573/Alarm%20Real-time%20and%20Historical%20List.png)

## Twice-a-day Automatically Generated Report on Station 3 Display
![image alt](https://github.com/mafazEE/Ignition-Design-Challenge/blob/90024aa2d3adc87c15e00197e647f88296c9f573/Automatically%20Generated%20Station%20Report.png)

## Verification of Off-System Alarm Notification using Papercut SMTP
![image alt](https://github.com/mafazEE/Ignition-Design-Challenge/blob/90024aa2d3adc87c15e00197e647f88296c9f573/Off-system%20Alarm%20Notification%20using%20Papercut%20SMTP.png)
Alarm notifications are recieved via email, verifying set-up SMTP connection

## Verification of Role-based Off-System Alarm Notification
![image alt](https://github.com/mafazEE/Ignition-Design-Challenge/blob/90024aa2d3adc87c15e00197e647f88296c9f573/Off-system%20role%20Based%20Alarm%20Email.png)
Alarm Notification are sent to appropriate plant floor personnel, user Connor is Roaster, so he receives Temp High AND Temp Low Alarms according to configured Alarm Notification Pipeline


