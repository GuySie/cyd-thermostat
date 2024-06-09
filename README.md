# cyd-thermostat
ESPHome/Home Assistant based thermostat controller for Cheap Yellow Display (CYD).

![cyd-thermostat in action!](https://raw.githubusercontent.com/GuySie/cyd-thermostat/main/cyd-thermostat.jpg)
*CYD thermostat controller controlling my studio thermostat*

The "ESP32-2432S028R", an ESP32 with a built in 320 x 240 2.8" LCD display with touch screen, is colloquially known as the "Cheap Yellow Display" or CYD. It's about $15 delivered and offers an easy, no-solder touch display to control your smart home. It is supported in ESPHome and can be used to easily visualize Home Assistant entities and control Home Assistant itself, straight out of the box. You can find out more about the CYD on [Brian Lough's CYD repository](https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display), check out this [Hackster article](https://www.hackster.io/news/brian-lough-looks-to-build-a-community-around-the-espressif-esp32-powered-cheap-yellow-display-66d23972910d), or watch Brian's video on YouTube:

[![Cheap and Easy to Use ESP32 Screen!](http://img.youtube.com/vi/0AVyvwv0agk/0.jpg)](http://www.youtube.com/watch?v=0AVyvwv0agk "Cheap and Easy to Use ESP32 Screen!")

This code is my first experiment to create a thermostat controller on a CYD, programmed using ESPHome and connected to a thermostat in Home Assistant.

# Installation

- Follow normal ESPHome instructions. 
- Copy the yaml code into a new ESPHome project.
- Modify the substitutions. Pay particular attention to:
- `thermostat_entity:` Fill in the climate entity in Home Assistant that you are controlling with this CYD.
- `temperature_entity:` Fill in the current temperature sensor you want to display. The sensors built into TRV climate entities are often too sensitive to heat (close to the radiator) and cold (close to windows) so it's better to use a temperature sensor located more centrally in the room for accurate readings.
- If you still want to use the current temperature sensor built into your climate entity, scroll down to the `sensor:` part of the yaml code. There is a replacement block of code you can use in the comments.
- You need to the connect the CYD by cable for the first flash of an ESPHome firmware; all future updates are flashed over-the-air.

ESPHome no longer lets devices make Home Assistant service calls by default. Because the thermostat commands used here are service calls, you will need to turn this on manually for every new device:

Go to: Settings > Devices & Services > ESPHome > Configure (on the right of your CYD device) > turn on "Allow the device to make Home Assistant service calls."

![ESPHome device service calls window!](https://raw.githubusercontent.com/GuySie/cyd-thermostat/main/cyd-servicecalls.png)

# Thanks
This code is based on the ESPHome example code by [Jonny Bergdahl](https://github.com/jonnybergdahl).
