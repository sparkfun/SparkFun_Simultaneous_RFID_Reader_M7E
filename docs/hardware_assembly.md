In this section we'll cover the two ways to set up the Simultaneous RFID Reader - M7E Nano 3.3V. 

### Communicating via USB-C Serial

The fastest and easiest way to start using the board is through the USB-C connector. Simply plug the board into a computer with a USB-C cable and open up the Universal Reader Assistant.



Reminder, most computer USB ports can only supply <b>~500mA @5V</b> which limits the power level settings to roughly 20dBm and lower. If you intend to run the M7E at higher power levels, a dedicated power supply is necessary.

### Communicating via Serial PTH Header

Users who prefer to communicate with the RFID reader using the Serial PTH header should solder either wires or header pins to connect them to a <b>3.3V</b> microcontroller (you can also use this to connect to a USB UART board like the [Serial Basic](https://www.sparkfun.com/products/15096)). If you are not familiar with through-hole soldering or would like a refresher, take a read through [this tutorial](https://learn.sparkfun.com/tutorials/how-to-solder-through-hole-soldering).



We'll demonstrate soldering male headers to the board and use jumper wires to connect the RFID Reader to the [SparkFun IoT RedBoard - ESP32](https://www.sparkfun.com/products/19177) for use with the [SparkFun Simultaneous RFID Tag Reader Arduino Library](https://github.com/sparkfun/SparkFun_Simultaneous_RFID_Tag_Reader_Library).


<table class="table table-striped table-hover table-bordered">
    <tr>
        <th class="text-center" colspan="2">Connection Table</th>
    </tr>
    <tr>
        <th class="text-center">RFID Reader</th>
        <th class="text-center">RedBoard IoT</th>
    </tr>
    <tr align="center">
        <td>RX</td>
        <td>TX / D2 <sup><a href="#M7ENano_Note1">[1]</a></sup></td>
    </tr>
    <tr align="center">
        <td>TX</td>
        <td>RX / D3 <sup><a href="#M7ENano_Note1">[1]</a></sup></td>
    </tr>
    <tr align="center">
        <td>VIN <sup><a href="M7ENano_Note2">[2]</a></sup></td>
        <td>5V</td>
    </tr>
    <tr align="center">
        <td>Ground</td>
        <td>Ground</td>
    </tr>
</table>

<div class="alert alert-info">
    <a name="M7ENano_Note1"></a><a href="https://learn.sparkfun.com/tutorials/simultaneous-rfid-reader---M7E-nano-33v-hookup-guide#M7ENano_Note1"><b>1:</b></a> Digital pin values are the default selections for Software Serial in the <a href="https://github.com/sparkfun/SparkFun_Simultaneous_RFID_Tag_Reader_Library">Simulataneous RFID Reader Arduino Library</a> and may be incompatible with your selected microcontroller. Refer to the <a href="https://docs.arduino.cc/learn/built-in-libraries/software-serial#limitations-of-this-library">Arduino Software Serial Reference</a> for pin limitations for common microcontrollers.
</div>

<div class="alert alert-danger">
    <a name="M7ENano_Note2"></a><a href="https://learn.sparkfun.com/tutorials/simultaneous-rfid-reader---M7E-nano-33v-hookup-guide#M7ENano_Note2"><b>2:</b></a> We strongly recommend opening the <b>VIN</b> jumper on the Simultaneous RFID Reader - M7E Nano 3.3V when connecting the <b>VIN</b> PTH pin to an external power source. When the <b>VIN</b> jumper is closed <b>VIN</b> is netted with <b>V_USB</b> (as well as <b>VCC</b>).
</div>

#### Power Supply Considerations

When connecting the Simultaneous RFID Reader - M7E Nano 3.3V to a microcontroller, make sure your power supply can source sufficient current for your selected power level as the board can draw up to <b>720mA @5V</b> at max read power level. The M7E's internal voltage regulator includes built-in protection that engages when the current draw reaches <b>1A</b> and will not allow any more supply current to the module. As such, it is strongly recommended to use a <b>5V</b> power supply when setting the read power to above +26 dBm.

If you opt to power the RFID Reader from your development board's output voltage we recommend using the <b>5V</b> out (if applicable) and then powering your development board through a dedicated power supply to avoid browning the circuit out as USB ports can only source <b>~500mA@5V</b>. The image below shows the Simultaneous RFID Reader - M7E Nano 3.3V connected to the RedBoard IoT and powered with a dedicated power supply through the barrel jack.
