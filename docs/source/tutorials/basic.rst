##############
Basic Tutorial
##############

Introduction
------------

This is the basic tutorial and should be used as template for other tutorials.

Requirements
------------

* Arduino IDE
* ESP32 Board
* Good USB Cable

Steps
-----

Here are the steps for this tutorial.

1. Open the Arduino IDE

.. figure:: ../_static/tutorials/basic/tutorial_basic_ide.png
    :align: center
    :width: 600
    :alt: Arduino IDE (click to enlarge)
    :figclass: align-center

2. Build and Flash the `blink` project.

Code
----

.. code-block:: arduino
    :caption: Blink.ino
    :linenos:

    /*
    Blink

    Turns an LED on for one second, then off for one second, repeatedly.

    Most Arduinos have an on-board LED you can control. On the UNO, MEGA and ZERO
    it is attached to digital pin 13, on MKR1000 on pin 6. LED_BUILTIN is set to
    the correct LED pin independent of which board is used.
    If you want to know what pin the on-board LED is connected to on your Arduino
    model, check the Technical Specs of your board at:
    https://www.arduino.cc/en/Main/Products

    modified 8 May 2014
    by Scott Fitzgerald
    modified 2 Sep 2016
    by Arturo Guadalupi
    modified 8 Sep 2016
    by Colby Newman

    This example code is in the public domain.

    http://www.arduino.cc/en/Tutorial/Blink
    */

    // the setup function runs once when you press reset or power the board
    void setup() {
    // initialize digital pin LED_BUILTIN as an output.
    pinMode(LED_BUILTIN, OUTPUT);
    }

    // the loop function runs over and over again forever
    void loop() {
    digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
    delay(1000);                       // wait for a second
    digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
    delay(1000);                       // wait for a second
    }

Log Output
----------

If the log output from the serial monitor is relevant, please add here:

.. code-block::

    I (0) cpu_start: App cpu up.
    I (418) cpu_start: Pro cpu start user code
    I (418) cpu_start: cpu freq: 160000000
    I (418) cpu_start: Application information:
    I (423) cpu_start: Project name:     a2dp_source
    I (428) cpu_start: App version:      v4.4-dev-1811-gecf015ef68-dirty
    I (435) cpu_start: Compile time:     Jun 23 2021 16:08:32
    I (441) cpu_start: ELF file SHA256:  2e294414643e7e7a...
    I (447) cpu_start: ESP-IDF:          v4.4-dev-1811-gecf015ef68-dirty
    I (454) heap_init: Initializing. RAM available for dynamic allocation:
    I (461) heap_init: At 3FFAFF10 len 000000F0 (0 KiB): DRAM
    I (467) heap_init: At 3FFB6388 len 00001C78 (7 KiB): DRAM
    I (474) heap_init: At 3FFB9A20 len 00004108 (16 KiB): DRAM
    I (480) heap_init: At 3FFC8EB8 len 00017148 (92 KiB): DRAM
    I (486) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
    I (492) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
    I (499) heap_init: At 4009657C len 00009A84 (38 KiB): IRAM
    I (506) spi_flash: detected chip: gd
    I (509) spi_flash: flash io: dio


Resources
---------

* `ESP32 Datasheet`_ (Datasheet)

.. _ESP32 Datasheet: https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_en.pdf
