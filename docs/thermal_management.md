---
icon: material/thermometer
---

The module can reach temperatures greater than 85&deg;C (185&deg;F) when operating at full read power over extended periods so thermal management is an important consideration using this board. 

The module will automatically throttle itself to prevent permanent damage from heat. This board provides enough ground plane heatsinking to allow the module to operate at full read power for tens of minutes before throttling occurs. If you plan to operate the module at full power for extended periods (over an hour) we recommend attaching a heatsink. 

You can get the 1:1 dimensional drawing of the board [here](https://cdn.sparkfun.com/assets/f/c/d/5/3/Simultaneous_RFID_Reader_3.3V-Dimensions1.png). The dimensional drawing below shows the exposed thermal pad and mounting holes. 

<figure markdown>
[![Board Dimensions](https://cdn.sparkfun.com/r/600-600/assets/f/c/d/5/3/Simultaneous_RFID_Reader_3.3V-Dimensions1.png){width="600"}](https://cdn.sparkfun.com/assets/f/c/d/5/3/Simultaneous_RFID_Reader_3.3V-Dimensions1.png "Click to enlarge")
<figcaption><i>Dimensional Drawing showing the mounting holes and exposed thermal pad</i></figcaption>
</figure>

Heatsinking won’t be required in most prototyping applications. However, if you have heat-sensitive items near the module (such as temperature or humidity sensors) they may be influenced by the module. If you are planning to install the module for long-term operation we recommend attaching a heatsink with [thermal compound](https://www.sparkfun.com/products/9599) for best results.

The module also supports changing the read duty cycle to reduce heat dissipation as well. Refer to the [M7E-Hecto Design Guide](./assets/component_documentation/M7E_HECTO_User_Guide.pdf) for more information.



