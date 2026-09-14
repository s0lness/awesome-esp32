# Devices

It can be difficult knowing which device to get, so every entry in the [README](README.md) names the device it runs on and this file spells
each name and links where to buy it.

A device gets a section the first time one project uses it. Projects that run on a bare ESP32 plus parts, or on dozens of boards, name no device and are listed at the bottom.

## Waveshare ESP32-S3-Touch-AMOLED-1.8

ESP32-S3, 368x448 touch AMOLED, IMU, ES8311 audio codec, battery support. Shipped with
two panel controllers (SH8601 on V1, CO5300 on V2) that firmware must be built against;
the bus is write-only, so the board cannot report which one it has.
[Product page](https://www.waveshare.com/product/esp32-related/boards-kits/esp32-s3/esp32-s3-touch-amoled-1.8.htm) ·
[field guide](guides/waveshare-amoled-18.md)

## Waveshare ESP32-S3-Touch-AMOLED-1.75

ESP32-S3R8, 466x466 round touch AMOLED, QMI8658 6-axis IMU, PCF85063 RTC, AXP2101 PMIC,
dual microphones, battery support.
[Product page](https://www.waveshare.com/esp32-s3-touch-amoled-1.75.htm)

## Waveshare ESP32-S3-Touch-AMOLED-2.06

ESP32-S3R8, 410x502 touch AMOLED, QMI8658 6-axis IMU, battery support. Larger sibling of
the 1.8 and a different device: pin map, panel and drivers do not carry over.
[Product page](https://www.waveshare.com/esp32-s3-touch-amoled-2.06.htm)

## Waveshare ESP32-C6-Touch-AMOLED-2.16

ESP32-C6, 480x480 CO5300 touch AMOLED on QSPI, CST9217 touch, QMI8658 6-axis
IMU, AXP2101 PMIC, battery support. The PMIC gates the panel rails and its
ALDO3 doubles as the panel reset, so power-up ordering matters; Waveshare's
own ESP-IDF example gives LCD_CS as GPIO5, which is wrong for this board.
[Product page](https://www.waveshare.com/esp32-c6-touch-amoled-2.16.htm)

## Waveshare ESP32-S3-Touch-LCD-3.49B

ESP32-S3R8, 172x640 capacitive touch LCD, audio codecs, microphones, speaker output,
QMI8658 6-axis IMU, PCF85063 RTC and lithium polymer battery support.
[Product page](https://www.waveshare.com/esp32-s3-touch-lcd-3.49.htm)

## Waveshare RP2350-Touch-AMOLED-1.8

The same 368x448 touch AMOLED shell as the ESP32-S3 board, on an RP2350 instead. Present
here because projects port across the two rather than living on one.
[Product page](https://www.waveshare.com/rp2350-touch-amoled-1.8.htm)

## Waveshare ESP32-P4-ETH

ESP32-P4 with wired Ethernet and an ESP32-C6 radio co-processor.
[Product page](https://www.waveshare.com/esp32-p4-eth.htm)

## Waveshare ESP32-P4-Module-DEV-KIT

ESP32-P4 dev kit driving a 7-inch DSI touch panel.
[Product page](https://www.waveshare.com/esp32-p4-module-dev-kit.htm)

## M5StickS3

ESP32-S3 stick with a small display, IMU, microphone and battery.
[Product page](https://shop.m5stack.com/products/m5sticks3-esp32s3-mini-iot-dev-kit)

## M5Stack StopWatch

ESP32-S3R8 round 1.75" 466x466 AMOLED touch, two buttons, vibration motor, ES8311 audio, BMI270 IMU, 450mAh battery.
[Product page](https://shop.m5stack.com/products/m5stack-stopwatch-dev-kit-esp32-s3)

## M5Stack CoreS3

ESP32-S3 in the stackable Core case: 320x240 touch screen, IMU, camera, microphone,
speaker, battery base.
[Product page](https://shop.m5stack.com/products/m5stack-cores3-esp32s3-lotdevelopment-kit)

## M5Stamp Pico

ESP32-PICO stamp-sized module meant to be soldered into a build rather than sit on a desk.
[Product page](https://shop.m5stack.com/products/m5stamp-pico-diy-kit)

## M5Stack AtomS3R-CAM

ESP32-S3 with 8MB PSRAM and a GC0308 camera in the Atom footprint, roughly a 24mm cube.
[Product page](https://shop.m5stack.com/products/atoms3r-camera-kit)

## M5Stack Atom JoyStick

Two analogue sticks and buttons in a battery-powered base, shipped with an M5AtomS3 in it.
[Product page](https://shop.m5stack.com/products/atom-joystick-with-m5atoms3)

## M5Stack Core2

ESP32 in the stackable Core case: 320x240 touch screen, IMU, speaker, battery base.
Discontinued by M5Stack, and the CoreS3 above is its successor in the same case, so check
what you can still get before buying a project that names it.
[Product page](https://shop.m5stack.com/products/m5stack-core2-esp32-iot-development-kit-v1-1)

## M5Stack Tab5

ESP32-P4 with an ESP32-C6 radio co-processor for Wi-Fi 6, a 5-inch 1280x720 MIPI-DSI
touch screen, a 2MP MIPI-CSI camera, ES8388 audio codec with dual microphones and a
speaker, and a removable NP-F550 battery.
[Product page](https://shop.m5stack.com/products/m5stack-tab5-iot-development-kit-esp32-p4)

## Ulanzi Smart Pixel Clock TC001

A shipped consumer clock built on an ESP32 driving a 32x8 addressable LED matrix, with
light and temperature sensors, buttons and a battery.
[Product page](https://www.ulanzi.com/products/ulanzi-pixel-smart-clock-2882)

## TRMNL

A shipped ESP32-C3 e-ink dashboard, sold assembled, with a plugin ecosystem behind it.
[Product page](https://trmnl.com)

## Narya board

Open hardware built for Family mruby Retro: an ESP32-S3 paired with an ESP32-WROVER that
drives NTSC composite video and I2S audio, so the board plugs into a TV, with a USB host
port for a keyboard and mouse, an SD card slot and an RTC. Sold assembled in small
batches, and the KiCAD sources are published.
[Product page](https://booth.pm/ja/items/8128031) ·
[design files](https://github.com/family-mruby/narya-board)

## No single device

These projects name no device, and inventing one would misrepresent them. What each takes
instead:

- **InkSight**: an ESP32-C3 development board and a 4.2-inch e-paper panel, wired by you.
  The project publishes its own purchasing guide and a browser flasher.
- **OpenEPaperLink**: second-hand electronic shelf labels, many models of them, plus an
  ESP32 acting as the access point that drives the tags over radio.
- **squeezelite-esp32**: a bare ESP32, usually with an I2S DAC board when you want sound
  out of the device rather than streamed on to another endpoint.
- **esp32_basic_synth**: a bare ESP32 and a DAC, nothing else.
- **The Lantern Project**: two boards you wire yourself, an ESP32 as the remote and an ESP8266 as the receiver, plus an addressable RGB strip. Circuit diagrams for both sides are in the repo.
- **HomePoint**: any ESP32 carrying a screen; it ships prebuilt binaries for a generic
  module and for an M5Stack.
- **esp32-lvgl-watchface**: any board with a 240x240 display that LVGL can drive.
- **Midbar**: versions exist for a dozen microcontrollers including the ESP32, each with
  its own parts list and its own build.
- **tempmeter**: an ESP32-C3 SuperMini, a BME280 breakout and a TM1637 4-digit
  display, wired by you, in a 3D-printed case. The README gives the pin map and the
  transmit-power setting the SuperMini needs to keep its access point up.
- **Tasmota, WLED, Meshtastic, ESPHome, xiaozhi-esp32**: firmware ecosystems running on
  hundreds to thousands of boards. Each publishes the compatibility list; no short answer
  here would be true.
- **ESP32-Calculator**: an ESP32 development board, an SSD1306 128x64 OLED display, and a 7x5 matrix keypad, wired by you.
