# Introduction

The project aims to identify the flight dynamics of a drone, and possibly use the acquired information for the detection of an engine failure, by training a neural network using a Dataset generated from a Simulink model.
To carry out the project, we trained two types of neural networks: an LSMT network on Python and a NARX network from Matlab's Neural Network Toolbox.

# Dataset

An initial dataset of a quadrotor with 12 different trajectories was provided for network training; for each trajectory there is a table file containing 60,000 rows and 16 columns (sampling time is 0.5 ms for a total time period of 30 seconds). 
The triad integral to the quadrotor is placed as in the following figure with the axes and motors numbered counterclockwise:
 
 ![Uploading Screenshot 2024-01-10 alle 00.52.18.png…]()
