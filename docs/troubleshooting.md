
### Power Supply

Make sure your selected power supply can source enough current to power the Simultaneous RFID Reader 3.3V to avoid brown outs as the board can draw over <b>720mA @5V</b> when read power is maxed out. Refer to page 29, "DC Power Requirements" of the [M7E Nano Design Guide](https://cdn.sparkfun.com/datasheets/Sensors/ID/Nano_Design_Guide_rev01E.pdf) for a detailed chart of current draw at various input voltages and read power levels.

### Thermal Throttling

The M7E Nano has built-in thermal protection that will throttle itself to prevent permanent damage from heat. This board has a thermal pad to help dissipate heat for some applications but if you plan to run the M7E Nano at high read powers for extended periods of time (1hr +), we recommend attaching an external heat sink to the thermal pad.

You can also use the module's ability to change read duty cycle to reduce the heat dissipation as well. Check out the [M7E Nano Design Guide](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Nano_Design_Guide_rev01E.pdf) for more information.

### Logic Levels

Reminder, the Simultaneous RFID Reader 3.3V operates at <b>3.3V</b> logic. Make sure any devices (development board or serial converter) connected to the serial interface operate at <b>3.3V</b> logic or are properly [shifted](https://learn.sparkfun.com/tutorials/logic-levels) to avoid damaging the M7E Nano.

### General Troubleshooting and Technical Assistance

<div class="alert alert-info" role="alert">
    <span class="glyphicon glyphicon-question-sign" aria-hidden="true"></span>
    <strong> Not working as expected and need help? </strong> 
    <br>
    <br>

    If you need technical assistance and more information on a product that is not working as you expected, we recommend heading on over to the <a href="https://www.sparkfun.com/technical_assistance">SparkFun Technical Assistance</a> page for some initial troubleshooting. <br /><br />
   
    -> <!-- button(SparkFun Technical Assistance Page, https://www.sparkfun.com/technical_assistance) --> <-
    <br>
   
    If you don't find what you need there, the <a href="https://forum.sparkfun.com/index.php">SparkFun Forums</a> are a great place to find and ask for help. If this is your first visit, you'll need to <a href="https://forum.sparkfun.com/ucp.php?mode=register">create a Forum Account</a> to search product forums and post questions.<br /><br />
   
    <div class="text-center"><!-- button(Create New Forum Account, https://forum.sparkfun.com/ucp.php?mode=register) -->&nbsp;&nbsp;&nbsp;<a class="btn btn-danger" href="https://forum.sparkfun.com/index.php" role="button">Log Into SparkFun Forums</a></div>

</div>