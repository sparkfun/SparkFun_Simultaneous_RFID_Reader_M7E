

## UART Switch Position & Software Serial

Make sure the Serial Selection Switch is in the <b>"SER"</b> position when using this library. All of the examples in this Arduino library use the [Software Serial Library](https://docs.arduino.cc/learn/built-in-libraries/software-serial/) so if you are not using the SparkFun RedBoard IoT and following the assembly instructions in the Hardware Assembly section, make sure to connect the RX/TX pins on the SER header to compatible pins on your chosen development board. Note, this library 

## Code to Note

The latest version of the Simultaneous RFID Reader Library has a couple of settings to take note of and adjust accordingly depending on your hardware and setup.

### Serial Selection (Software vs Hardware)

If you're using a development board that supports [Software Serial](https://docs.arduino.cc/learn/built-in-libraries/software-serial/), uncomment the following lines and adjust the pins for RX/TX if necessary:

``` c++
#include <SoftwareSerial.h>
SoftwareSerial softSerial(2, 3); //RX, TX
```

The next option selects which type of serial is used. The code lists a couple of examples for both software serial and hardware so adjust the definition as needed. For example, if you're using a software serial library, define this as `softserial`. If you're using a hardware serial port on your development board, select the serial port (eg. Serial1) as shown below: 

``` c++
// #define rfidSerial softSerial // Software serial (eg. Arudino Uno or SparkFun RedBoard)
#define rfidSerial Serial1 // Hardware serial (eg. ESP32 or Teensy)
```

### Baud Rate Selection

Next, you'll want to define the baud rate for `rfidBaud`. We recommend setting it to 38400 like shown below when using software serial and 115200 when using hardware serial:

``` c++
// #define rfidBaud 38400
#define rfidBaud 115200
```

### Module Selection

Since this library supports both the M6E Nano and M7E Hecto, you'll need to define which module you are using. Adjust or comment/uncomment the `moduleType` definition to set it to the correct module:

``` c++
// #define moduleType ThingMagic_M6E_NANO
#define moduleType ThingMagic_M7E_HECTO
```

## Example 1 - Constant Read

The first example sets the M7E to constantly scan and report any tags it sees in the vicinity. Open the example by navigating to **File > Examples > SparkFun Simultaneous RFID Reader Library > Example 1 Constant Read**. Select your Board and Port and click the "Upload" button. Once the code finishes uploading, open the [serial monitor](https://learn.sparkfun.com/tutorials/terminal-basics/arduino-serial-monitor-windows-mac-linux) with the baud set to **115200**. The code attempts to set up the module with the defined baud rate and if that fails, it prints "Module failed to respond. Please check wiring" If you see this prompt, double-check your connections to your development board and retry. On successful module startup and setup, the code prints "Press a key to begin scanning for tags." Send any key message and the M7E will begin to scan for any tags in range and print out their EPC as the screenshot below shows:


