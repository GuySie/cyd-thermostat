# cyd-thermostat
ESPHome/Home Assistant based thermostat controller for Cheap Yellow Display (CYD).

The "ESP32-2432S028R", an ESP32 with a built in 320 x 240 2.8" LCD display with touch screen, is colloquially known as the "Cheap Yellow Display" or CYD. It's about $15 delivered and offers an easy, no soldering, touch display to control your smart home with. It is supported in ESPHome and can be easily used to visualize Home Assistant entities and control Home Assistant itself, straight out of the box. Connect it once by cable to flash an ESPHome firmware, then do future updates over-the-air. You can find out more about the CYD on [Brian Lough's CYD repository](https://github.com/witnessmenow/ESP32-Cheap-Yellow-Display), check out this [Hackster article](https://www.hackster.io/news/brian-lough-looks-to-build-a-community-around-the-espressif-esp32-powered-cheap-yellow-display-66d23972910d), or watch Brian's video on YouTube:

[![Cheap and Easy to Use ESP32 Screen!](http://img.youtube.com/vi/0AVyvwv0agk/0.jpg)](http://www.youtube.com/watch?v=0AVyvwv0agk "Cheap and Easy to Use ESP32 Screen!")

This code is a first experiment to create a thermostat controller with a CYD, based on the ESPHome example code by [Jonny Bergdahl](https://github.com/jonnybergdahl).
