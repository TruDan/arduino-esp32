######
Boards
######

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
    * Wi-Fi and BLE
* ESP32-S
    * Wi-Fi only
* ESP32-C
    * Wi-Fi and BLE 5

For each family, we have SoC variants with some differentiation. The differences are more about the embedded flash and its size and the number of the cores (dual or single).

The modules uses the SoC internally, including the external flash, PSRAM (in some models) and other essential electronics components. Essentially all
modules from the same family uses the same SoC.

.. figure:: ../_static/soc-module.png
    :align: center
    :width: 250
    :alt: ESP32 SoC and Module (click to enlarge)
    :figclass: align-center

**For example:**

The SoC partnumber is the ESP32-D0WD-V3 and it's the same SoC used inside of the ESP32-WROVER (with PSRAM) and ESP32-WROOM modules. This mean that the
same characteristics are present in both modules core.

For more detailed information regarding the SoC's and modules, see the `Espressif Product Selector`_.

Now you know that the module could be different but the heart is the same, you can choose your development board.

Before buying: Keep in mind for some "must have" features when choosing the best board for your needs:

- Embedded USB-to-Serial
    - This is very convenient for programming and monitoring the logs with the terminal via USB. 
- Breadboard friendly
    - If you are prototyping, this will be very useful to connect your board directly on the breadboard.
- open-source/open-hardware
    - Check if the schematics are available for download. This helps a lot on prototyping.
- Support
    - Some of the manufactures offers a very good level of supporting, with examples and demo projects.


.. toctree::
    :maxdepth: 1
    :caption: Espressif Boards:

    ESP32-DevKitC <ESP32-DevKitC-1>
    ESP32-S2-Saola-1 <ESP32-S2-Saola-1>
    ESP32-C3-DevKitM-1 <ESP32-C3-DevKitM-1>

Third Party
-----------

Add here the third party boards, listed by vendors.

.. toctree::
    :maxdepth: 1
    :caption: Generic Boards:

    Generic <generic>