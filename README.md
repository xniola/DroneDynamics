# Introduction

The project aims to identify the flight dynamics of a drone, and possibly use the acquired information for the detection of an engine failure, by training a neural network using a Dataset generated from a Simulink model.
To carry out the project, we trained two types of neural networks: an LSMT network on Python and a NARX network from Matlab's Neural Network Toolbox.

# Dataset

An initial dataset of a quadrotor with 12 different trajectories was provided for network training; for each trajectory there is a table file containing 60,000 rows and 16 columns (sampling time is 0.5 ms for a total time period of 30 seconds). 
The triad integral to the quadrotor is placed as in the following figure with the axes and motors numbered counterclockwise:

<div style="text-align:center; margin-bottom:20px;">
  <img src="https://github.com/xniola/DroneDynamics/blob/main/DronePhoto.png" width="500" height="400">
</div>

# Features
On the table below the features of the dataset are listed and described:
Variable | Description | Unit of measurement | 
--- | --- | --- |
time | Moment of acquisition | s |
xF, yF, zF | Location of the center of mass | m
xFdot, yFdot, zFdot | Linear velocity of the center of mass | m/s
p,q,r | Instantaneous rotation speeds around the XB, yB, zB axes | rad/s
phi,theta,psi | Euler angles describing the drone's angular orientation (attitude), following the roll, pitch, yaw convention | rad
Omega1,Omega2,Omega3,Omega4 | Angular speeds of engines | rad/s

Motor speeds are considered positive and follow what is given in the following table:
Engines | Rotation direction | 
--- | --- |
1,3 | counter-clockwise |
2,4 | clockwise |

# Models
## Gru network
Gated Recurrent Unit (GRU) Network:
A Gated Recurrent Unit (GRU) is a type of recurrent neural network (RNN) architecture that is designed to capture long-term dependencies in sequential data. It is a variation of the traditional RNN that aims to address the vanishing gradient problem, which can occur when training RNNs on long sequences.

## Linear Regression
Linear Regression is a simple and widely used statistical method for modeling the relationship between a dependent variable and one or more independent variables. The basic idea is to find the best-fitting linear relationship (a line) between the independent variables and the dependent variable.

# Results

