# SDC40-Read-and-Cache

A handful of arduino scripts to save, read, and clear C02 and humidity readings from on-board EEPROM

## Scripts 👨🏽‍💻

- c02_humidity_to_eeprom:\tCompress and save the SDC40 co2 and humidity to 4-bits each, combined into a single 8 bit write
- eeprom_to_csv:\t\tRead and uncompress the readings saved on the arduino's EEPROM
- clear_eeprom:\n\nReset all EEPROM addresses to 255, their original value when empty.

## Instructions 📜

0. Set the arduino Serial Monitor baud rate to 1200.
1. Upload and run *c02_humidity_to_eeprom* for at least 30 seconds.
2. Launch and recover le balloóń.
3. (optional) Set the arduino Serial Monitor baud rate to 19200
4. Upload and run the eeprom_to_csv sketch until it stops outputting data, or starts outputing 250 a bunch of times.
5. Upload and run the clear_eeprom sketch to remove all old readings and format the arduino EEPROM.

## Notes to the team 📝

- If you choose to follow step 3, you need to change the baud rate in Serial.begin(...) to 19200 as well. I found this to be worth it because it speeds the read and delete times way up.
- The read and write scripts output CSV data to the serial monitor, just clear the monitor and use *CRTL+a* to copy it all at once.
