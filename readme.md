# NEC Projector Controller

_2016 gmb_

OSC-enabled MaxMSP utility for sending projector commands over serial to NEC projectors (for a project with the NP-M282X and NP-M322W models).

Basic UI for Power On, Power Off, VGA Source. Other command codes can be found in the NEC manuals.

### OSC on port 53007:
/projector/on <bang> — Power on/start warmup
/projector/off <bang> — Poweroff/start cooldown
/projector/vga <bang> — force VGA input source

### Dependencies
* USB to RS232 converter, such as https://www.sparkfun.com/products/11304
* [Jasch's](http://www.jasch.ch/) [toascii] Max external.

### Other Notes
* Designed for sending same commands via three USB-Serial adapter, hence 3 serport menus. Check the serial port speed! In this project it's set to 9600 in case of Arduino-style hardware getting swapped in and uncertain cable lengths.
* Remember to use a null modem cable or mini adapter.
* You'll probably need a gender adapter at one end or the other.
* The [standalone] object will create a 'fat' app on building to account for machines without a Java runtime. It's not ideal, but it was necessary.