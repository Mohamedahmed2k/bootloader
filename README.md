# STM32 Blue Pill Bootloader Project README

## Introduction
This README provides comprehensive instructions for setting up a bootloader on the *STM32 Blue Pill* microcontroller. The guide covers the setup process, connections, and instructions for flashing the bootloader, enabling programming via the micro USB port.

### Prerequisites
Before starting, ensure you have the following components:

1. *Hardware*:
   - STM32F103C8 (Blue Pill) board
   - USB-TTL converter (or FTDI programmer)
   - Connecting wires
   - Breadboard
   - 1.5k ohm resistor (if needed)

2. *Software*:
   - [STM32 Flash Loader](https://www.st.com/en/development-tools/flasher-stm32.html)
   - [STM32 USB Mini Driver](https://www.st.com/en/development-tools/stsw-stm32102.html)
   - [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)

## Circuit Setup
1. Connect your STM32 Blue Pill to the USB-TTL converter as follows:
   - *USB-TTL Converter*:
     - VCC → 3.3V
     - GND → GND
     - RX → PA9
     - TX → PA10

2. Move the *BOOT jumper* on the Blue Pill from position 0 to 1 to enter programming mode.

## Uploading the Bootloader
To upload the Maple bootloader to your STM32 Blue Pill:

1. Plug in the USB-TTL converter to your computer.
2. Download the TestBootloader.bin file from the **python script**
3. Download the [STM32 Flash Loader](https://www.st.com/en/development-tools/flasher-stm32.html).
4. Open the STM32 Flash Loader, which will detect the connected COM port.
5. Follow the on-screen instructions to flash the bootloader.

## Testing the Bootloader
1. Disconnect the USB-TTL converter after flashing.
2. Reconnect the Blue Pill to your computer via the micro USB port.
3. Program your STM32 Blue Pill using tools like *Arduino IDE* or *STM32CubeIDE*.
