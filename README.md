# Water-Level-Pressure-Transducer *BUILD-NOTES*
1) calculates water level height up to 50 KPA of pressure using Freescale Semiconductor MPX5500DP
2) measures water temp with DSB1820 1-Wire Digital Thermometer 
3) sample hose is driven with a PARKER T2-03 micro diaphragm pump / Air-Gas medical grade pump [10,000+ hour rating]
4) Motion sensor is a PARRALAX MINI SENSOR 28033 - Pir turns on LCD and prevents air pump cycle when motion is detected
5) Motor and Fan are controlled by a DROK L298N Motor Drive Controller Board DC Dual H-Bridge
6) LCD is a SainSmart IIC/I2C/TWI 1602 Serial LCD Module
7) Processing is done with (YUN) ATmega32U4 microcontroller and Atheros AR9331 (Linux part) 5v & VIN diodes were removed
8) Main fuse is a Bussmann GMA-1A 1 Amp Glass Fast Acting Cartridge Fuse, 250V UL Listed
9) Thermal protection consist of a KSD9700 NC 45C Bimetal Thermostat Temperature Switch (113*F Cuts Main Power)
10) Enclosure = Hammond 1591ESBK ABS
11) 5 Volt Vin Power = Pololu 5V, 1A Step-Down Voltage Regulator D24V10F5
12) Cooling fan = 40x40x10mm, Ball Bearing, 3-pin 12-volt
13) Power supply is a 12-volt 1-amp UL Listed switching step down transformer
--------------------------------------------------------------------------------------------------------------------------
System updates measured readings once every 60 minutes to https://thingspeak.com/plugins/11756
If motion is detected updates and samples will be delayed as long is motion is present 
Motion will not turn on LCD for 10 seconds while Air pump is cycling and reading is taking place
Normal operating temperature inside enclosure is 92*F at 70*F ambient air temperaturet
Fan Will turn on at 95*F and will cycle until enclosure drops to 85*F or below (Main power cut-out @ 113*F)
Transducer accuracy @ (0 to 85°C) = (±2.5%) -- Testing showed results within ± 1/2" after math conversions
