# Installing Micropython on an ESP32.

## Prerequisites
- [esptool](https://docs.espressif.com/projects/esptool/en/latest/esp32/) installed via pip or the github releases.
- [mpremote](https://docs.micropython.org/en/latest/reference/mpremote.html)
- [Micropython Firmware](https://micropython.org/download/ESP32_GENERIC/), [Direct Download v.1.25.0](https://micropython.org/resources/firmware/ESP32_GENERIC-20250415-v1.25.0.bin)

## Flashing the Firmware
1. Connect the ESP32 to your computer via USB.
2. Open a terminal and run the following command to erase the flash memory:
   ```bash
   esptool.py  erase_flash
   ```
3. Flash the Micropython firmware using the following command:
   ```bash
    esptool.py --baud 460800 write_flash 0x1000 ESP32_GENERIC-20250415-v1.25.0.bin
    ```
4. Test if everything worked with mpremote:
   ```bash
   mpremote
   ```

## Further information
- [Official Documentation](https://micropython.org/download/ESP32_GENERIC/)
