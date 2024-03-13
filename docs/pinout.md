# Header pinout

![Header pinout](pinout/header.png)

* All pins can be accessed by other HATs with a stacking header.

* The MacArthur HAT uses the <span style="color:red">red pins</span> , which can also be used by other HATs but only one at a time.

* The MacArthur HAT uses the <span style="color:green">green pins</span>, which can also be used by other HATs at the same time.

* The MacArthur HAT does not use the <span style="color:black">black pins</span>.


| Feature | Interface | BCM | Pins | BCM | Interface | Feature |
|:-------:|:---------:|:---:|:----:|:---:|:---------:|:-------:|
|  |  | 3.3V | <span style="color:green">1</span> - <span style="color:green">2</span> | 5V |  |  |
| <span style="font-size:12px">I2C sensors<br>compass, heel, trim</span> | <span style="font-size:12px">I2C SDA</span> | GPIO2 | <span style="color:green">3</span> - <span style="color:green">4</span> | 5V |  |  |
| <span style="font-size:12px">I2C sensors<br>compass, heel, trim</span>| <span style="font-size:12px">I2C SCL</span> | GPIO3 | <span style="color:green">5</span> - <span style="color:green">6</span> | GND |  |  |
| <span style="font-size:12px">NMEA 0183<br>TX1*</span> | <span style="font-size:12px">UART3 TX</span> | GPIO4 | <span style="color:red">7</span> - <span style="color:red">8</span> | GPIO14 | <span style="font-size:12px">UART0 TX</span> | <span style="font-size:12px">MAIANA AIS<br>dAISy HAT<br>Pypilot controller</span>|
| | | GND | <span style="color:green">9</span> - <span style="color:red">10</span> | GPIO15 | <span style="font-size:12px">UART0 RX</span> | <span style="font-size:12px">MAIANA AIS<br>dAISy HAT<br>Pypilot controller</span>|
| | | GPIO17 | <span style="color:black">11</span> - <span style="color:black">12</span> | GPIO18 | | |
| | | GPIO27 | <span style="color:black">13</span> - <span style="color:green">14</span> | GND | | |
| | | GPIO22 | <span style="color:black">15</span> - <span style="color:black">16</span> | GPIO23 | | |
| | | 3.3V | <span style="color:green">17</span> - <span style="color:black">18</span> | GPIO24 | | |
| <span style="font-size:12px">NMEA 2000</span> | <span style="font-size:12px">SPI0<br>MOSI</span> | GPIO10 | <span style="color:green">19</span> - <span style="color:green">20</span> | GND | | |
| <span style="font-size:12px">NMEA 2000</span> | <span style="font-size:12px">SPI0<br>MISO</span>| GPIO9 | <span style="color:green">21</span> - <span style="color:red">22</span> | GPIO25 | <span style="font-size:12px">GPIO</span> | <span style="font-size:12px">NMEA 2000<br>INT</span> |
| <span style="font-size:12px">NMEA 2000</span> | <span style="font-size:12px">SPI0<br>SCLK</span>| GPIO11 | <span style="color:green">23</span> - <span style="color:black">24</span> | GPIO8 | | |
| | | GND | <span style="color:green">25</span> - <span style="color:red">26</span> | GPIO7 | <span style="font-size:12px">SPI0<br>CE1</span> | <span style="font-size:12px">NMEA 2000<br>CS</span> |
| | | GPIO0 | <span style="color:black">27</span> - <span style="color:black">28</span> | GPIO1 | |  |
| <span style="font-size:12px">NMEA 0183<br>RX1*</span> | <span style="font-size:12px">UART3 RX</span>| GPIO5 | <span style="color:red">29</span> - <span style="color:green">30</span> | GND | | |
| | | GPIO6 | <span style="color:black">31</span> - <span style="color:red">32</span> | GPIO12 | <span style="font-size:12px">UART5 TX</span> | <span style="font-size:12px">NMEA 0183<br>TX2*</span> |
| <span style="font-size:12px">NMEA 0183<br>RX2*</span> | <span style="font-size:12px">UART5 RX</span>| GPIO13 | <span style="color:red">33</span> - <span style="color:green">34</span> | GND | | |
| <span style="font-size:12px">1-Wire sensors<br>GPIO</span> | <span style="font-size:12px">1W/GPIO</span>| GPIO19 | <span style="color:red">35</span> - <span style="color:black">36</span> | GPIO16 | | |
| <span style="font-size:12px">Power Off</span> | <span style="font-size:12px">GPIO</span>| GPIO26 | <span style="color:red">37</span> - <span style="color:red">38</span> | GPIO20 | <span style="font-size:12px">GPIO</span> | <span style="font-size:12px">Seatalk<sup>1</sup>  RX<br>GPIO</span> |
| | | GND | <span style="color:green">39</span> - <span style="color:red">40</span> | GPIO21 | <span style="font-size:12px">GPIO</span> | <span style="font-size:12px">Shutdown</span> |

*If you want to use these GPIOs for other purposes, note that they all have pull-up resistors.