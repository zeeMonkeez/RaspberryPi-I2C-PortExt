RaspberryPi-I2C-PortExt
=======================

This is an I2C 8bit port extender for RaspberryPi using an MCP23008.

Using an appropriate header/socket (e.g. SAMTEC ESQ-113-24-T-D, Farnell 1930727) the module is stackable.
Pinheader X3 can be fitted to select the address of the MCP with jumpers. If not fitted, wire jumpers have to be soldered in.
X4 can be soldered in so the /RST and INT lines can be connected to GPIO lines.
The I2C lines and /RST are protected by MOSFETs (according to NXP's application note). INT is level shifted using a 74LVC1G07DCK buffer. The buffer's output again is protected through R6 against accidentally setting the GPIO it's connected to as an output.
If /RST is not needed, T3 and R4 do not have to be fitted. If INT is not needed, IC2 and R6 can be left out.
For C1/C4 and C2/C3, SMD or through hole components can be used.

License
-------
<a rel="license" href="http://creativecommons.org/licenses/by-sa/2.0/uk/"><img alt="Creative Commons Licence" style="border-width:0" src="http://i.creativecommons.org/l/by-sa/2.0/uk/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/2.0/uk/">Creative Commons Attribution-ShareAlike 2.0 UK: England &amp; Wales License</a>.

<a target="_blank" href="http://freedomdefined.org/OSHW"><img width="100" alt="OSHW" src="http://summit.oshwa.org/files/2012/04/oshw-logo-100-px.png"></a>

&copy;2012 Jonas Zimmermann.
