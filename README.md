# DIY SpO2 Monitor

A pulse oximeter (SpO2 + heart rate) built around an Arduino Nano and a MAX30102 sensor, with a custom 4-layer PCB designed in KiCad. College project.

![PCB layout](docs/images/pcb_layout.png)


## Overview
SpO2 is the percentage of hemoglobin carrying oxygen (normal is about 95-100%). The MAX30102 shines red and infrared light through the fingertip, and the ratio of the pulsating (AC) to steady (DC) components of each signal is used to estimate SpO2. The same signal gives heart rate.

## Hardware
| Block | Part | Interface |
|---|---|---|
| Microcontroller | Arduino Nano v3.x | - |
| Sensor | MAX30102 module | I2C |
| Display | SSD1306 OLED | I2C |
| Input | 3 push buttons (MENU / UP / DOWN) with RC debounce | GPIO |
| Indicator | Alarm LED | GPIO |

- Both I2C devices share SDA/SCL (A4/A5).
- Powered from the Nano's 5V rail (USB).
- Custom KiCad footprints made for the MAX30102 and SSD1306 modules.

## Schematic
![Schematic](docs/images/schematic.png)

## Repository Contents
- `hardware/`: KiCad project files (schematic, PCB, custom footprints)
- `docs/`: schematic and PCB images
- `firmware/`: Arduino code (to be added)

## Status
PCB designed and routed in KiCad. Firmware, test results and fabrication files will be added.

## TODO
- [ ] Add firmware
- [ ] Add board dimensions and test results
- [ ] Add BOM, Gerbers and photos of the built board

## Disclaimer
Educational project only, not a medical device.

## License
MIT
