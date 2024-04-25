---
icon: material/book-open-page-variant
---

<div class="grid cards desc" markdown>

-   <a href="https://www.sparkfun.com/products/22925">
    **SparkFun Simultaneous RFID Reader - M7E Hecto**<br>
    **SKU:** DEV-22925

    ---

    <figure markdown>
    ![SparkFun Simultaneous RFID Reader - M7E Hecto](https://cdn.sparkfun.com/r/600-600/assets/parts/2/5/0/6/2/WRL-24738-Simultaneous-RFID-Reader-Feature.jpg)
    </figure></a>

-   The M7E Hecto is a Ultra-High Frequency (UHF) RFID reader from JADAK<sup>&copy;</sup> capable of reading multiple tags simultaneously at up to 150 tags per second and can also write data to tags. The M7E Nano can read tags from several feet away (up to 16 feet in our testing!) with the proper antenna, conditions and device settings. This board includes a USB-C connector and CH340C USB to UART converter to quickly connect the board to a computer and read tags with no soldering required.

    Along with the USB-C connector, the Simultaneous RFID Reader 3.3V has a 0.1"-spaced PTH header for connecting it to an external converter or to a 3.3V microcontroller of your choice to use it with the SparkFun Simultaneous RFID Tag Reader Library. A 2-way switch on the board allows for easy switching between the included communication interfaces.

    <center>
    [Purchase from SparkFun :fontawesome-solid-cart-plus:](https://www.sparkfun.com/products/22925){ .md-button .md-button--primary }
    </center>

</div>

In this guide we'll cover everything you need to set up this RFID reader and use it with the Universal Reader Assistant application to read and write to UHF tags. We'll also cover how to set this board up in a circuit with a 3.3V microcontroller and point you to where you can get started using the SparkFun Simultaneous RFID Tag Reader Arduino Library.

### Required Materials

We designed this version of the Simultaneous RFID Reader to work over either USB-C or a serial plated through-hole (PTH) connection so depending on your application, you may need different materials. 

#### USB Connection

The quickest way to get the RFID Reader up and running is through the USB-C connector. If you opt for this you'll need a USB-C cable like the ones below:

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/14743">

    <figure markdown>
    ![USB 3.1 Cable A to C - 3 Foot](https://cdn.sparkfun.com//assets/parts/1/2/9/7/2/14743-USB_3.1_Cable_A_to_C_-_3_Foot-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/14743">
    **USB 3.1 Cable A to C - 3 Foot**<br>
    CAB-14743
    </a>

-   <a href="https://www.sparkfun.com/products/15424">
    
    <figure markdown>
    ![Reversible USB A to C Cable - 2m](https://cdn.sparkfun.com//assets/parts/1/3/9/8/3/15424-Reversible_USB_A_to_C_Cable_-_2m-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/15424">
    **Reversible USB A to C Cable - 2m**<br>
    CAB-15424
    </a>

-   <a href="https://www.sparkfun.com/products/15425">

    <figure markdown>
    ![Reversible USB A to C Cable - 0.8m](https://cdn.sparkfun.com//assets/parts/1/3/9/8/4/15425-Reversible_USB_A_to_C_Cable_-_0.8m-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/15425">
    **Reversible USB A to C Cable - 0.8m**</br>
    CAB-15425
    </a>

-   <a href="https://www.sparkfun.com/products/15426">

    <figure markdown>
    ![Reversible USB A to C Cable - 0.3m](https://cdn.sparkfun.com//assets/parts/1/3/9/8/5/15426-Reversible_USB_A_to_C_Cable_-_0.3m-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/15426">
    **Reversible USB A to C Cable - 0.3m**<br>
    CAB-15426
    </a>

</div>

#### PTH Serial Connection

Users who prefer to use the PTH headers to connect to a serial converter or microcontroller will want to solder either wire or a set of header pins to the board to make connections to the external device. If you don't have wire, header pins or soldering tools you may want to add the products below to your cart:

!!! warning "Logic Levels"
    <b>Note:</b> The serial output on the Simultaneous RFID Reader - M7E  operates at <b>3.3V logic</b> so make sure the microcontroller or serial converter connected to this interface operates at <b>3.3V</b> or are properly level-shifted.

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/15096">

    <figure markdown>
    ![SparkFun Serial Basic Breakout - CH340C and USB-C](https://cdn.sparkfun.com//assets/parts/1/3/4/5/2/15096-SparkFun_Serial_Basic_Breakout_-_CH340C_and_USB-C-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/15096">
    **SparkFun Serial Basic Breakout - CH340C and USB-C**<br>
    DEV-15096
    </a>

-   <a href="https://www.sparkfun.com/products/9873">

    <figure markdown>
    ![SparkFun FTDI Basic Breakout - 3.3V](https://cdn.sparkfun.com//assets/parts/3/9/5/8/09873-01a.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/9873">
    **SparkFun FTDI Basic Breakout - 3.3V**<br>
    DEV-09873
    </a>

-   <a href="https://www.sparkfun.com/products/19177">

    <figure markdown>
    ![SparkFun IoT RedBoard - ESP32 Development Board](https://cdn.sparkfun.com//assets/parts/1/8/8/0/0/ESP32_03.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/19177">
    **SparkFun IoT RedBoard - ESP32 Development Board**<br>
    DEV-19177
    </a>

-   <a href="https://www.sparkfun.com/products/15444">

    <figure markdown>
    ![SparkFun RedBoard Artemis](https://cdn.sparkfun.com//assets/parts/1/4/0/1/9/15444-SparkFun_RedBoard_Artemis-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/15444">
    **SparkFun RedBoard Artemis**<br>
    DEV-15444
    </a>

-   <a href="https://www.sparkfun.com/products/14456">

    <figure markdown>
    ![Soldering Iron - 60W (Adjustable Temperature)](https://cdn.sparkfun.com//assets/parts/1/2/4/9/0/14456-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/14456">
    **Soldering Iron - 60W (Adjustable Temperature)**<br>
    TOL-14456
    </a>

-   <a href="https://www.sparkfun.com/products/9325">

    <figure markdown>
    ![Solder Lead Free - 100-gram Spool](https://cdn.sparkfun.com//assets/parts/2/8/7/3/09325_9161-Solder_Lead_Free_-_100-gram_Spool-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/9325">
    **Solder Lead Free - 100-gram Spool**<br>
    TOL-09325
    </a>

-   <a href="https://www.sparkfun.com/products/11375">

    <figure markdown>
    ![Hook-Up Wire - Assortment (Stranded, 22 AWG)](https://cdn.sparkfun.com//assets/parts/7/1/2/0/11375-Hook-Up_Wire_-_Assortment__Solid_Core__22_AWG_-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/11375">
    **Hook-Up Wire - Assortment (Stranded, 22 AWG)**<br>
    PRT-11375
    </a>

-   <a href="https://www.sparkfun.com/products/553">

    <figure markdown>
    ![Break Away Male Headers - Right Angle](https://cdn.sparkfun.com//assets/parts/3/7/8/00553-03-L.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/553">
    **Break Away Male Headers - Right Angle**<br>
    SKU
    </a>

</div>

#### Additional Materials

You'll also need UHF RFID tags for the M7E Nano to read/write. For best range performance you'll need an external antenna along with the appropriate adapter cables. We'll demonstrate how to connect the external antenna using the cables listed below:

<div class="grid cards" markdown>

-   <a href="https://www.sparkfun.com/products/14131">

    <figure markdown>
    ![UHF RFID Antenna (RP-TNC)](https://cdn.sparkfun.com//assets/parts/1/2/0/2/8/14131-02a.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/14131">
    **UHF RFID Antenna (RP-TNC)**<br>
    WRL-14131
    </a>

-   <a href="https://www.sparkfun.com/products/18569">

    <figure markdown>
    ![RP-SMA to U.FL Cable - 150mm](https://cdn.sparkfun.com//assets/parts/1/8/0/3/0/18569-RP-SMA_to_U.FL_Cable_-_150mm-01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/18569">
    **RP-SMA to U.FL Cable - 150mm**<br>
    WRL-18569
    </a>

-   <a href="https://www.sparkfun.com/products/20228">

    <figure markdown>
    ![UHF RFID Tags - Adhesive (5 Pack)](https://cdn.sparkfun.com//assets/parts/2/0/0/3/2/TagStrip_01.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/20228">
    **UHF RFID Tags - Adhesive (5 Pack)**<br>
    WRL-20228
    </a>

-   <a href="https://www.sparkfun.com/products/14132">

    <figure markdown>
    ![Interface Cable for RP-TNC to RP-SMA - 1m](https://cdn.sparkfun.com//assets/parts/1/2/0/2/9/14132-01a.jpg)
    </figure>
    </a>
    ---
    <a href="https://www.sparkfun.com/products/14132">
    **Interface Cable for RP-TNC to RP-SMA - 1m**<br>
    CAB-14132
    </a>

</div>

### Suggested Reading

If you aren't familiar with the following concepts, we recommend reading through these tutorials before continuing with this guide.

<div class="grid cards hide col-4" markdown align="center">

-   <a href="https://learn.sparkfun.com/tutorials/8">
    <figure markdown>
    ![Serial Communication](https://cdn.sparkfun.com/c/264-148/assets/7/d/f/9/9/50d24be7ce395f1f6c000000.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/8">**Serial Communication**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/62">
    <figure markdown>
    ![Logic Levels](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/2/Input_Output_Logic_Level_Tolerances_tutorial_tile.png)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/62">**Logic Levels**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/633">
    <figure markdown>
    ![RFID Basics](https://cdn.sparkfun.com/assets/learn_tutorials/6/3/3/RFID_Tag-104.png)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/633">**RFID Basics**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/61">
    <figure markdown>
    ![Installing Arduino IDE](https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/6/1/arduinoThumb.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/61">**Installing Arduino IDE**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/15">
    <figure markdown>
    ![Installing an Arduino Library](https://cdn.sparkfun.com/c/178-100/assets/b/e/4/b/2/50f04b99ce395fd95e000001.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/15">**Installing an Arduino Library**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/112">
    <figure markdown>
    ![Serial Terminal Basics](https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/1/1/2/terminalThumb.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/112">**Serial Terminal Basics**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/845">
    <figure markdown>
    ![Three Quick Tips About Using U.FL](https://cdn.sparkfun.com/assets/learn_tutorials/8/4/5/Connected.jpg)
    </a>
    <a href="https://learn.sparkfun.com/tutorials/845">**Three Quick Tips About Using U.FL**
    </a>

-   <a href="https://learn.sparkfun.com/tutorials/664">
    <figure markdown>
    ![How to Work with Jumper Pads and PCB Traces](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg)
    </figure>
    </a>
    <a href="https://learn.sparkfun.com/tutorials/664">**How to Work with Jumper Pads and PCB Traces**
    </a>
</div>