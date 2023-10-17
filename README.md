# BPS-PeripheralSOMPCB
The BPS Peripheral System on Module takes in the SPI or I2C of the various BPS boards (Volttemp and Amperes) and sends that along a can bus.

## Daughter Board Connector Pinout Usage Guide
 * SPI1 is the main SPI
    * If additional GPIOs are necessary, avoid using SPI1_MOSI and SPI1_SCK due to terminating resistors.
 * I2C1 is the main I2C
    * These pins cannot be used as GPIO due to pullups
 * SPI2 is a secondary SPI, used only if necessary
    * Primary usage for SPI2 should be GPIO
 * I2C2 is a secondary I2C, used only if necessary
    * Primary usage for I2C2 should be GPIO
    * Enable external Pullups () to use as I2C bus
PA1, PA2, and SPI1_NSS can be used as ADC inputs
VDDA and GNDA should be used only for voltage reference
 * Drawing significant current will result in 
 * unstable voltage output

## Connectors
| # | Name | Type | Pin 1 | 2 | 3 | 4 | 5 | 6 | Purpose |
| - | - | - | - | - | - | - | - | - | - |
| J1  | SWD | 1x4xP2.54mm Female | +3.3V | SWCLK | SWDIO | GND | | | Flashing |
| J2  | CAN_In | 430450612 | Can Voltage | Can High | External 5V | Can GND | Can Low | Power GND | Input for CAN and Power |
| J3  | USB  | 105017-0001 | VBus | D+ | D- | ID | | | USB Debugging |
| J4  | | | | | | | | | Daughter Board Connector |
| J5  | CAN_Out | 430450612 | Can Voltage | Can High | External 5V | Can GND | Can Low | Power GND | Input for CAN and Power |


## Switches LEDs
| # | Purpose |
| - | - |
| D2  | 3.3V LED |
| D4  | Heartbeat LED |
| D12 | Extra LED |
| D13 | Extra LED |
| D14 | Extra LED |
| SW1 | Reset Switch |
| SW2 | Single Pole Double Throw Switch |
| SW5 | Push Button Switch |

## Testpoints
| # | Purpose |
| - | - |
| TP3 | 5V PWR |
| TP4 | GND PWR |
| TP5 | Isolated 5V |
| TP6 | Isolated GND |

## BOM
IBOM [TBA]  
Mouser Cart [TBA]

## PCB
[Image to be added]

## Schematic
[Image to be added]