# PeripheralSOMPCB
The Peripheral System on Module takes in the SPI or I2C of the various Peripheral boards and sends that along a can bus.

## Daughter Board Connector Pinout Usage Guide
 * SPI1 is the main SPI
 * I2C1 is the main I2C
    * These pins cannot be used as GPIO due to pullups
 * SPI2 is a secondary SPI, used only if necessary
    * Primary usage for SPI2 should be GPIO
 * I2C2 is a secondary I2C, used only if necessary
    * Primary usage for I2C2 should be GPIO
    * To use these pins are I2C you must use the JP1, JP3 headers to pull up to 3.3V
 * PA1, PA2, and SPI1_NSS can be used as ADC inputs
 * VDDA and GNDA should be used only for voltage reference
    * Drawing significant current will result in unstable voltage output

## BOM
[**BOM**](bom/BPS-PeripheralSOM.csv)  
[**IBOM**](bom/ibom.html)  

## PCB
![image](https://github.com/lhr-solar/BPS-PeripheralSOMPCB/blob/docs/BPS-PeripheralSOM_PCB.png?raw=true)

## Schematic
[**PDF with all sheets**](BPS-PeripheralSOM_SCH.pdf)

## Version History
### V1.0: 
Using STM32L4CBT1 with 2 I2C, 2 SPI, 1 CAN, 1 UART (USB)
### v1.1:
Add ADC pins as a quick hotfix
### v2.0:
Updated UART-> USB chip and moved to a 12V architecture


