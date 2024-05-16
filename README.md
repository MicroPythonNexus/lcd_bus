# lcd_bus
Bus drivers for [MPDisplay](https://github.com/bdbarnett/mpdisplay) on MicroPython.  API compatible with Kevin Schlosser's [mplcd_bus], which is currently under development and included as part of his [LVGL MicroPyton](https://github.com/kdschlosser/lvgl_micropython) port.

lcd_bus currently has drivers for SPI and i80 buses.  It may have I2C buses added later.  It likely will never have RGB buses added due to the timing requirements which are much better implemented in C than MicroPython.

The bus drivers have been tested extensively on ESP32 and RP2040 platforms, but are written to work with all microcontrollers that have enough processor and RAM resources to support displays.  There may be issues with those microcontrollers, and I ask you to leave your feedback on [MPDisplay's discussion board](https://github.com/bdbarnett/mpdisplay/discussions).

The constructor signature of SPIBus is the same as CircuitPython's FourWire class.  The constructor signature of I80Bus is the same as CircuitPython's ParallelBus class.  The API is different in order to maintain compatibility with Kevin Schlosser's work.
