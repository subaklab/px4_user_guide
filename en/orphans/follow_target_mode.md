# Follow Me Mode

Follow me mode allows a multicopter to autonomously follow and track a
user via an Android device using QGroundcontrol.  While in this mode no
user input is required.

**Quick Start**

An OTG capable Android device is required.  This along with an SiK
telemetry radio connected to the multicopter and your Android device
allows the positioning information to be relayed between them.

When follow me mode is activated the multicopter will ascend to the
minimum height of 8 meters, pause for a moment and start following your
movements.

A demonstration of the follow me mode can be seen here:

https://www.youtube.com/watch?v=RxDL4CtkzAQ

------------------------------------------------------------------------

**Precautions To Be Aware Of**

***Since follow me mode does not implement any type of obstacle
avoidance,** **special care must be taken when this mode is used, the
following flight precautions should be observed.***

-   Follow me mode should only be used in wide open areas that are
    unobstructed by trees, power lines, houses, ect.  The default height
    that the multicopter is set to follow relative to the home and
    arming position is 8 meters. (about 26 feet) Be sure to set this
    height to a value well above any surrounding obstructions.
-   Although follow me mode implements auto take off, it is safer to fly
    to a default height of 8 meters in a manual control mode rather than
    switching to follow me mode while landed.
-   In general most Android devices do not update their position very
    frequently.  To overcome this problem the autopilot will try and
    estimate the speed and direction of the target in between updates
    received by the device. Given this fact be sure to give your
    multicopter plenty of room to stop. The faster you are going the
    larger a distance it will take the multicopter to stop and keep pace
    with the you and your Android device.
-   The accuracy of positioning is dependent on the quality of the GPS
    chip set used by the Android device.  If the chip set is not
    accurate, this will be reflected in follow me. When using follow me
    mode for the first time, be ready to take control with with an RC in
    case something goes wrong.

**Known Issues**

The SiK 915 Mhz radio is known to interfere with the GPS signal being
received by an Android device.  Be sure to keep the radio and Android
device as far apart as possible when using the follow target mode to
avoid interference.

It is important that you set your Android device to not go to sleep as
this could cause the GPS signal to cease being emitted at regular
intervals to the UAV.

This can be found under settings-\>display

It is important to set your android location mode to "Device Only".  As
high accuracy mode has been observed to give a slower overall device
position change.

This can be found under settings-\>location-\>location mode

**Verified Android Devices**

Nexus 5

Nexus 7 Tablet

