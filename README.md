# Xarxes

Xarxes is a project that aims to create a simple and scalable design for the creation of LoRa connected sensors.
The goal is to create a generic device for collecting and transmitting data from analog sensors, all while trying to be as cheap as possible.
The current design is based on an Arduino Mega card for data collection, and a TTGO LORA32 V1 (ESP32) to transmit data with LoRaWAN protocol. The project aims to be useable with other LoRa module (RN2483, SX1276), but for now, I use the TTGO LORA32 because I own one and it already contain an SX1276 module.

```
+--------------------------------------------------------------------------------------------------+
|                                                                                                  |
|                                              Xarxes                                              |
|                                                                                                  |
+--------------------------------------------------------------------------------------------------+

    +-----------------------------+                                           +----------------+
    |                             |                                           |                |
    | ARDUINO MEGA                |SDA                                     SDA| TTGO LORA32    |
    |                             +-------------------------------------------+                |
    |                             |                                           |                |
    |                             |SCL                                     SCL|                |
    |                             +-------------------------------------------+                |
    |                             |                                           |                |
    |                             |5V                                       5V|                |
    |                             +-------------------------------------------+                |
    |                             |                                           |                |
    |                             |GND                                     GND|                |
    |                             +-------------------------------------------+                |
    |                             |                                           |                |
    |                             |                                           |                |
    |                             +-----+ Analog input                        |                |
    |                             |                                           |                |
    |                             +-----+ Analog input                        |                |
    |                             |                                           |                |
    |                             +-----+ Digital input                       |                |
    |                             |                                           |                |
    |                             +-----+ Digital input                       |                |
    |                             |                                           |                |
    +-----------------------------+                                           +--------+-------+
      |VIN   |GND                                                                      |
      |      |                                                                         |
      |      |                                                                         |
      | 5V   | GND                    - +--------------------------+ +                 |
      v      v                          |                          |
      |      |                    +-----+ Battery                  +-----+          LoRaWAN
      |      |                    |     |                          |     |
      |      |                    |     +--------------------------+     |
      |      |                    |                                      |
      |      |                    |     +--------------------------+     |
      |      |                    +-----+                          +-----+
      |      |                          | Battery Charging Module  |       <-----+ Energy Source
      |      |                    +-----+                          +-----+
      |      |                    |     +--------------------------+     |
      |      |                    |                                      |
      |      |                    |     +--------------------------+     |
      |      |                    +-----+                          +-----+
      |      |                          | Power Supply  Module     |
      |      +--------------------------+                          +-----+
      |                                 +--------------------------+     |
      |                                                                  |
      +------------------------------------------------------------------+
```

## Costs

Here are the costs of the project following my purchases.

* Arduino Mega 7€
* TTGO LORA32 10€
* Cables 1€
* Sensors 1€ / 20€ -> depends on your needs

For a basic project, 20€ are sufficient.
