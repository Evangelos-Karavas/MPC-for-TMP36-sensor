# MPC-for-TMP36-sensor

In the folder Matlab Code there is a file for the MPC model in Simulink and the all the workspace variables needed to run the project.
Also there is the Schematics file to see and understand all the connections needed for the project to work.

# About
This project was created to understand the Model Predictive Control in association with the TMP36 sensor.
The sensor sends data to the controller, which has a reference point for the sensor to reach. We stimulate
the sensor with a power transistor who operates only on the command of the controller.

At first, we need a model for the controller, so we had to stimulate the sensor with a PRBS signal, and take its data to
the System Identification App in Matlab. Then, we continue to extract the model (Process Model) and use it as our system
in the MPC Designer Block.

Subsequently, we can also tune the Controller. To do so, we can set some Constraints about the temperature, or make the
controller more Robust or Aggressive. After you make some changes, you can save the changes on the controller.

# Use
To run the code, you need to setup the Hardware and select the Run on board or Connected IO. Setup the Stop Time to be 
infinite and change the ref block to whatever temperature you want. The temperature must be between the ranges of your
sensor (In my case I chose 50 degrees C).
