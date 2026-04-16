<img width="1012" height="718" alt="aethernodeS3view" src="https://github.com/user-attachments/assets/4a5db4b3-947f-40ff-b6ce-806dbb32cabb" />

A Reticulum Network stationary transport/discovery enabled node - RRNode. Designed around OrangePI Zero LTE, an ESP32 S3 and a CDEBYTE E22-XXXM33S LoRa radio. 
⚪ Built in power supply block, that takes from 18VDC to 53VDC, being designed for the nominal Power Over Ethernet(PoE) voltage of 48VDC, and provides 5V@6A to power the RNode and the SBC, running RNS. 
⚪ Up to 33dBm (2W) of output power.
⚪ I2C header for 0.96" RNode display for install and debug, standard QWIIC connector with options for 3.3V and 5V power (zero resistor selectable for I2C sensors, in daisy chain with the display port.
⚪ Two options for TX/RX module control:
1) DIO2 based control with an external transistor inverter to control also the RXEN pin. (REMOVE R3/R4 if selected!)
2) TXEN/RXEN external control of the module via pins G17/G16. (REMOVE R2/Q1 if selected!)

NOTE: While the power supply on the PCBA is capable of withstanding 75V input voltage, the protection diode D1 is set to conduct at around 55VDC. This allows ample window for standard 48V PoE voltage. If one uses battery backup, for example Lead-Acid, the output voltage of a fully charged set would be around 55-57VDC and this WILL cause D1 to conduct and short the PS. If one uses such backup, change D1 to SMCJ58A, which will conduct at around 67VDC and will not interfere with normal operation under such backup.
