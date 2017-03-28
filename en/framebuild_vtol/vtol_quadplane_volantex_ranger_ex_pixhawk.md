# Volantex Ranger-Ex QuadPlane VTOL (Pixhawk)

The QuadRanger is a VTOL conversion of the Volantex Ranger-Ex. It's a
1980mm wingspan plane that is capable of vertical takeoff and land.

![QuadRanger](../../images/quadranger_vtol_complete_build.jpg)


## Conversion kit

-   The basic parts required are;
-   Pixhawk or compatible
-   Digital airspeed sensor
-   3DR Power module or compatible
-   GPS

For a full parts list with links to Hobbyking EU and International
warehouse see:
[QuadRanger-VTOL-partslist](http://px4.io/wp-content/uploads/2016/01/QuadRanger-VTOL-partslist-1.xlsx)

The image below depicts the parts required for one wing.

![QuadRanger
Parts](../../images/quadranger_vtol_parts_for_one_wing.jpg)

 
The tools required for the conversion are;

-   A Dremel or similar rotary tool
-   A hobby knife
-   UHU POR glue
-   CA glue
-   Tape-line
-   Tape

![QuadRanger conversion tools](../../images/quadranger_vtol_conversion_tools.jpg)

## Wing conversion

A full build log is provided in the following video.

> **Success** Please note that the conversion in this build
  log is performed on a wing that shows damage from a previous conversion. 
  
{% youtube %}
https://www.youtube.com/embed/l_ppJ_HhAUQ
{% endyoutube %}

Cut both 800mm square carbon tubes to a length of 570mm and 230mm.

Making a slot in the Styrofoam wing 1.5cm deep using a rotary tool with
some form of guidance to keep a fixed depth. The slot should be the
length, depth and width of one 230mm square carbon tube. It should be
located as indicated below.

![QuadRanger carbon tube slot](../../images/quadranger_vtol_carbon_tube_slot.jpg)

Glue the 300x150x1.5mm carbon sheet to the 230mm carbon tube using CA
glue and create an opening to run wires through. Insert the wires for
power and signal to the ESC's. Using UHU POR glue the sheet and carbon
tube to the Styrofoam wing as indicated below.

![QuadRanger sheet attachment](../../images/quadranger_vtol_sheet_attachment.jpg)

Using CA glue, glue the 570mm square carbon tube to the carbon sheet. It
should be located 285mm from where the wings join. The tube should be
centred relative to the vertical area of the wing. It should extend
exactly 165mm on both sides.

Attach the motor mount to the motor. With another motor mount plate and
4 M3x25mm screws clamp the motor on the end of the square carbon tube as
indicated below. Attach the ESC's with tie wraps to the carbon tube.
When using the Afro ESC be sure to connect at least signal and ground
wire.

![QuadRanger motor and esc](../../images/quadranger_vtol_motor_and_esc.jpg)

## Wiring 

The outputs of Pixhawk should be wired like this (orientation as seen
like "sitting in the plane").

-   MAIN1: Front right motor, CCW
-   MAIN2: Back left motor, CCW
-   MAIN3: Front left motor, CW
-   MAIN4: Back right motor, CW
-   AUX1: Left aileron
-   AUX2: Right aileron
-   AUX3: Elevator
-   AUX4: Rudder
-   AUX5: Throttle

> **Success** The servo direction can be reversed using the
  PWM\_REV parameters in the PWM\_OUTPUT group of QGroundControl (cogwheel
  tab, last item in the left menu)
  
For further instructions on wiring and configurations please see: 
[Standard VTOL Wiring and Configuration](../config/standard_configuration_vtol_quad.md)


## Configuration

Configure the frame as shown in QGroundControl below (do not forget to
click **Apply and Restart** in the top).

![QGC - select firmware for standard VTOL](../../images/qgc_firmware_standard_vtol_fun_cub_quad.png)


## Support

If you have any questions regarding your VTOL conversion or configuration please visit <http://discuss.px4.io/c/vtol>.

 
