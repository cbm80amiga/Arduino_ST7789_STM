# Arduino_ST7789_STM
Fast STM32 SPI/DMA library for ST7789 240x240 IPS display

YouTube video (AVR Arduino): https://youtu.be/GciLKcWQZK4

Significantly optimized for STM32 boards. Supports 36MHz SPI and DMA channel

Developed and tested using Roger's stm32duino and Arduino IDE 1.6.5

## Configuration

Use "#define COMPATIBILITY_MODE" - then the library doesn't use DMA

Use "#define CS_ALWAYS_LOW" for LCD boards where CS pin is internally connected to the ground, it gives little better performance

## Extra Features
- invertDisplay()
- sleepDisplay()
- enableDisplay()
- idleDisplay() - saves power by limiting colors to 3 bit mode (8 colors)
- resetDisplay() - software reset
- partialDisplay() and setPartArea() - limiting display area for power saving
- setScrollArea() and setScroll() - smooth vertical scrolling
- fast drawImage() from RAM
- fast drawImageF() from flash (PROGMEM)

## Connections:

|LCD pin|LCD pin name|Arduino|
|--|--|--|
 |#01| GND| GND|
 |#02| VCC |3.3V|
 |#03| SCL |PA5|
 |#04| SDA|PA7|
 |#05| RES|PA0 or any digital|
 |#06| DC|PA1 or any digital|
 |#07| BLK | NC|

If you find it useful and want to buy me a coffee or a beer:

https://www.paypal.me/cbm80amiga
