# TroyHacks Experimental P4 build

Mostly this exists to support my porting of [WLED to the ESP32-P4](https://github.com/troyhacks/WLED/tree/P4_experimental), so may not work for every feature as I haven't tested it across all use cases.

I do include the features for enabling WiFi (and likely Bluetooth) via the ESP32-C6 which is included on several of these boards.

Works with all ESP32-P4 boards I can get my hands on - the [Espressif ESP32-P4 EV](https://docs.espressif.com/projects/esp-dev-kits/en/latest/esp32p4/esp32-p4-function-ev-board/user_guide.html) board, the [Waveshare ESP32-P4 Nano](https://www.waveshare.com/esp32-p4-nano.htm), and the [Olimex ESP32-P4-Devkit](https://www.olimex.com/Products/IoT/ESP32-P4/ESP32-P4-DevKit/open-source-hardware). 

**Note:** _Currently generic Serial monitor over USB doesn't work "out of the box" with the Olimex ESP32-P4-Devkit as it has a Serial+JTAG USB port. This library is compiled for that feature - perhaps I just don't know how to use it._ Code uploads and runs just fine tho otherwise.

Libraries are stored separately now, hosted at https://github.com/troyhacks/esp32-arduino-libs/

## PlatformIO Usage:

```
platform                =  https://github.com/troyhacks/platform-espressif32#Arduino/IDF5
platform_packages       =  framework-arduinoespressif32 @ https://github.com/troyhacks/arduino-esp32#feature/esp32p4
                           framework-arduinoespressif32-libs @ https://github.com/troyhacks/esp32-arduino-libs#main
                           toolchain-riscv32-esp @ https://github.com/espressif/crosstool-NG/releases/download/esp-13.2.0_20240530/riscv32-esp-elf-13.2.0_20240530-x86_64-w64-mingw32.zip
board_build.arduino.upstream_packages = no
board                   =  esp32p4
board_build.mcu         =  esp32p4
board_build.f_cpu       =  360000000L
```

**(This readme might not always be up-to-date)**
