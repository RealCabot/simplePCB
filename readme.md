Arduino shield for CaBot
=============================
The motor driver is copied from the Solarbotics L298 driver: https://solarbotics.com/product/k_cmd/

Parts list: see Team G order sheet for parts requested on 1/3/18

Questions and comments for team/Navarro:
1) Should we connect the motor driver LDO 5V with the Arduino's 5V? 
	I think this means the Arduino will be powered from 12V (Arduino turned on whenever CaBot is powered on)
2) Will EMI from motor driver cause problems with the sensors?
	We can connect capacitors across motor terminals to reduce EMI
3) We need to protect against static shock. See included document: "ESD considerations for touch sensing...": 
	i) Connect resistor in series with touch pad
	ii) Using Kapton tape to cover touch pad
