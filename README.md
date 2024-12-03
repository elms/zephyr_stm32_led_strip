# Demonstrating `stm32_min_dev` LED strip

Using the [stm32 blue
pill](https://docs.zephyrproject.org/latest/boards/others/stm32_min_dev/doc/index.html),
pin `A7` pin for the data to WS2812 LED strip. Make sure to have the
ground of LED strip common with the LED power source. For
low-intensity and short strands, the 5V on the blue pill is
sufficient.

## Notes

To change the duration, run `west build -t menuconfig`. This allows
you to set the duration. This is also saved in `build/zephyr/.config`.

### UART
UART is on PA9 and PA10.

Tested using command `screen /dev/ttyUSB0 115200 8n1`

#### Example output
```
*** Booting Zephyr OS build v3.7.0-5545-g9f93dede369c ***
[00:00:00.000,000] <inf> main: Found LED strip device ws2812@0
[00:00:00.000,000] <inf> main: Displaying pattern on strip
```
