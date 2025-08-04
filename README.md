# Portable WeatherStation PCB Created With KiCAD 9
A fully functional custom designed portable weather station PCB that integrates the use of multiple sensors, real time data visualization, and user interaction.
I built this to explore various concepts of embedded systems, I wanted more expirence in data visualization on a display and power efficient programming on a microcontroller.
This system displays and updates weather and time related information in real time using a flicker free responsive UI that includes dynamic weather icons that correspond to the current time of day along with a toggle switch that the user can flip to toggle a light and dark mode to better suit the current enviorment of the user.
<br>
 
TFT displays tend to run into the issue of flickering whenever updating data quickly on a slower microcontroller like the Arduino Nano, when working on this project I ran into the issue of the display constantly flickering when updating the data To get past this issue I came up with implementing a condtional system to only update data when detecting change in sensor values instead of updating it constantly in the loop function which better optimized the system as well.
 
This system was designed entirly from scratch (converted perfboard to PCB) and all components were selected for compatibility and the PCB includes custom made symbols and footprints for each of the components  along with labeling on the silkscreen of the PCB for clarity
 
This board is meant to operate at 5v (via mini USB connection), this system uses I2C to communicate to the RTC module along with SPI to communicate with the ST7735S TFT display for fast user updates. Mounting holes are present at each corner of the board for M2 screws. <br>
*created by: Bryan Diaz | Focus: Embedded Systems, Hardware and PCB Design*

# Technologies and Components
## Hardware Related
- Arduino Nano
- DS3231 Real Time Clock Module
- MQ-135 (air quality sensor)
- DHT-11 (temp & hum sensor)
- ST7735 1.44" TFT display (operates using SPI)
- Toggle Switch (to toggle between themes: *switch facing up: light/day theme; switch facing down: dark/night theme*)
- Custom 2 layer PCB (designed in KiCAD 9)
- Soldering of through hole components
- Power bank (5000 MaH) & 6 in mini USB cable
