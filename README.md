Pocket Tester – Multi-Sensor Diagnostic Tool 
Pocket Tester is a portable, menu-driven sensor and protocol testing device built using Arduino UNO and an SSD1306 SPI OLED display.
It allows quick testing of common sensors and digital signals without writing new test code every time.

 Features:

Main Modes:

1)Protocol Mode:
  GPIO Test
  GPIO Activity Check
  I2C Scan (device presence check)

2)Component Mode:
  DHT11 Temperature & Humidity Sensor
  IR / Digital Sensor
  Ultrasonic Distance Sensor (HC-SR04)

3)Logic Probe Mode:
  Digital HIGH / LOW detection on test pin

User Interface:
1)SSD1306 128×64 SPI OLED display
2)Button-based navigation:
  UP
  DOWN
  ENTER

Clean menu system with back navigation.
Pin-information screen before running each sensor test.



Hardware Required:
Arduino UNO1SSD1306-1
OLED (SPI, 128×64)-1 
Push Buttons-3 
Resistors (optional pull-ups)
As needed Jumper Wires.

Pin Connections:
OLED:
Vcc     -    5v
GND     -    GND
D0/SCK  -    D13
D1/MOSI -    D11
CS      -    D10
DS      -    D9
RST     -    D8

Buttons:
UP      -    D2
DOWN    -    D3
ENTER   -    D4


Note: Pin D1 is normally used for Serial TX.
Avoid using Serial Monitor while testing the ultrasonic sensor.


How to Use
Power On
OLED displays Pocket Tester splash screen
Automatically enters Main Menu

Navigate Menus
UP / DOWN → Move selection
ENTER → Select option / Go back


 Protocol Mode
GPIO Test → Reads logic level on test pin
GPIO Activity → Checks signal toggling
I2C Scan → Displays connected I2C devices


 Component Mode
Select sensor
View pin connection info
Press ENTER to run test
Results displayed on OLED

 Logic Probe Mode
Shows live HIGH / LOW state of test pin (D6)



Software Architecture:
Finite State Machine (FSM)
Non-blocking menu navigation
Safe button debouncing
Optimized SRAM usage for Arduino UNO
No dynamic memory allocation




Libraries Used:
Adafruit SSD1306
Adafruit GFX
DHT Sensor Library
SPI (built-in)

Install via Arduino Library Manager.




Important Notes
Ensure correct OLED SPI wiring
Avoid blocking code outside controlled delays
Button handler arrays sized correctly to prevent SRAM corruption
Designed specifically for Arduino UNO





Future Improvements
EEPROM-based pin remapping
Auto sensor detection
Battery voltage monitoring
Logic analyser waveform view
Support for I2C OLED variant




License
This project is open-source and free to use for educational and personal projects.


Author
Pocket Tester
Developed by: TechBots-SIT
Platform: Arduino UNO
Display: SSD1306 SPI OLED

