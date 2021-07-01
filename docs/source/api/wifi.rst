#########
Wi-Fi API
#########

About
-----

The Wi-Fi API provide support for the 802.11b/g/n protocol driver. This API includes:


* Station mode (STA mode or Wi-Fi client mode). ESP32 connects to an access point.

* AP mode (aka Soft-AP mode or Access Point mode). Devices connects to the ESP32.

* Security modes (WPA, WPA2, WEP, etc.)

* Scanning for access points.

Working as AP
*************

In this mode...

Working as STA
**************

The STA mode...

API Description
---------------

WiFi
****

WiFiAP
******

WiFiSTA
*******

WiFiClient
**********

WiFiGeneric
***********

WiFiMulti
*********

WiFiScan
********

WiFiServer
**********

WiFiType
********

WiFiUdp
*******

Examples
--------

Wi-Fi AP (Client)
*****************

.. literalinclude:: ../../../libraries/WiFi/examples/WiFiClient/WiFiClient.ino
    :language: arduino

Wi-Fi STA 
*********

.. literalinclude:: ../../../libraries/WiFi/examples/WiFiAccessPoint/WiFiAccessPoint.ino
    :language: arduino

References
----------
