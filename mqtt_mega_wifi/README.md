Install and use MQTT with Ardunio+ESP8266.


Reference, [MQTT Communication with Arduino using ESP8266 ESP-01](https://sonyarouje.com/2016/03/15/mqtt-communication-with-arduino-using-esp8266-esp-01/).

## Necessary libraries

### MQTT broker

[Step by step installing and configuring Mosquitto with Windows 7](https://sivatechworld.wordpress.com/2015/06/11/step-by-step-installing-and-configuring-mosquitto-with-windows-7/)

* The most recently version (v1.1.0g) dose not contain the necessary DLLs, (v1.0.2) is still available.
* It can either started from the `SERVICE`, or from the CMD in directory `C:\Program Files (x86)\mosquitto`.

### Program libs

At first, I encounter [beerfactory/hbmqtt, MQTT client/broker using Python asynchronous I/O](https://github.com/beerfactory/hbmqtt) with both broker and client, but I failed to use it since the `asynchronous` is somewhat not so straightforward.

Then the most used (maybe) broker is `Mosquitto` mentioned above, we still need one client (in python), so here it is, [eclipse/paho.mqtt.python](https://github.com/eclipse/paho.mqtt.python).

## Status

The codes are pretty direct, however, the ESP will broke along the way, PC will failed to write to its socket. In fact, NOT A SINGLE `subscribe` is usable in Arduino side. I changed the baud rate of `Serial3` and no good luck. Maybe use a linux platform??

