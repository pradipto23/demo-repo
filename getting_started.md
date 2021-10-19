# Getting Started with Radar BGT60 Shield & PSoC 6

This page explains how to set up everything to work with the Modus Toolbox, PSoC 6 and the BGT60.

## Overview

### Required experience
-Experience level: Moderate

-Basic programming skills: C / C++

### Required Hardware
Name         | Picture |
---          |---      |
[BGT60LTR11AIP](https://www.infineon.com/cms/en/product/evaluation-boards/demo-bgt60ltr11aip/) | ![alt text](https://github.com/Infineon/radar-bgt60/blob/master/docs/img/bgt60-without-background.png)
PSoC 6 kit like [this](https://www.cypress.com/documentation/development-kitsboards/psoc-6-wi-fi-bt-prototyping-kit-cy8cproto-062-4343w) |<img src="img/CY8CPROTO_062_4343W_KitImage.png" height="80px">
Micro-USB to USB A cable | use the cable included into the [CY8CPROTO-062-4343W Prototyping Kit](https://www.cypress.com/documentation/development-kitsboards/psoc-6-wi-fi-bt-prototyping-kit-cy8cproto-062-4343w)
pin headers and cables | solder or plug them into the shield and prototyping kit

### Required Software

* [Modus Toolbox](https://www.cypress.com/products/modustoolbox)
* Infineon multi-half-bridge library (this library)
* see library <a href="PSoc-Library-Installation">Lib Installation</a><br>
* for Windows: [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) Serial Terminal 
* for Linux: [miniCom](https://help.ubuntu.com/community/Minicom)

### Tutorial

#### Software Installation

0. **install Modus Toolbox**. Download the software and follow the instructions in the following [website](https://www.cypress.com/products/modustoolbox)

1. **for Windows install PuTTY**. Downloadable from the official [website](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html) or use an other
sufficient terminal under your system.

2. **for Linux install miniCom**. Use your system installer (apt, apt-get, pkcon, zypper or similar). You can also use any other
similar software.

3. **install the multi-half-bridge library**. Follow the steps in the [PSoC Library Installation](PSoc6-Library-Installation) section. 

### Tutorial

#### Hardware Setup for PSoC 6

| Pin Number            | Pin Function   |
| ------------          | -------------  |
|P6.0                   | Phase detect pin on PSoC 6 |
|P6.1                   | Target Detect pin on PSoC 6 |

Once you connect the BGT60 shield with the PSoC 6 you can connect the micro USB cable to PSoC and connect everything to your computer.


### Ready to Go !

1. **Example Detect Motion**

   Ensure the macro *Current Example* is set to the *Motion_ Detect*. Now you can compile the code and can open the terminal window in your system. The serial monitor should tell you that the radar shield is initialized after a short time. Now you can move a object in front of the sensor and the monitor should tell you : "Target in motion detected!".

2. **Example Direction Detect**

   Ensure the macro *Current Example* is set to the *Target_ Detect*. Now you can compile the code and can open the terminal window in your system. The serial monitor should tell you that the radar shield is initialized after a short time. Now you can move a object towards the sensor and the monitor should tell you : "Target approaching!".
