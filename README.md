# Portable Weather Station PCB Created With KiCAD 9
A custom designed portable weather station PCB that integrates the use of multiple sensors, real time data visualization, and user interaction.
I built this to explore deeper concepts of embedded systems and hardware as a whole, I wanted more expirence in data visualization on a display, power efficient programming on a microcontroller, and end to end hardware development.
 
This system displays and updates weather and time related information in real time using a flicker free responsive UI that includes dynamic weather icons that correspond to the current time of day along with a toggle switch that the user can flip to toggle a light and dark mode to better suit their current environment.
<br>
 
TFT displays tend to run into the issue of flickering whenever updating data quickly on a slower microcontroller like the Arduino Nano, when working on this project I ran into the issue of the display constantly flickering when updating the data. To get past this issue I came up with implementing a conditional system to only update data when detecting change in sensor values instead of updating it constantly in the loop function which better optimized the system as well.
 
This system was designed entirely from scratch (started as bread-perfboard & converted to PCB) and all components were selected for compatibility and the PCB includes custom made symbols and footprints for each of the components along with labeling on the silkscreen for clarity
 
This board is meant to operate at 5V (via mini USB connection), this system uses I2C to communicate to the RTC module along with SPI to communicate with the ST7735S TFT display. Mounting holes are present at each corner of the board for M2 screws. <br>
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
- Power bank (5000 MaH)
- 6 in mini USB cable

## Software Related
- Arduino IDE
- C++ (custom functions for optimizing display logic (only updating stuff when needed), managing toggle switch states, and for drawing UI upon start of system to correspond with initial switch state)
- KiCAD 9 (Used for schematic design, creating custom symbols and footprints for componenets, mixed signal routing, and validating ERC & DRC)
- Various libraries for components:
 - Adafruit GFX
 - Adafruit ST7735
 - RTCLib
 - DHT
- Gerber File generation for manufacturing (manufactured using PCBWay)

# Custom Footprints
Footprints were created for the PCB based on the exact physical measurments of the components in mm for accurate pad and pin allignments (2.54 mm spacing between pads)

- DHT-11: 14.5mm X 29mm (W X L)
- MQ-135: 20mm X 32mm (W X L)
- DS3231 RTC: 22mm X 38.5mm (W X L)
- ST7735S TFT Display: 30mm X 43.5mm (W X L)

# System Features
## Displays Current:
+ AM/PM formatted time (PST)
+ Day of week
+ Date (MM/DD/YYYY)
+ Temperature (F|C)
+ Humidity (%)
+ General air quality

## Time Responsive Icons 
+ Morning Icon: 6 AM - 3 PM
+ Afternoon Icon: 4 PM - 6 PM
+ Evening/Night Icon: 7 PM - 5 AM

## User Responsive UI/THEME Toggle
+ Manual toggle switch that allows user to switch theme of system

# System Preview

<img src = "https://github.com/user-attachments/assets/dde273cc-182d-4e56-90b9-a000ba16ea54" width = "550" height = "550"/> 
<img src = "https://github.com/user-attachments/assets/4f40f132-bb81-4a42-82a9-b12d7365d039" width = "550" height = "550"/>



https://github.com/user-attachments/assets/ecc253c0-51ab-447f-b8cf-1e997ebe2ff8

# Perfboard Prototype
<img width="550" height="550" alt="weatherStationPerf" src="https://github.com/user-attachments/assets/ddf8209c-aeb4-44ee-9170-c10dc0df8f23" />





