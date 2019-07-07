# CarND-Path-Planning-Project
Self-Driving Car Engineer Nanodegree Program

# Overview
 The Project aims at safely navigating a car having highway with 50mph speed limit.
Also the car should not experience total acceleration over 10 m/s^2 and jerk that is greater than 10 m/s^3.the code will be ru un the udacity simulator , which can be downloaded [here](https://github.com/udacity/self-driving-car-sim/releases/tag/T3_v1.2) .
The communication between the simulator and the path planner is done using WebSocket. 

##Prerequisites
  The project has the following dependencies (from Udacity's seed project):

    cmake >= 3.5
    make >= 4.1
    gcc/g++ >= 5.4
    libuv 1.12.0
    Udacity's simulator.

## Compilation and Execution


1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./path_planning`.

# Performance 
 
 All the criteria requested in Rubric is met
 1.code compiles
 2.No collision,max accelearetion or jerk
 3. car changes lanes 
 4.has run 12 miles without collision![Output](./data/pp6.png)

# Design and code Flow

1. Prediction 
   with sensor fusion data prediction is made if
    a. Car is ahead of us
    b. Car is present in Right /left lane
2.Behaviour planning
   there are three state in current planning 
    a. Keep Lane
    b. Lane Change left
    c. Lane change Right
    this part of the code deals with when to change the lane and when to keep following 
3.Trajectory 
   This part of the code uses car coordinates ,speed and past points to calulate the trajectory  

