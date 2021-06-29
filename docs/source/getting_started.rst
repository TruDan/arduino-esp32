###############
Getting Started
###############

About Arduino ESP32
-------------------

Welcome to the Arduino ESP32 documentation! Here you will find important information on how to use the project.

First Things First
------------------

.. note::
    Before continuing, we must be clear that this project is supported by `Espressif Systems`_ and the community.
    Everyone is more than welcome to contribute back to this project.

ESP32 is a single 2.4 GHz Wi-Fi-and-Bluetooth SoC (System On a Chip) designed by `Espressif Systems`_.

ESP32 is designed for mobile, wearable electronics, and Internet-of-Things (IoT) applications. It features all the state-of-the-art characteristics 
of low-power chips, including fine-grained clock gating, multiple power modes,and dynamic power scaling. For instance, in a low-power IoT sensor 
hub application scenario, ESP32 is woken-up periodically and only when a specified condition is detected. Low-duty cycle is used to minimize the 
amount of energy that the chip expends. 

The output of the power amplifier is also adjustable, thus contributing to an optimal trade-off between communication range, data rate and 
power consumption.

The ESP32 series is available as a chip or module.

Supported SoC's
---------------

Here are the ESP32 series supported by the Arduino-ESP32 project:

======== ====== =========== ===================================
SoC      Stable Development Datasheet
======== ====== =========== ===================================
ESP32    Yes    Yes         `ESP32 Datasheet`_
ESP32-S2 No     Yes         `ESP32-S2 Datasheet`_
ESP32-C3 No     Yes         `ESP32-C3 Datasheet`_
ESP32-S3 No     No          Not Available Yet
======== ====== =========== ===================================

Supported Operating Systems
---------------------------

+-------------------+-------------------+-------------------+
| |windows-logo|    | |linux-logo|      | |macos-logo|      |
+-------------------+-------------------+-------------------+
| Windows           | Linux             | macOS             |
+-------------------+-------------------+-------------------+

.. |windows-logo| image:: _static/windows-logo.png
.. |linux-logo| image:: _static/linux-logo.png
.. |macos-logo| image:: _static/macos-logo.png

Support
*******

This is a community project and it's supported by the community. Fell free to ask for help in one of the community channels.

Issues Reporting
****************

Before opening a new issue, please read this first: 

Be sure to search for a similar reported issue. This is to avoid duplicating or creating noise in the GitHub Issues reporting.
We also have the troubleshooting guide to save your time on the most common issues reported by users.

Community
*********

The Arduino community is huge! You can find a lot of useful content on the Internet.
Here are some community channels you may found information and ask for some help, if needed.

- `ESP32 Forum`_: Official Espressif Forum for ESP32 related discussions.
- `Gitter`_
- `Espressif MCUs (Discord)`_
- `ESP32 on Reddit`_

Arduino Core Reference
----------------------

This documentation is built on the ESP32 and we are not going to cover the common Arduino API. To see the Arduino reference documentation, 
please consider to read the official documentation.

Arduino Official Documentation: `Arduino Reference`_.

How to Getting Started
----------------------

Installing
**********

To install Arduino-ESP32, please see the dedicated section on the Installation guide. We recommend you to install using the boards manager.

`Installing <installing>`_

Examples
********

After installing the toolchain into your environment, you will be able to see all dedicated examples for the ESP32. Those examples are located
in the examples menu or by the `examples` folder inside each `libraries`.

https://github.com/espressif/arduino-esp32/tree/master/libraries

Development Boards
------------------

You will need a development board or a custom board with the ESP32 (see Supported SoC's) to start playing with.
There is a bunch of different types and models widely available on the Internet. You need to choose one that covers all your requirements.
To help you on this selection, we point out some facts about choosing the proper boards and somehow to help you to save money and time.

One ESP32 to rule them all!
***************************

One important information that usually makes some confusion is regarding the different models of the ESP32 SoC and modules.

The ESP32 is divided by family:

* ESP32
* ESP32-S
* ESP32-C

For each family, we have SoC variants with some differentiation. The differences are more about the embedded flash and its size.

The modules uses the SoC internally, including the external flash, PSRAM (in some models) and other essential electronics components. Essentially all
modules from the same family uses the same SoC.

**For example:**

The SoC partnumber is the ESP32-D0WD-V3 and it's the same SoC used inside of the ESP32-WROVER and ESP32-WROOM modules. This means that the
same characteristics are present in both modules.

For more detailed information regarding the SoC's and modules, see the `Espressif Product Selector`_.

Now you know that the module could be different but the heart is the same, you can choose your development board.

Before buying: Keep in mind for some "must have" features when choosing the best board for your needs:

- Embedded USB-to-Serial
- This is very convenient for programming and monitoring the logs with the terminal. 
- Breadboard friendly
- If you are prototyping this will be very useful to connect your board directly on the breadboard.
- open-source/open-hardware
- Check if the schematics are available for download. This helps a lot on prototyping.
- Support
- Some of the manufactures offers a very good level of supporting, with examples and demo projects.

.. _Espressif Systems: https://www.espressif.com 
.. _Espressif Product Selector: https://products.espressif.com/
.. _ESP32 Datasheet: https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_en.pdf
.. _ESP32-S2 Datasheet: https://www.espressif.com/sites/default/files/documentation/esp32-s2_datasheet_en.pdf
.. _ESP32-C3 Datasheet: https://www.espressif.com/sites/default/files/documentation/esp32-c3_datasheet_en.pdf
.. _Arduino.cc: https://www.arduino.cc/en/Main/Software
.. _Arduino Reference: https://www.arduino.cc/reference/en/
.. _ESP32 Forum: https://esp32.com
.. _Gitter: https://gitter.im/espressif/arduino-esp32
.. _Adafruit (Discord): https://discord.gg/adafruit
.. _Espressif MCUs (Discord): https://discord.gg/nKxMTnkD
.. _ESP32 on Reddit: https://www.reddit.com/r/esp32
