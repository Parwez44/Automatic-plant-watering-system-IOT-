# Automatic Plant Watering System  
A simple Arduino-based project that waters your plant whenever the soil gets too dry.  
Great for beginners, hobbyists, or anyone (like me 😅) who forgets to water their plants on time.



# What This Project Does
This setup uses a soil moisture sensor to check how dry your plant’s soil is.  
If the soil crosses a certain dryness level, a relay automatically turns on a small water pump for a few seconds. After watering, it shuts off again.

Basically:  
**Dry soil → Pump ON → Watering → Pump OFF**

Super simple, surprisingly useful.



# Components Used
You can use these or any equivalent parts:

- Arduino UNO  
- 5V Relay Module  
- Soil Moisture Sensor (analog type works best)  
- Small DC Water Pump + tube  
- Jumper wires  

Everything is pretty plug-and-play.



# Wiring (Quick Overview)
- Soil sensor → A0  
- Relay IN → D8  
- Relay VCC/GND → Arduino 5V/GND  
- Pump is powered through the relay (NO + COM terminals)

**Important:** If your pump uses an external power supply (like 9V/12V), make sure all grounds (Arduino + pump + relay) are connected together.


# Before You Run the Code (Important)
Every soil sensor gives slightly different values.  
So it's a good idea to calibrate the dryness threshold using Serial Monitor.

Here’s how:
1. Upload the code.
2. Open **Serial Monitor**.
3. Note the reading when the sensor is **in dry soil**.
4. Note the reading when the soil is **wet**.
5. Pick a number somewhere in between — that becomes your `DRY_THRESHOLD`.

I’ve set a default in the code, but you should tweak it for accurate results.



#  The Code
The full code is available in this repository.  
It’s clean, commented, and easy to modify — feel free to customize timings, threshold, or add features.



# How To Use
1. Upload the `.ino` file to your Arduino UNO.  
2. Watch Serial Monitor to check moisture values.  
3. Adjust the threshold if needed.  
4. Connect your plant, pump, and sensor… and enjoy automatic watering!  



# Things You Can Improve Later
- Add an OLED screen to show moisture level  
- Add WiFi (ESP8266/ESP32) to monitor remotely  
- Add a button for manual watering  
- Log moisture data over time  

This is a great beginner project if you're just getting into Arduino or home automation.


# License
Do whatever you want with this project — use it, modify it, build on it.  
A star ⭐ on the repo would be appreciated if you found it useful!

