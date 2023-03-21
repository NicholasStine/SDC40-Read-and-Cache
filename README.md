# SDC40-Read-and-Cache

A handful of arduino scripts to save, read, and clear C02 and humidity readings from on-board EEPROM

## Scripts:
- c02_humidity_to_eeprom:\tCompress and save the SDC40 co2 and humidity to 4-bits each, combined into a single 8 bit write
- eeprom_to_csv:\t\tRead and uncompress the readings saved on the arduino's EEPROM
- clear_eeprom:\n\nReset all EEPROM addresses to 255, their original value when empty.
