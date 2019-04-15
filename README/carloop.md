# EdgeAuto-carloop
#### By Chad Brown

## Objective
A full functional component that supports CAN message and GPS data collection from a Car via Carloop and its associated GPS components

## Design Scheme
Collect data within the Particle Photon from the Carloop GPS and the Carloop Basic that’s attached to the OBD2 port of a vehicle. This data is printed to a serial port to verify data is being collected.

## Hardware
### Carloop basic
https://store.carloop.io/products/carloop-basic

Retrieves CAN messages through a vehicles OBD2 port.

### Carloop GPS
https://store.carloop.io/products/carloop-gps?variant=4846877966372

Obtains GPS coordinates of the carloop in real-time.

### Particle Photon
https://store.particle.io/products/photon

Allows code to be added to it through the Particle IDE. Photon code controls gathering the CAN message and GPS data.

## Software
### Particle IDE
https://build.particle.io


IDE that uses c++ to add functionality to the Particle Photon and associated components.			

## Configuration
Setup Particle Photon (https://docs.particle.io/quickstart/photon/)

Enter the IDE.

Create a new app and add Carloop library to it.

Use Carloop library objects (carloop) and functions (.gps() and .can()) to retrieve CAN and GPS information. 
(https://docs.particle.io/reference/device-os/firmware/photon/)

Print information to serial port or publish it to the particle console to confirm reception.	

## License

There is none. If for some unlikely reason you want to use anything here, you can do so without my permission. I grant thee the privilege.
