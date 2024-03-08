# Header pinout

![Header pinout](pinout/header.png)

* All pins can be accessed by other HATs with a stacking header.

* The MacArthur HAT uses the <span style="color:red">red pins</span> , which can also be used by other HATs but only one at a time.

* The MacArthur HAT uses the <span style="color:green">green pins</span>, which can also be used by other HATs at the same time.

* The MacArthur HAT does not use the black pins.


| Feature | Interface | BCM | Pins | BCM | Interface | Feature |
|:-------:|:---------:|:---:|:----:|:---:|:---------:|:-------:|
|  |  | 3.3V | <span style="color:green">1</span> - <span style="color:green">2</span> | 5V |  |  |
| <span style="font-size:12px">I2C sensors</span> | I2C SDA | GPIO2 | <span style="color:green">3</span> - <span style="color:green">4</span> | 5V |  |  |
| <span style="font-size:12px">I2C sensors</span>| I2C SCL | GPIO3 | <span style="color:green">5</span> - <span style="color:green">6</span> | GND |  |  |
| <span style="font-size:12px">NMEA 0183 TX1*</span> | UART3 TX | GPIO4 | <span style="color:red">7</span> - <span style="color:red">8</span> | GPIO14 | UART0 TX | <span style="font-size:12px">MAIANA AIS<br>dAISy HAT</span>|
| | | GND | <span style="color:green">9</span> - <span style="color:red">10</span> | GPIO15 | UART0 RX | <span style="font-size:12px">MAIANA AIS<br>dAISy HAT</span>|
| | | GPIO17 | 11 - 12 | GPIO18 | | |
| | | GPIO27 | 13 - <span style="color:green">14</span> | GND | | |
| | | GPIO22 | 15 - 16 | GPIO23 | | |
| | | 3.3V | <span style="color:green">17</span> - 18 | GPIO24 | | |
| <span style="font-size:12px">NMEA 2000</span> | SPI0 MOSI | GPIO10 | <span style="color:green">19</span> - <span style="color:green">20</span> | GND | | |

