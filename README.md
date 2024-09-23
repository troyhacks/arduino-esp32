# TroyHacks Experimental P4 build

...in theory with ESP-Hosted (v0.0.6) and ESP-Wifi-Remote which should work with the ESP32-P4 EV board.

## Usage:

```
platform                =  https://github.com/troyhacks/platform-espressif32#Arduino/IDF5
platform_packages       =  framework-arduinoespressif32 @ https://github.com/troyhacks/arduino-esp32#feature/esp32p4
                           framework-arduinoespressif32-libs @ https://github.com/troyhacks/esp32-arduino-libs#main
                           toolchain-riscv32-esp @ https://github.com/espressif/crosstool-NG/releases/download/esp-13.2.0_20240530/riscv32-esp-elf-13.2.0_20240530-x86_64-w64-mingw32.zip
                           toolchain-xtensa-esp32s3 @ https://github.com/espressif/crosstool-NG/releases/download/esp-13.2.0_20240530/xtensa-esp-elf-13.2.0_20240530-x86_64-w64-mingw32_hotfix.zip
board_build.arduino.upstream_packages = no
board                   =  esp32p4
board_build.mcu         =  esp32p4
board_build.f_cpu       =  360000000L
```

**(This readme might not always be up-to-date)**
