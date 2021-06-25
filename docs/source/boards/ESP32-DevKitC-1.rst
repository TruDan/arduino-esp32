ESP32-DevKitC-1
===============

Header Block
------------

J1
^^^
===  ====  =====  ===================================
No.  Name  Type   Function
===  ====  =====  ===================================
1    3V3   P      3.3 V power supply
2    EN    I      CHIP_PU, Reset
3    IO36  I      GPIO36, ADC1_CH0, S_VP
4    IO39  I      GPIO39, ADC1_CH3, S_VN
5    IO34  I      GPIO34, ADC1_CH6, VDET_1
6    IO35  I      GPIO35, ADC1_CH7, VDET_2
7    IO32  I/O    GPIO32, ADC1_CH4, TOUCH_CH9, XTAL_32K_P
8    IO33  I/O    GPIO33, ADC1_CH5, TOUCH_CH8, XTAL_32K_N
9    IO25  I/O    GPIO25, ADC1_CH8, DAC_1
10   IO26  I/O    GPIO26, ADC2_CH9, DAC_2
11   IO27  I/O    GPIO27, ADC2_CH7, TOUCH_CH7
12   IO14  I/O    GPIO14, ADC2_CH6, TOUCH_CH6, MTMS
13   IO12  I/O    GPIO12, ADC2_CH5, TOUCH_CH5, MTDI
14   GND   G      Ground
15   IO13  I/O    GPIO13, ADC2_CH4, TOUCH_CH4, MTCK
16   IO9   I/O    GPIO9, D2
17   IO10  I/O    GPIO10, D3
18   IO11  I/O    GPIO11, CMD
19   5V0   P      5 V power supply
===  ====  =====  ===================================

J3
^^^
===  ====  =====  ====================================
No.  Name  Type   Function
===  ====  =====  ====================================
1    GND   G      Ground
2    IO23  I/O    GPIO23
3    IO22  I/O    GPIO22
4    IO1   I/O    GPIO1, U0TXD
5    IO3   I/O    GPIO3, U0RXD
6    IO21  I/O    GPIO21
7    GND   G      Ground
8    IO19  I/O    GPIO19
9    IO18  I/O    GPIO18
10   IO5   I/O    GPIO5
11   IO17  I/O    GPIO17
12   IO16  I/O    GPIO16
13   IO4   I/O    GPIO4, ADC2_CH0, TOUCH_CH0
14   IO0   I/O    GPIO0, ADC2_CH1, TOUCH_CH1, Boot
16   IO2   I/O    GPIO2, ADC2_CH2, TOUCH_CH2
17   IO15  I/O    GPIO15, ADC2_CH3, TOUCH_CH3, MTDO
17   IO8   I/O    GPIO8, D1
18   IO7   I/O    GPIO7, D0
19   IO6   I/O    GPIO6, SCK
===  ====  =====  ====================================

    P: Power supply;
    I: Input;
    O: Output;
    T: High impedance.

Pin Layout
----------

.. figure:: ../_static/esp32_pinmap.png
    :align: center
    :alt: ESP32-DevKitC-1 (click to enlarge)
    :figclass: align-center
