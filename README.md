# TroyHacks customized arduino-esp32

Use at own risk, crazy personal experiments mostly customized for ONLY the ESP32-S3

(likely will NOT work with other ESP32 variants)

Check commits for hints.

Usage:

```
platform_packages =  platformio/framework-arduinoespressif32 @ https://github.com/troyhacks/arduino-esp32.git#release/v2.x @ 2.0.17+sha.{commit}
  toolchain-riscv32-esp@~12.2
  toolchain-xtensa-esp32s3@~12.2
board_build.arduino.upstream_packages = no
```

Toolchain lines are optional, but used during all testing.
