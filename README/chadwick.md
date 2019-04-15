# Milestone 1

## Objective
A full functional component that supports CAN message and GPS data collection from a Car via Carloop and its associated GPS components

## Design Scheme
Collect data within the Particle Photon from the Carloop GPS and the Carloop Basic that’s attached to the OBD2 port of a vehicle. This data is printed to a serial port to verify data is being collected.

## Hardware
### Carloop basic
Retrieves CAN messages through a vehicles OBD2 port.
### Carloop GPS
Obtains GPS coordinates of the carloop in real-time.
### Particle Photon
Allows code to be added to it through the Particle IDE. Photon code controls gathering the CAN message and GPS data.

## Software
### Particle IDE
IDE that uses c++ to add functionality to the Particle Photon and associated components.			

## Configuration
Setup Particle Photon (https://docs.particle.io/quickstart/photon/)
Enter the IDE
Create a new app and add Carloop library to it.
Use Carloop library objects (carloop) and functions (.gps() and .can()) to retrieve CAN and GPS information. 
(https://docs.particle.io/reference/device-os/firmware/photon/)
Print information to serial port or publish it to the particle console to confirm reception.	
