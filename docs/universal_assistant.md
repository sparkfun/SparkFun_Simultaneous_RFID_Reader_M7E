If you’re a Windows user the Universal Reader Assistant is a great way to get up and playing with the full capabilities of the M7E-NANO. The downside is that it’s only currently available for Windows.

Start by downloading the Universal Reader Assistant (URA). 32-bit and 64-bit versions are available.

-> <!-- button(Universal Reader Assistant Download, https://www.jadaktech.com/products/thingmagic-rfid/thingmagic-universal-reader-assistant/) --> <-

Once downloaded and installed, hover over the right side of the window. The *Setting/Status* control panel will open up. Click on the thumbtack icon to keep it open.

-> [![Opening communications tab in URA](https://cdn.sparkfun.com/r/600-600/assets/learn_tutorials/6/1/3/Opening_Comm_Sidebar.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Opening_Comm_Sidebar.jpg) <-

Expand the *Connect* menu and select `Serial Reader` and drop down the menu to select your COM port. Click `Connect`. The module will be pinged over the serial connection to verify its existence. 

-> [![Select the com port](https://cdn.sparkfun.com/r/600-600/assets/learn_tutorials/6/1/3/Starting_Communication_2.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Starting_Communication_2.jpg) <-

Next, select your `Region`. Since we are in North America, we've selected **NA2**.

-> [![Connecting to Serial Com Port](https://cdn.sparkfun.com/r/600-600/assets/learn_tutorials/6/1/3/Starting_Communication_-_2.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Starting_Communication_-_2.jpg) <-

<div class="alert alert-info"><b>Note:</b> The ‘Transport Logging’ checkbox is very handy. Select this box and all the serial communication will be recorded to a log file. These HEX bytes can be deciphered and recreated using an Arduino or other microcontroller if you need a particular capability or feature that is not supported in the SparkFun Simultaneous RFID Reader Arduino library.</div>

Next open the `Read/Write Options` and click on **1** under *Antennas*. 

-> [![Select the Antenna](https://cdn.sparkfun.com/r/600-600/assets/learn_tutorials/6/1/3/Starting_Communication_-_Antenna_Selection.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Starting_Communication_-_Antenna_Selection.jpg) <-

Finally, open the `Reader Power Settings` tab and select your Read Power. Tune this setting down to 5dBm. If you want to power the board from USB then use a power setting below 5dBm. 27dBm is ok to use only if you have external power (more than one USB port can provide). See the [Power Supply Considerations](https://learn.sparkfun.com/tutorials/simultaneous-rfid-reader-33v-hookup-guide/hardware-assembly) in the Hardware Assembly section for more information.

-> [![Power Setting Menu](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Starting_Communication_-_Power_Settings.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Starting_Communication_-_Power_Settings.jpg) <-

Now we’re ready to read! Click on the `Read` button at the top. Bring some RFID tags near the reader and you'll see them appear.

-> [![Continuously reading tags](https://cdn.sparkfun.com/r/600-600/assets/learn_tutorials/6/1/3/Continuous_Read.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Continuous_Read.jpg) <-

There are a ton of features to the Nano from ThingMagic. Poke around the Universal Reader Assistant to learn more. *Write EPC* and *User Memory* are two of the most commonly used tabs.

**Thermal Throttling:** If you see this window pop up it means the module is reporting a temperature-limit fault condition.

-> [![Thermal error window](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Temperature-Limit.jpg)](https://cdn.sparkfun.com/assets/learn_tutorials/6/1/3/Temperature-Limit.jpg) <-

The module has an internal temperature sensor and will protect itself from permanent damage. You’ll need to lower your read power or add heatsinking. See the previous section of this guide, [Thermal Considerations](https://learn.sparkfun.com/tutorials/simultaneous-rfid-reader-33v-hookup-guide/thermal-management-considerations), for more information.