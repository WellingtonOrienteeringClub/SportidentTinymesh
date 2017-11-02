# Components used in the Radio Unit


## Basic components to get a working unit up for lab/development purposes

SMA female connector for PCB mount
https://www.electrokit.com/sma-hona-pcb-4mm-djup.49423

Whip antenna for 169MHz with SMA male connector 
https://www.digikey.se/product-detail/en/taoglas-limited/FW.80.SMA.M/931-1195-ND/3664652

RC1701HP-TM	Tinymesh transciever module
http://www.actesolutions.se/sv/produkt/rcxxxx-tm (need to order via a company or organization)

https://www.digikey.com/product-detail/en/radiocrafts-as/RC1701HP-TM-DK/RC1701HP-TM-DK-ND/7100561 
https://www.digikey.com/product-detail/en/radiocrafts-as/RC1701HP-TM/RC1701HP-TM-ND/7100560 
(not possible to ship to sweden)
A demo kit is easiest to use for the Gateway, since it is a ready made appliance that you just connect to the PC with USB. 
But you could also design and build your own using a USB-to-UART cable and a Tinymesh module. 

Teensy-LC 
https://www.electrokit.com/teensy-lc.52909

## Connecting to a Sportident station

SRR dongel for connecting to SRR BSM station
http://www.sportident.se/order.aspx?id=472

Alternative: wired connection to RS232 BSM station
RS232-to-UART converter
https://www.electrokit.com/en/max3232-breakout.49804
RS323 connector
https://www.electrokit.com/en/dsub-9-conn-male.42706


## Non-mandatory extras
Teensy 3.2 may be an alternative to the Teensy-LC. The LC is cheaper, but the 3.2 has an internal voltage regulator that can feed more current (250mA) to power the Tinymesh module.
https://www.pjrc.com/teensy/external_power.html

Recommend headers for mounting the Teensy on the PCB when in the lab/design phase.
https://www.electrokit.com/stiftlist-2-54mm-1x40p-brytbar.43412
https://www.electrokit.com/hylslist-2-54mm-1x40p-svarvad-brytbar.44672

Some LEDs and resistors to connect to RSSI and CONN indicator outputs.

## For maximum outdoor range
To use full transmit power, an additional voltage regulator from the USB's 5V to the Tinymesh VCC_PA that takes 3.3V. I think a buck (switched step-down) converter is better than a linear since it is more energy efficient. It is a tradeoff between battery size and complexity of design. It needs to be able to output >800mA (gut feeling estimate). Note that you may need capacitors too, check the datasheet.

Slim Jim VHF antenna tuned for 169.4MHz with SMA male connector.
http://www.2wayelectronix.com/N9TAX-Original-VHF-Slim-Jim-antenna-VHF-STD.htm