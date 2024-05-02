The Universal Reader Assistant is a great way to start taking advantage of the full capabilities of the M7E-Hecto. Unfortunately, it's only available for Windows.

## Download & Install

Start by downloading the Universal Reader Assistant (URA). 32-bit and 64-bit versions are available.

<center>
[Universal Reader Assistant Download](https://www.jadaktech.com/product/thingmagic-universal-reader-assistant/){ .md-button .md-button--primary }
</center>

Open the installer once downloading finishes and follow the installation wizard instructions.

## Universal Reader Assistant Setup Wizard

Make sure the Simultaneous RFID Reader is plugged in either over USB or through the Serial Header to a USB-to-Serial converter with the UART selection switch in the correct position, and open the Universal Reader Assistant. You should be greeted by the Connection Wizard menu to select the reader type and port:

<figure markdown>
[![Photo of URA Connection Wizard.](./assets/img/URA-Port_Selection.jpg){ width="600}](./assets/img/URA-Port_Selection.jpg "Click to enlarge")
</figure>

You can skip this selection and move on to the main menu of the Universal Reader Assistant. Otherwise, select the port your Simultaneous RFID Reader is on and click "Next" and the Connection Wizard should show you the RFID reader settings:

<figure markdown>
[![Photo showing connection settings with M7E selected.](./assets/img/URA-M7E_Selected.jpg){ width="600"}](./assets/img/URA-M7E_Selected.jpg "Click to enlarge")
</figure>

Click either "Connect & Read" or "Connect" to open up the Universal Reader Assistant main window.

## Universal Reader Assistant Main Window

The main window of the Universal Reader Assistant contains a whole bunch of settings and status menus to adjust everything from the M7E's read/write options, power level and even perform firmware updates. It also has a handy readout for the M7E's internal temperature along with multiple tabs for interacting with tags the M7E sees including simple tag data, writing to the user memory and also locking a tag with a custom password.

There are a ton of features to the M7E from ThingMagic. Poke around the Universal Reader Assistant to learn more. *Write EPC* and *User Memory* are two of the most commonly used tabs.

!!! info
    <b>Note:</b> The ‘Transport Logging’ checkbox is very handy. Select this box and all the serial communication will be recorded to a log file. These HEX bytes can be deciphered and recreated using an Arduino or other microcontroller if you need a particular capability or feature that is not supported in the SparkFun Simultaneous RFID Reader Arduino library.

### Thermal Throttling

If you see this window pop up it means the module is reporting a temperature-limit fault condition. The module has an internal temperature sensor and will protect itself from permanent damage. You’ll need to lower your read power or add heatsinking. See the previous section of this guide, Thermal Considerations, for more information.