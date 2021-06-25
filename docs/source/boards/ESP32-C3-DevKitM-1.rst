ESP32-C3-DevKitM-1
==================

Header Block
------------

J1
^^^
===  ====  ==========  ===================================
No.  Name  Type [1]_   Function
===  ====  ==========  ===================================
1    GND   G           Ground
2    3V3   P           3.3 V power supply
3    3V3   P           3.3 V power supply
4    IO2   I/O/T       GPIO2 [2]_, ADC1_CH2, FSPIQ
5    IO3   I/O/T       GPIO3, ADC1_CH3
6    GND   G           Ground
7    RST   I           CHIP_PU
8    GND   G           Ground
9    IO0   I/O/T       GPIO0, ADC1_CH0, XTAL_32K_P
10   IO1   I/O/T       GPIO1, ADC1_CH1, XTAL_32K_N
11   IO10  I/O/T       GPIO10, FSPICS0
12   GND   G           Ground
13   5V    P           5 V power supply
14   5V    P           5 V power supply
15   GND   G           Ground
===  ====  ==========  ===================================

J3
^^^
===  ====  ==========  ====================================
No.  Name  Type [1]_   Function
===  ====  ==========  ====================================
1    GND   G           Ground
2    TX    I/O/T       GPIO21, U0TXD
3    RX    I/O/T       GPIO20, U0RXD
4    GND   G           Ground
5    IO9   I/O/T       GPIO9 [2]_
6    IO8   I/O/T       GPIO8 [2]_, RGB LED
7    GND   G           Ground
8    IO7   I/O/T       GPIO7, FSPID, MTDO
9    IO6   I/O/T       GPIO6, FSPICLK, MTCK
10   IO5   I/O/T       GPIO5, ADC2_CH0, FSPIWP, MTDI
11   IO4   I/O/T       GPIO4, ADC1_CH4, FSPIHD, MTMS
12   GND   G           Ground
13   IO18  I/O/T       GPIO18, USB_D-
14   IO19  I/O/T       GPIO19, USB_D+
15   GND   G           Ground
===  ====  ==========  ====================================

.. [1] P: Power supply; I: Input; O: Output; T: High impedance.
.. [2] GPIO2, GPIO8, and GPIO9 are strapping pins of the ESP32-C3FN4 chip. During the chip's system reset, the latches of the strapping pins sample the voltage level as strapping bits, and hold these bits until the chip is powered down or shut down. For description and application of strapping pins.

Pin Layout
----------

.. figure:: ../_static/esp32c3_pinmap.png
    :align: center
    :alt: ESP32-C3-DevKitM-1 (click to enlarge)
    :figclass: align-center
