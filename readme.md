Arduino shield for CaBot
=============================
![alt text](https://github.com/RealCabot/simplePCB/blob/master/PCB_layout.PNG "PCB")
This shield fits on top of an Arduino Mega. It provides breakouts for the sensors listed below, and fuses to protect the motor driver and motors. The PCB can be connected to a [L298 motor driver](https://solarbotics.com/product/k_cmd/) or a [Sabertooth 2x12 motor driver](https://www.dimensionengineering.com/products/sabertooth2x12).

**Parts list:**
See Excel file: "simple_component_list.xlsx"

**Sensors:**
1) [IMU](https://www.adafruit.com/product/2472)
2) [Touch Sensor](https://www.adafruit.com/product/1982)

**Connections**
1) M1_PWR (motor 1 power) <---> motor 1 positive and negative connections on motor driver
2) M2_PWR (motor 2 power) <---> motor 2 positive and negative connections on motor driver
3) GND (next to 5V) <---> GND on motor driver (this should be common GND)
4) 12V <---> 12V power supply
5) GND (next to 12V) <---> GND of 12V power supply (this should be common GND)
6) Connect Arduino's digital pins to the appropriate inputs on the motor driver. The pins will be different depending on whether you're using the L298 or Sabertooth (RTFM).
**If the motors are running the wrong direction, reverse the polarity**

**Known Issues**

1) The Arduino may disconnect from the laptop when running rosserial. Unfortunately, I don't know what's causing this. This has only happened once during our testing.
2) Current spikes may cause the fuse to blow (CaBot will stop moving). You must replace the 12V fuse if this happens. **You MUST use a 3A fuse with the L298 Motor Driver, otherwise it will burn out.** The Sabertooth can use up to a 20A fuse.
