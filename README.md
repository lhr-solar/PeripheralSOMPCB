# BPS-PeripheralSOMPCB
The BPS Peripheral System on Module takes in the SPI or I2C of the various Peripheral boards and sends that along a can bus. Used primarily by BPS and Data Acquisition

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
 * PA1, PA2, and SPI1_NSS can be used as ADC inputs
 * VDDA and GNDA should be used only for voltage reference
    * Drawing significant current will result in unstable voltage output

## Connectors
| # | Name | Type | Pin 1 | 2 | 3 | 4 | 5 | 6 | Purpose |
| - | - | - | - | - | - | - | - | - | - |
| J1  | SWD | 1x4xP2.54mm Female | +3.3V | SWCLK | SWDIO | GND | | | Flashing |
| J2  | CAN_In | 436500244 | 5V | GNDPWR | Can High | Can Low ||| Input for CAN and Power |
| J3  | USB  | 105017-0001 | VBus | D+ | D- | ID | | | USB Debugging |
| J4  | CAN_Out | 436500244 | 5V | GNDPWR | Can High | Can Low ||| Output for CAN and Power |
| J6  | | | | | | | | | Daughter Board Connector |

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
| TP1 | 3.3V |
| TP3 | 5V PWR |
| TP4 | GND PWR |
| TP6 | Isolated GND |

## BOM
[**BOM**](BPS-PeripheralSOMBOM.xls)  
[**IBOM**](bom/ibom.html)
[**Mouser Cart**](https://www.mouser.com/ProjectManager/ProjectDetail.aspx?AccessID=29ec1c3dbf)

## PCB
![image](https://github.com/lhr-solar/BPS-PeripheralSOMPCB/blob/docs/BPS-PeripheralSOM_PCB.png?raw=true)

## Schematic
[**PDF with all sheets**](BPS-PeripheralSOM_SCH.pdf)