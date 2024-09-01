![MacArthur HAT](https://raw.githubusercontent.com/OpenMarine/MacArthur-HAT/main/images/macarthur-render.jpg)

# MacArthur HAT v1.2 Documentation

After a few years of developing software for **OpenPlotter**, we have identified exactly what we need in terms of hardware to achieve our goals and the result is the **MacArthur HAT** (Hardware Attached on Top), an add-on board for **Raspberry Pi** running OpenPlotter. With this HAT we want to get the fully open-source boat to free ourselves from dependence on big companies and make our boats more respectful with the environment.

This name is not accidental, we want to honor [**Ellen MacArthur**](https://en.wikipedia.org/wiki/Ellen_MacArthur) who is not only known for being an exceptional sailor but also for her commitment to the [circular economy](https://ellenmacarthurfoundation.org). The MacArthur HAT is an electronic circuit that is as difficult to recycle and has an environmental cost to manufacture as any modern circuit, but it is designed to last and stay in your boat forever.

Its main function is to be able to communicate with any old or new marine electronic device using the proprietary and closed protocols **Seatalk<sup>1</sup>**, **NMEA 0183** or **NMEA 2000** and the free and open protocol **Signal K**. This means that when an on-board device dies, we are not forced to buy another of the same brand, that uses the same technology or even uses the same protocol because we can mix different devices. We will be able to recycle and reuse old devices giving them a second life or we will be able to gradually replace our old closed and proprietary models with new, cheaper, free and open ones.

You can also power the *Raspberry Pi* directly from the ship's batteries and it has a **smart power management system** to turn it on and off automatically and **protect the SD card**. This HAT is **stackable** and can be used with other HATs such as the **Moitessier HAT** or the **dAISy HAT**. It can also be connected directly to the **MAIANA AIS transponder** without the need for an adapter.

Some of the MacArthur HAT features, such as the power management, the AIS receiver/transponder, the **1-Wire sensors** or the **I2C internal and external sensors**, are optional. In this way you only buy what you need saving money and we do not have to manufacture things that will never be used saving natural resources.

MacArthur HAT is fully supported by OpenPlotter and all of its features can be easily configured with just a few clicks. No drivers needed. If you are not using OpenPlotter, you can still access all its features, but you have to enable all interfaces and configure the system manually.

## Compatibility

| Hardware | Software | Notes |
| -------- | -------- |------ |
| Raspberry Pi model 3 | [OpenPlotter v3.x.x](https://openplotter.readthedocs.io/3.x.x/description/what_is_openplotter.html)| NMEA 0183 does not work |
| Raspberry Pi model 4 | [OpenPlotter v3.x.x](https://openplotter.readthedocs.io/3.x.x/description/what_is_openplotter.html)<br>[OpenPlotter v4.x.x](https://openplotter.readthedocs.io/4.x.x/description/what_is_openplotter.html)| |
| Raspberry Pi model 5 | [OpenPlotter v4.x.x](https://openplotter.readthedocs.io/4.x.x/description/what_is_openplotter.html)| |

## Features

![MacArthur-HAT](https://raw.githubusercontent.com/OpenMarine/MacArthur-HAT/main/images/macarthur-diagram.png)

- 1x NMEA 2000 non-isolated input and output. Data connection by SPI0-1. Optional 120Ω termination resistor included. Compatible with any CAN bus.
- 2x NMEA 0183 opto-isolated inputs and 2x NMEA 0183 non-isolated outputs. Data connection by UART3 and UART5 (Raspberry Pi 4) or UART2 and UART4 (Raspberry Pi 5).
- 1x Seatalk<sup>1</sup> non-isolated input (not output). This connector can be also used as a general-purpose input.
- 1x Connector for multiple 1-Wire temperature sensors such as the DS18B20 (exhaust, engine, fridge...). A 1.6KΩ pull-up resistor is included. This connector can be also used as a non-isolated general-purpose input/output.
- 1x STEMMA QT/Qwiic connector for multiple I2C sensors (IMU, temperature, pressure, humidity, gas...). Compatible with most Adafruit and SparkFun sensors.
- Optional 12V to 5V DC/DC converter via [add-on module](https://shop.openmarine.net/home/24-power-module-for-macarthur-hat.html) to power the Raspberry Pi and its peripherals (including touch screens up to 10 inches). When you turn off the main switch of your ship, OpenPlotter will shut down safely. OpenPlotter will start cleanly when the main switch is turned on again.
- Optional GPS reception and AIS reception/transmission with the [MAIANA AIS base kit](https://shop.openmarine.net/home/15-maiana-ais-base-kit.html). The MacArthur HAT has all the features of all MAIANA AIS adapters in one. Data connection by UART0.
- Optional compass, heel, and trim via internal or external add-on module (IMU 9DOF).
- Compatible with [dAISy HAT](https://shop.openmarine.net/home/14-daisy-hat-ais-receiver.html), Moitessier HAT (hacked) and [Pypilot motor controllers](https://pypilot.org/opencart/index.php?route=product/category&path=59). Not compatible with Pypilot HAT. 
- Detachable screw connectors for easy mounting and maximum compatibility.
- Includes input and output LEDs to check activity at any time.
- No drivers needed.

## Safety

!!! important
	Most of the connections between the Raspberry Pi, the MacArthur HAT and your boat are not isolated. To avoid damaging the Raspberry Pi or MacArthur HAT, it is therefore important that everyone agrees on what represents ground, to which all other voltages are referenced.

	To ensure this, make sure that there is always a connection from the MacArthur HAT to the boat's ground before making any other connection. The easiest way to do this, is through the 12V/GND connector on the MacArthur HAT. Always make this connection first, and break it last. Do this even if you are not powering the Pi from 12V.

!!! note
	We are aware of the electrical gremlins that lure in ground loops caused by redundant grounding. However, those gremlins typically are less fatal to our equipment than grossly diverging ground potentials. So until we introduce a HAT with fully isolated interfaces, we think a conservative approach to grounding is the safest option.

## License and sources

Copyright Adrian Studer & Sailoog, 2023.

This source describes Open Hardware and is licensed under the CERN-OHL-S v2.

You may redistribute and modify this source and make products using it under the terms of the CERN-OHL-S v2 [https://ohwr.org/cern_ohl_s_v2.txt](https://ohwr.org/cern_ohl_s_v2.txt).

This source is distributed WITHOUT ANY EXPRESS OR IMPLIED WARRANTY, INCLUDING OF MERCHANTABILITY, SATISFACTORY QUALITY AND FITNESS FOR A PARTICULAR PURPOSE. Please see the CERN-OHL-S v2 for applicable conditions.

Source: [https://github.com/OpenMarine/MacArthur-HAT](https://github.com/OpenMarine/MacArthur-HAT)

As per CERN-OHL-S v2 section 4, should you produce hardware based on this source, you must where practicable maintain the Source Location visible on the external case of the MacArthur HAT or other products you make using this source.

## Buy

[**OpenMarine store** (Catalonia)](https://shop.openmarine.net/home/23-macarthur-hat.html)

[**Wegmatt store** (US)](https://shop.wegmatt.com/collections/openmarine)