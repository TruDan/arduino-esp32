ESP32-S2-Saola-1
================

Header Block
------------

J2
^^^
===  ====  =====  ===================================
No.  Name  Type   Function
===  ====  =====  ===================================
1    3V3   P      3.3 V power supply
2    IO0   I/O    GPIO0, Boot
3    IO1   I/O    GPIO1, ADC1_CH0, TOUCH_CH1
4    IO2   I/O    GPIO2, ADC1_CH1, TOUCH_CH2
5    IO3   I/O    GPIO3, ADC1_CH2, TOUCH_CH3
6    IO4   I/O    GPIO4, ADC1_CH3, TOUCH_CH4
7    IO5   I/O    GPIO5, ADC1_CH4, TOUCH_CH5
8    IO6   I/O    GPIO6, ADC1_CH5, TOUCH_CH6
9    IO7   I/O    GPIO7, ADC1_CH6, TOUCH_CH7
10   IO8   I/O    GPIO8, ADC1_CH7, TOUCH_CH8
11   IO9   I/O    GPIO9, ADC1_CH8, TOUCH_CH9
12   IO10  I/O    GPIO10, ADC1_CH9, TOUCH_CH10
13   IO11  I/O    GPIO11, ADC2_CH0, TOUCH_CH11
14   IO12  I/O    GPIO12, ADC2_CH1, TOUCH_CH12
15   IO13  I/O    GPIO13, ADC2_CH2, TOUCH_CH13
16   IO14  I/O    GPIO14, ADC2_CH3, TOUCH_CH14
17   IO15  I/O    GPIO15, ADC2_CH4, XTAL_32K_P
18   IO16  I/O    GPIO16, ADC2_CH5, XTAL_32K_N
19   IO17  I/O    GPIO17, ADC2_CH6, DAC_1
20   5V0   P      5 V power supply
21   GND   G      Ground
===  ====  =====  ===================================

J3
^^^
===  ====  =====  ====================================
No.  Name  Type   Function
===  ====  =====  ====================================
1    GND   G      Ground
2    RST   I      CHIP_PU, Reset
3    IO46  I      GPIO46
4    IO45  I/O    GPIO45
5    IO44  I/O    GPIO44, U0RXD
6    IO43  I/O    GPIO43, U0TXD
7    IO42  I/O    GPIO42, MTMS
8    IO41  I/O    GPIO41, MTDI
9    IO40  I/O    GPIO40, MTDO
10   IO39  I/O    GPIO39, MTCK
11   IO38  I/O    GPIO38
12   IO37  I/O    GPIO37
13   IO36  I/O    GPIO36
14   IO35  I/O    GPIO35
16   IO34  I/O    GPIO34
17   IO33  I/O    GPIO33
17   IO26  I/O    GPIO26
18   IO21  I/O    GPIO21
19   IO20  I/O    GPIO20, ADC2_CH3, USB_D+
20   IO19  I/O    GPIO19, ADC2_CH3, USB_D-
21   IO18  I/O    GPIO18, ADC2_CH3, DAC_2
===  ====  =====  ====================================

    P: Power supply;
    I: Input;
    O: Output;
    T: High impedance.

Pin Layout
----------

.. figure:: ../_static/esp32s2_pinmap.png
    :align: center
    :alt: ESP32-S2-Saola-1 (click to enlarge)
    :figclass: align-center
