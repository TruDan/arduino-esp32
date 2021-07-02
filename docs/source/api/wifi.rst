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

In this mode the ESP32 is configured as an Access Point (AP) and it's capable of receiving incomming connections from other devices (stations) by providing
a Wi-Fi network.

.. figure:: ../_static/wifi_esp32_ap.png
    :align: center
    :width: 520
    :figclass: align-center

This mode can be used for serving a HTTP or HTTPS server inside the ESP32, for example.

Working as STA
**************

The STA mode is used to connect the ESP32 to a Wi-Fi network, provided by an Access Point.

.. figure:: ../_static/wifi_esp32_sta.png
    :align: center
    :width: 520
    :figclass: align-center

If you need to connect your project to the Internet, this is the mode you are looking for.

API Description
---------------

Here is the description about the API.

WiFi
----

WiFiAP
------

The ``WiFiAP`` is used to configure and manage the Wi-Fi as Access Point. Here are located the related functions for the AP.

Basic Usage
***********


To start the Wi-Fi as AP

.. code-block:: arduino

    WiFi.softAP(ssid, password);

begin
*****

- Functions ``begin`` are used to configure and start the Wi-Fi.

.. code-block:: arduino

    wl_status_t begin(const char* ssid, const char *passphrase = NULL, int32_t channel = 0, const uint8_t* bssid = NULL, bool connect = true);

Where:

* ``const char* ssid``
* ``const char *passphrase``
* ``int32_t channel``
* ``const uint8_t* bssid``
* ``bool connect``

.. code-block:: arduino

    wl_status_t begin(char* ssid, char *passphrase = NULL, int32_t channel = 0, const uint8_t* bssid = NULL, bool connect = true);

Where:

* ``char* ssid``
* ``char *passphrase``
* ``int32_t channel``
* ``const uint8_t* bssid``
* ``bool connect``

.. code-block:: arduino

    wl_status_t begin();

config
******

Function ``config`` is used to configure Wi-Fi. After configuring, you can call function ``begin`` to start the Wi-Fi process.

.. code-block:: arduino

    bool config(IPAddress local_ip, IPAddress gateway, IPAddress subnet, IPAddress dns1 = (uint32_t)0x00000000, IPAddress dns2 = (uint32_t)0x00000000);

Where:

* ``IPAddress local_ip`` set the local IP.
* ``IPAddress gateway`` set the gateway IP.
* ``IPAddress subnet`` set the subnet mask.
* ``IPAddress dns1`` set the DNS.
* ``IPAddress dns2`` set the DNS alternative option.

Return ``true`` if the configuration was successful.

reconnect
*********

Function used to reconnect the Wi-Fi connection.

.. code-block:: arduino

    bool reconnect();

disconnect
**********

Function to force disconnection.

.. code-block:: arduino

    bool disconnect(bool wifioff = false, bool eraseap = false);

Where:

* ``bool wifioff`` use ``true`` to turn the Wi-Fi radio off.
* ``bool eraseap`` use ``true`` to erase the AP configuration from the NVS memory.

Return ``true`` if the configuration was successful.

isConnected
***********

.. code-block:: arduino

    bool isConnected();

setAutoConnect
**************

.. code-block:: arduino

    bool setAutoConnect(bool autoConnect);

Where:

* ``bool autoConnect``

getAutoConnect
**************

.. code-block:: arduino

    bool getAutoConnect();

setAutoReconnect
****************

.. code-block:: arduino

    bool setAutoReconnect(bool autoReconnect);

Where:

* ``bool autoConnect``

getAutoReconnect
****************

.. code-block:: arduino

    bool getAutoReconnect();

WiFiSTA
-------

Basic Usage
***********

The ``WiFiSTA`` is used to configure and manage the Wi-Fi as Station. Here are located the related functions for the STA.

.. code-block:: arduino

    WiFi.begin(ssid, password);

Where the ``ssid`` and ``password`` are from the network you want to connect the ESP32.

To check if the connection is successful, you can use:

.. code-block:: arduino

    while (WiFi.status() != WL_CONNECTED) {
        delay(500);
        Serial.print(".");
    }

After a successful connection, you can print the IP address given by the network.

.. code-block:: arduino

    Serial.println("IP address: ");
    Serial.println(WiFi.localIP());

Please see the full example of the WiFiSTA in: ref:: Wi-Fi STA.

softAP
******

To configure the Wi-Fi AP characteristics, the function ``softAP`` is used:

.. code-block:: arduino

    bool softAP(const char* ssid, const char* passphrase = NULL, int channel = 1, int ssid_hidden = 0, int max_connection = 4, bool ftm_responder = false);

Where:

* ``const char* ssid`` set the Wi-Fi network SSID.
* ``const char* passphrase`` set the Wi-Fi network password. If the network is open, set as ``NULL``. 
* ``int channel`` configure the Wi-Fi channel.
* ``int ssid_hidden`` set the network as hidden.
* ``int max_connection`` set the maxumum number of simultaneous connections. The default is 4.
* ``bool ftm_responder`` set the Wi-Fi FTM responder feature. **Only for ESP32-S2 and ESP32-C3 SoC!**

Return ``true`` if the configuration was successful.

softAPConfig
************

.. code-block:: arduino

    bool softAPConfig(IPAddress local_ip, IPAddress gateway, IPAddress subnet);

Where:

* ``IPAddress local_ip``
* ``IPAddress gateway``
* ``IPAddress subnet``

Return ``true`` if the configuration was successful.

softAPdisconnect
****************

.. code-block:: arduino

    bool softAPdisconnect(bool wifioff = false);

Where:

* ``bool wifioff``

Return ``true`` if the command was successful.

softAPgetStationNum
*******************

.. code-block:: arduino

    uint8_t softAPgetStationNum();

softAPIP
********

.. code-block:: arduino

    IPAddress softAPIP();

softAPBroadcastIP
*****************

.. code-block:: arduino

    IPAddress softAPBroadcastIP();

softAPNetworkID
***************

.. code-block:: arduino

    IPAddress softAPNetworkID();

softAPSubnetCIDR
****************

.. code-block:: arduino

    uint8_t softAPSubnetCIDR();

softAPenableIpV6
****************

.. code-block:: arduino

    bool softAPenableIpV6();

Return ``true`` if the configuration was successful.

softAPIPv6
**********

.. code-block:: arduino

    IPv6Address softAPIPv6();

softAPgetHostname
*****************

.. code-block:: arduino

    const char * softAPgetHostname();

softAPsetHostname
*****************

.. code-block:: arduino

    bool softAPsetHostname(const char * hostname);

Where:

* ``const char * hostname``

Return ``true`` if the configuration was successful.

softAPmacAddress
****************

.. code-block:: arduino

    uint8_t* softAPmacAddress(uint8_t* mac);

Where:

* ``uint8_t* mac``

.. code-block:: arduino

    String softAPmacAddress(void);

softAPSSID
**********

.. code-block:: arduino

    String softAPSSID(void) const;

WiFiClient
----------

WiFiGeneric
-----------

WiFiMulti
---------

WiFiScan
--------

WiFiServer
----------

WiFiType
--------

WiFiUdp
-------

Examples
--------

Wi-Fi AP Example
****************

.. literalinclude:: ../../../libraries/WiFi/examples/WiFiAccessPoint/WiFiAccessPoint.ino
    :language: arduino

Wi-Fi STA Example
*****************

.. literalinclude:: ../../../libraries/WiFi/examples/WiFiClient/WiFiClient.ino
    :language: arduino

References
----------
