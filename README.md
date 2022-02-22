# mini-weather
ESPHome based weather display
This is my ESPHome based weather station display, it’s main function is to display the details of the wind, but it also displays other values from my Ecowitt weather station.

When I bought the weather station I went cheap and got the wifi only version (i.e. no display). This is fine if I want to fire up HA and have a look, but I wanted something for the kitchen counter top.

![7a3d397a013ce5c1ca4b88116dd378262e462826_2_278x500](https://user-images.githubusercontent.com/41406374/155094191-fa5aa1d2-16db-402f-b751-a5232a406424.jpeg)

The hardware comprises of:

 - 2.2" TFT display with ili9341 controller
 - ESP32 Devkit V1
 - Micro PIR

From the top down, the display shows:

  - Current time
  - Current outside temperature
  - Compass rose with wind direction and strength indicator
  - Wind trend lines
  - Named wind direction and speed
  - Wind gust as reported by the weather station - “G” (last 20 sec max)
  - Trend display maximum - “TM” (this is the speed that the longest trend line represents)
  - Rainfall since midnight
  - Current air pressure

The display will go to sleep if not trigger by the motion sensor for 5 mins.

The software also attempts to prevent burn-in of the display.

This is a fairly simple project, the main things of note are the calculations for displaying the direction marker and the code for storing and displaying trend lines.

Pin connections for hardware are for a ESP32 Devkit V1
