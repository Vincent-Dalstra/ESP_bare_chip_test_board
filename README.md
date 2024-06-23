# ESP32 bare-chip test board / GPIB interface  #

This board primarily served as a practice design, to see if I could make a functioning esp32-s3 chip based circuit (not module!).
However, I prefer my boards to have a useful purpose rather than just being a paperweight, so decided to combine it with something else I was working on, which was to make an integrated verison of the boards in
https://github.com/Vincent-Dalstra/ESP32-GPIB-pcb/tree/master?tab=License-1-ov-file, which saves having to use dev boards for this.

The code that it's expected to run can be found at https://github.com/douardda/AR488-ESP32
It is a very useful project, which allows an ESP32 to control various old (and new!) test-equipment.

## Features ##

* Versatile power-input options
  * USB-C port
  * Choice of barrel-jack or 5.08mm screw terminals
    * Works with either polarity - bridge rectifier
    * 3-17V input range
  * If both USB-C and another source are provided, the higher-voltage will be used.
* Wired or Wireless network connectivity
  * Slot for SPI Ethernet adapter (USR-ES1, based on W5500 chip)
  * WiFi/Bluetooth Antenna
* Non-volatile storage
  * 16MB flash via high-speed QIO connection
    * Used to store program code
    * Excess can be used for other purposes
  * 16MB flash via SPI bus
    * Shares the bus with Ethernet adapter
* Programmeable via USB-C port or (optional) 6pin UART header
* Connectors:
  * 24pin connector for GPIB, with 16 IO pins OR
    * alternatively a 10pin 2.50mm JST connector (8x IO, 5V, Gnd)
  * 4pin 1.00mm Piicodev-compatible connector
  * 4pin 2.50mm JST (2x IO, 5V, Gnd)
* Misc.
  * 2x Yellow Indicator LED's
  * 2x Test points that can be soldered to.
