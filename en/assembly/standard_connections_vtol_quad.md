# Standard VTOL Connections

This document shows the connections for a standard VTOL setup (also referred to as a QuadPlane). For airframe specific documentation and build instructions see [VTOL Framebuilds](./framebuild_vtol/README.md).

## Pixhawk Connections

Pixhawk Port | Connection
--- | ---
MAIN 1   | Quad motor 1
MAIN 2   | Quad motor 2
MAIN 3   | Quad motor 3
MAIN 4   | Quad motor 4
AUX 1    | Left aileron
AUX 2    | Right aileron
AUX 3    | Elevator
AUX 4    | Rudder
AUX 5    | Throttle (motor)


> **Caution** It is assumed that your pusher/puller motor uses an ESC with an
  integrated BEC which means power will be supplied to the Pixhawk on
  AUX5. If not, you will need to setup a 5V BEC to connect to one of the
  free Pixhawk ports. Failure to do so will result in nonfunctional servos.

## Configuration

* [VTOL Configuration](../config/vtol_quad_configuration.md)
* [VTOL Configuration (without an Airspeed Sensor)](../advanced_config/vtol_without_airspeed_sensor.md)

## Support

If you have any questions regarding your VTOL conversion or
configuration please visit <http://discuss.px4.io/c/vtol>.


 

