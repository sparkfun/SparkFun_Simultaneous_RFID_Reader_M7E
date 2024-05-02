## Power Supply

Make sure your selected power supply can source enough current to power the Simultaneous RFID Reader - M7E to avoid brown outs as the board can draw over <b>720mA @5V</b> when read power is maxed out. Refer to page 29, "DC Power Requirements" of the [M7E Hecto Design Guide](./assets/component_documentation/M7E_HECTO_User_Guide.pdf) for a detailed chart of current draw at various input voltages and read power levels.

## Thermal Throttling

The M7E has built-in thermal protection that will throttle itself to prevent permanent damage from heat. This board has a thermal pad to help dissipate heat for some applications but if you plan to run the M7E at high read powers for extended periods of time (1hr +), we recommend attaching an external heat sink to the thermal pad.

You can also use the module's ability to change read duty cycle to reduce the heat dissipation as well. Check out the [M7E Hecto Design Guide](./assets/component_documentation/M7E_HECTO_User_Guide.pdf) for more information.

## Logic Levels

Reminder, the Simultaneous RFID Reader M7E 3.3V operates at <b>3.3V</b> logic. Make sure any devices (development board or serial converter) connected to the serial interface operate at <b>3.3V</b> logic or are properly [shifted](https://learn.sparkfun.com/tutorials/logic-levels) to avoid damaging the M7E Hecto.

## Range Discrepancies

The functional range of the Simultaneous RFID Reader - M7E depends on a wide variety of factors and any one of these can increase or decrease the range at which tags are read. Make sure the antenna (either PCB or external) is free of anything that may cause interference. For example, the PCB antenna's range can drastically change depending on whether it is in open space or next to a solid object (such as a desk or person). Similarly, a tag's position in relation to the antenna as well as any solid objects (again, think person or other object) it may be near or placed on can significantly change the range.

For ideal range, make sure both the antenna and tag are in as much open space as possible and positioned in line with the antenna's radiation pattern.

## General Troubleshooting and Technical Assistance

If you need technical assistance and more information on a product that is not working as you expected, we recommend heading on over to the [SparkFun Technical Assistance](https://www.sparkfun.com/technical_assistance) page for some initial troubleshooting.

<center>
[SparkFun Technical Assistance Page](https://www.sparkfun.com/technical_assistance){ .md-button .md-button--primary }
</center>

If you don't find what you need there, the [SparkFun Forums](https://forum.sparkfun.com/index.php) are a great place to find and ask for help. If this is your first visit, you'll need to [create a Forum Account](https://forum.sparkfun.com/ucp.php?mode=register) to search product forums and post questions.<br /><br />

<center>
[Create New Forum Account](https://forum.sparkfun.com/ucp.php?mode=register){ .md-button .md-button--primary }
</center>

<center>
[Log Into SparkFun Forums](https://forum.sparkfun.com/index.php){ .md-button .md-button--primary }
</center>


