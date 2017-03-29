# Standard Plane Connections

This document shows the flight controller connections for a standard plane (a standard plane is a plane with aileron, elevator, rudder and throttle).

## Pixhawk Connections

Port | Rate | Actuator
--- | --- | ---
MAIN 1 | 50 Hz | Aileron (assuming a Y cable)
MAIN 2 | 50 Hz | Elevator
MAIN 3 | 50 Hz | Throttle
MAIN 4 | 50 Hz | Rudder

> **Caution** It is assumed that you will supply to the power rail (in order to power the servos for aileron, elevtor, rudder). Typically your throttle motor uses an ESC with an
  integrated BEC so that power is supplied to the Pixhawk from MAIN3. If not, you will need to setup a 5V BEC to connect to one of the free Pixhawk ports.                           

