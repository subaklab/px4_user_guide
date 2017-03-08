---
Author: HamishWillee
Status: draft
---

# Pixhawk Mini Wiring Quick Start

> **Warning** Under construction.

This quick start guide shows how power the [Pixhawk Mini](pixhawk_mini.md)
and connect its most important peripherals.

## Standard Wiring Chart

The image below shows standard Quadcopter wiring using the *Pixhawk Mini
Kit* and 3DR Telemetry Radios (along with ESC, motor, battery and a
ground control station running on a phone. We'll go through each main
part in the following sections.

![Pixhawk Mini Electronics Wiring for QAV250 (off frame)](../../images/qav250_wiring_image_pixhawk_mini.jpg)
 

## Mount and Orient Controller

The *Pixhawk Mini* should be mounted on the frame using
vibration-damping foam pads (included in the kit). It should be
positioned as close to your vehicle’s center of gravity as possible .

The controller should be placed on the frame top-side up, oriented so
that the arrow points towards the front of the vehicle.

![Pixhawk Mini recommended orientation](../../images/pixhawk_mini_mounting_arrow.png)
![Mounting foam](../../images/3dr_anti_vibration_mounting_foam.png)

> **Note** If the controller cannot be mounted in the
  recommended/default orientation (e.g. due to space constraints) you will
  need to configure the autopilot software with the orientation that you
  actually used: LINK TO: Flight Controller Orientation.

## GPS + Compass

Attach the 3DR GPS + Compass to the Pixhawk Mini's **GPS&I2C** port (top
right) using the supplied 6 pin cable. The GPS/Compass should be mounted
on the frame as far away from other electronics as possible, facing the
front of the vehicle (separating the compass from other electronics will
reduce interference).

![Connecting compass/GPS to Pixhawk Mini](../../images/pixhawk_mini_with_compass.jpg)

NOTE - INSERT IMAGE SHOWING BOTH PORTS? OR FRONT-FACING image of GPS&I2C

[IN CALIBRATION, IS ORIENTATION TO VEHICLE FRONT or RELATIVE TO
PIXHAWK?]

The compass must be calibrated before it is first used. For more
information see: [COMPASS CALIBRATION LINK]

## Power

The image below shows typical power-supply wiring when using *Pixhawk
Mini* in a Quadcopter. This uses the *Quad Power Distribution
Board* that comes in the kit to supply both the Pixhawk Mini and the
ESC/Motor from the battery (and can also power other accessories).

> **Note** The *Quad Power Distribution Board* includes a power
  module (PM) that is suitable for batteries <= 4S. 
  The [3DR 10S Power Module](https://store.3dr.com/products/10s-power-module) 
  is recommended if you need more power.

[PLACHOLDER IMAGE - need more detail and consistent name for power
board]

![Pixhawk Mini - Powering](../../images/pixhawk_mini_powering_quad_board.jpg)

The *Pixhawk Mini* is powered through the **PM** port. When using a
power module (as in this case) the port will also read analog voltage
and current measurements.

Up to 4 ESCs can be separately powered from the power distribution board
(though in this case we only have one connected).

The control signals come from MAIN OUT. In this case there is only one
control channel, which is connected to the ESC via the *8 Channel PWM
Breakout Board*.

The Pixhawk Mini output rail (MAIN OUT) cannot power attached devices
(and does not need to in the circuit as shown). For vehicles where MAIN
OUT is attached to devices that draw power (e.g. a servo used in a
plane) then you will need to power the rail using a BEC (battery
elimination circuit). The included breakout board allows one channel to
provide power on the other outputs. [Show a diagram of this?]


## Radio/Remote Control

Pixhawk Mini supports many different radio receiver models:

- PPM and S.BUS receivers must connect to the **RCIN** port.
  ![Pixhawk Mini - Radio port for PPM receivers](../../images/pixhawk_mini_port_rcin.png)
- PWM receivers (with individual cables for each channel) must connect
  to the RCIN channel *via* a PPM encoder 
  [like this one](http://www.getfpv.com/radios/radio-accessories/holybro-ppm-encoder-module.html).
- Spektrum and DSM receivers must connect to the **SPKT/DSM** input.
  ![Pixhawk Mini - Radio port for Spektrum receivers](../../images/pixhawk_mini_port_spkt_dsm.png)

*PX4* and *Pixhawk Mini* is have been validated with:

- All Spektrum DSM RC receivers
- All Futaba S.BUS and S.BUS2 RC receivers
- All FrSky PPM and S.Bus models
- Graupner HoTT
- All PPM models from other manufacturers

> **Note** ADD SOMETHING ON BINDING TO RECIEVER TO BIND
> **Note** ADD SOMETHING ON DIFFERENT TRANSMITTERS. We PERHAPS NEED A COMPATIBILITY PAGE  

## Safety switch (optional)

The controller has an integrated safety switch that you can use for
motor activation once the autopilot is ready to take off. If this switch
is hard to access on a particular vehicle you can attach the (optional)
external safety button, as shown below.

![Pixhawk Mini - Optional Switch](../../images/pixhawk_mini_safety_switch_wiring.jpg) 

[IMAGE PLACEHOLDER - GOOD IMAGE of SIDE PORTS + CONNECTED SWITCH]

## Motors

![Pixhawk Mini - port for motors/servos](../../images/pixhawk_mini_port_main_out.png)


### Copter

### Plane

### VTOL



## Telemetry Radios


## Other Peripherals

 

## Configuring Pixhawk

GENERAL CONFIG INSTRUCTIONS - LINK TO [Autopilot Configuration](../config/autopilot_configuration.md)

## Further information

- - [Pixhawk Mini Quick Start Guide (3DR)](https://3drobotics.zendesk.com/hc/en-us/article_attachments/115000349564/PixhawkMiniQuickStartGuide.pdf)

 

