![Sendero](http://sendero.uy/images/logo-white.png)

# Sendero Lighting Firmware


C++ firmware for NodeMCU V2 DevKit boards that works as intermediary between [Sendero Middleware](https://github.com/Sendero-Project/SenderoMiddleware) and Sendero LED Driver (Bondibar).

The code is wrapped in a [PlatformIO](http://platformio.org/platformio-ide) project. It compiles for **NodeMCU v2 DevKit** board using [Arduino framework](https://github.com/esp8266/Arduino).

Installation
============

- Install PlatformIO IDE, open this project, compile and install it in your NodeMCU V2 DevKit board.

- Connect to the board's WiFi access point. In your browser go to `https://192.168.4.1` and set your router's SSID and PASSWORD.

![enter image description here](http://sendero.uy/images/ap-config.png)

- Also insert the number ID for your device and then click Save button (at the bottom of the table).

![enter image description here](http://sendero.uy/images/id-config.png)

> **Note:**
> It is recommended to set sequential numbers in `Device.number` settings starting from 0 (i.e.: set 0 to the first device, 1 to the next, and so on...)

- Restart the device and connect back to your router's AP.

- You can now verify if the device connected to your AP by accessing to your router's admin page. It's possible to access to the configuration form through the local network using the device's IP adderess. The device's *AP mode* turns off while it's connected to the router. To activate it back just leave ssid and password inputs blank, save and restart the device.

- It is now possible to receive streaming from [Sendero Middleware](https://github.com/Sendero-Project/SenderoMiddleware). Go to its repository to check how to configure the device as a receiver.


Connection with Bondibar
========================

The connection mapping from the NodeMCU to the Bondibar is as follows:

NodeMCU pin | USB pin
----------- | -------
D5 | DATA+
D7 | DATA-
VIN | USB Vcc
GND | USB Ground

We recommend using Sendero Wireless Dongle, but the connection can be achieved with a custom cable.

![enter image description here](http://sendero.uy/images/wireless-dongle.png)
![enter image description here](http://sendero.uy/images/custom-usb.png)

The following picture shows the way to connect the wireless dongle to the Bondibar

![enter image description here](http://sendero.uy/images/wb-connection.png)


-------------

For more information about Sendero Project go to the [base repository](https://github.com/Sendero-Project/Sendero).
