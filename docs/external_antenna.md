The integrated PCB antenna works well over short distances but users who want to get the maximum range for the M7E Nano will want to add an external antenna. Adding an external antenna does require a few considerations prior to connecting one. Let's take a quick look at these considerations. 

### FCC Regulations

From page 42 of the [Nano Design Guide](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Nano_Design_Guide_rev01E.pdf):

<blockquote>No additional transmitter-compliance testing is required if the module is operated with the same type of antenna as listed in the FCC filing as long as it has equal or lower gain than the antenna listed. Equivalent antennas must be of the same general type (e.g. dipole, circularly polarized patch, etc.), must be of equal or less gain than an antenna previously authorized under the same FCC ID, and must have similar in band and out of band characteristics (consult specification sheet for cut-off frequencies).</blockquote>

The board's PCB trace antenna is a patch antenna with much lower gain than the list of approved antennas which allows use of an unmodified board in the field without additional FCC testing.

The **u.FL connector** allows users to connect higher gain directional antennas. However, there are stipulations as to what external antennas can be used and **additional FCC certifications may be required**. 

<div class="alert alert-info">
    <b>Note:</b> The onboard PCB antenna complies with the FCC regulation.
</div>

The list below outlines antennas ThingMagic has tested and gotten approved by the FCC. You may use a different antenna from the ones in the list but it <b><i>must be of equal or less gain than an antenna previously authorized under the same FCC ID, and must have similar in band and out of band characteristics (consult specification sheet for cut-off frequencies)</i></b> if used in a product without additional testing.

-> [![Table of antennas](https://cdn.sparkfun.com/r/600-600/assets/learn_tutorials/6/1/3/List_of_Antennas.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/List_of_Antennas.jpg) <-

-> *List of approved antennas* <-

### Attaching the External Antenna

If you want to switch from the onboard antenna, you will need to change the position of the antenna jumper resistor to enable the u.FL connector.

 <div class="alert alert-info"><b>Note: </b> You do not need an external antenna for basic use of the Simultaneous RFID Reader - M7E Nano 3.3V but it's read range is limited to a few inches at the highest read power so users who want to take advantage of the full range need to modify the board to enable the u.FL connector for an external antenna. 
<br>
</br>
If you have never worked with solder jumpers before or would like some tips or a refresher, we highly recommend reading through this tutorial:
<!-- tutorial_big(664) -->
 </div>

Carefully reflow the 0k&ohm; RF resistor to move it to the u.FL position. You can either use a [soldering iron]() or [hot air rework station]() to reflow the solder holding the resistor into place.

<figure markdown>
[![Photo showing 0k ohm resistor adjusted to external antenna position.](./assets/img/Simultaneous_RFID_Reader_M7E-Antenna_Selection.jpg){ width="600"}](./assets/img/Simultaneous_RFID_Reader_M7E-Antenna_Selection.jpg "Click to enlarge")
</figure>

Next, attach the u.FL to the [RP-SMA connector cable](https://www.sparkfun.com/products/662). Because this connector is fragile we recommend either taping or hot gluing the sheath of the cable to the PCB. This will help prevent damage to the u.FL connector in case the cable gets pulled on.

<figure markdown>
[![Photo showing u.Fl cable secured with electrical tape.](./assets/img/Simultaneous_RFID_Reader_M7E-UFL.jpg){ width="600"}](./assets/img/Simultaneous_RFID_Reader_M7E-UFL.jpg "Click to enlarge")
</figure>

To get the best range we recommend attaching an external high-gain antenna to a tri-pod of some sort. If you only have a desk, that's ok too.

<figure markdown>
[![Photo showing external antenna mounted.](./assets/img/Simultaneous_RFID_Reader_M7E-Antenna_Mounted.jpg){ width="600"}](./assets/img/Simultaneous_RFID_Reader_M7E-Antenna_Mounted.jpg "Click to enlarge")
</figure>

We used the included hardware with the antenna to attach it to a leg of the tripod. 

**Photo of Antenna attached to tripod**

Now connect the RP-SMA to RP-TNC cable. And finally connect the RP-TNC to the external antenna. You can use a different UHF RFID antenna but you will need to have the correct connectors and cables to go from the u.FL connector on the board to the connector on your specific antenna.

<figure markdown>
[![Photo showing completed external antenna assembly](./assets/img/Simultaneous_RFID_Reader_M7E-Full_External_Antenna.jpg){ width="600"}](./assets/img/Simultaneous_RFID_Reader_M7E-Full_External_Antenna.jpg "Click to enlarge")
</figure>

-> *u.FL connector to RP-SMA to RP-TNC* <-


!!! warning

    <b>Don't Forget!</b> Ensure that personnel do not stand in the radiation beam of the antenna unless they are more than 21cm away from the face of the antenna (to adhere to FCC limits for long-term exposure). Refer to the <a href="https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Nano_Design_Guide_rev01E.pdf">M7E Nano design guide</a> for more information.
