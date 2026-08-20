# awesome-esp32

Hand-picked ESP32 projects worth building, copying, or just watching run. Every entry links to a working repository; demo links are kept when the demo is the point.

Two top-level sections: **Applications** are actual things people have built and run on an ESP32; **Tools, utilities & libraries** is what you build them with. Subcategories are provisional and will be reshaped as the list grows. See [CONTRIBUTING.md](CONTRIBUTING.md) to add a project, or [ideas/ideas.md](ideas/ideas.md) for things waiting to be built. Two field guides distill how the listed projects are built: [ESP32 development practices](guides/esp32-practices.md) (any board) and the [Waveshare AMOLED 1.8 guide](guides/waveshare-amoled-18.md).

## Applications

### Companions & AI devices

- [chat-stick](https://github.com/steveruizok/chat-stick) - Hold-to-talk voice interface to Gemini Live on an ESP32-S3 stick, with persistent timers, server-side tools, and OTA updates. ([demo](https://x.com/steveruizok/status/2081132808341176405))
- [xiaozhi-esp32](https://github.com/78/xiaozhi-esp32) - MCP-based AI chatbot firmware powering a whole ecosystem of talking desk companions. `ecosystem`
- [pixelcat](https://github.com/toddsherman/pixelcat) - Tamagotchi-style pixel cat on an ESP32-S3 AMOLED handheld that learns your schedule, reacts to touch and sound, and can never irrecoverably die. ([demo](https://x.com/tdd/status/2088804262646288883))
- [pocket-pet](https://github.com/frolic/pocket-pet) - Pocket-Pikachu-style virtual-pet watch on an ESP32-S3 AMOLED dev kit: a pixel pet roams a grass field, counts your real steps, sleeps with the screen, and levels up as you walk.

### Displays & ambient screens

- [awtrix3](https://github.com/Blueforcer/awtrix3) - Turns an Ulanzi pixel clock into a scriptable smart display with a large community of apps. `ecosystem`
- [HomePoint](https://github.com/sieren/HomePoint) - A small ESP32 screen for switching MQTT and HomeKit devices.
- [esp32-lvgl-watchface](https://github.com/fbiego/esp32-lvgl-watchface) - Renders smartwatch binary watchfaces on a 240x240 LVGL screen, with a converter that turns watchface files into compilable code. ([demo](https://www.youtube.com/watch?v=lvRsTp9v6_k))

### E-paper

- [trmnl firmware](https://github.com/usetrmnl/firmware) - Firmware behind the TRMNL e-ink dashboard, an ESP32-C3 driving a battery-friendly plugin ecosystem. `ecosystem`
- [OpenEPaperLink](https://github.com/OpenEPaperLink/OpenEPaperLink) - Repurposes electronic shelf labels into a wireless e-paper display network with an ESP32 access point. `ecosystem`
- [InkSight](https://github.com/datascale-ai/inksight) - E-paper desk companion on an ESP32-C3: 24 display modes (weather, poetry, habit tracking), a community mode marketplace, and browser-based flashing. `ecosystem`

### Home & ambient

- [Tasmota](https://github.com/arendst/Tasmota) - Flash-and-forget firmware giving off-the-shelf smart plugs and lights local MQTT control. `ecosystem`
- [WLED](https://github.com/Aircoookie/WLED) - The addressable-LED firmware, with effects, segments, and an ecosystem of controllers built around it. `ecosystem`

### Creative & play

Most of this section (plus pixelcat above) targets one board: the [Waveshare ESP32-S3 Touch AMOLED 1.8](https://www.waveshare.com/esp32-s3-touch-amoled-1.8.htm), a pocket-size touchscreen with IMU, speaker and battery support. One purchase runs nearly everything below. Building for it yourself? Start with [the field guide](guides/waveshare-amoled-18.md) distilled from how these projects are built.

- [tinydraw](https://github.com/aliceisjustplaying/tinydraw) - Finger-drawing app for ESP32-S3/RP2350 touch AMOLED handhelds, with variable-width ink, zoom, undo, and SVG/PNG export. ([demo](https://x.com/aliceisplaying/status/2087153749240217805))
- [infinite-golf](https://github.com/MikeWilson/infinite-golf) - Procedurally generated mini-golf on an ESP32-S3 AMOLED handheld; you physically swing the device and the IMU measures the shot. ([demo](https://x.com/mk_wlsn/status/2087389762042958242))
- [esp32-gameos](https://github.com/MikeWilson/esp32-gameos) - A handheld gaming OS for the same AMOLED device: launcher plus six fully procedural games at 60 fps, no engine, no asset files. ([demo](https://x.com/mk_wlsn/status/2089740913195274284))
- [esp32-fluidbox](https://github.com/V4C38/esp32-fluidbox) - A 3D particle fluid living inside the device's case: ~900 particles slosh with the accelerometer as if liquid sat behind the screen. ([demo](https://x.com/JohannesTscharn/status/2085248949061922855))
- [puck apps](https://github.com/s0lness/puck/tree/master/apps) - Clock, connect 4, and friends: small apps written once against the puck convention, each running on both of its boards. ([live gallery](https://puck.sylve.org))

### Audio & music

- [squeezelite-esp32](https://github.com/sle118/squeezelite-esp32) - Multi-room audio player and AirPlay/Spotify/Bluetooth endpoint on a bare ESP32.
- [esp32_basic_synth](https://github.com/marcel-licence/esp32_basic_synth) - A polyphonic MIDI synthesizer from one chip and a DAC.

### Radio & mesh

- [Meshtastic](https://github.com/meshtastic/firmware) - Off-grid, encrypted LoRa mesh messaging; the reference ESP32 radio project. `ecosystem`

### Remote access

- [ESP-KVM](https://github.com/espkvm/espkvm) - IP-KVM on an ESP32-P4 and a TC358743 HDMI bridge: captures the target machine's screen, presents itself to that machine as a USB keyboard and mouse, and puts both in a browser, down to the BIOS of a box with no working OS. ([demo](https://espkvm.io/demo/))

### Drones & robotics

- [ESP-Drone](https://github.com/Circuit-Digest/ESP-Drone) - Phone-controlled DIY ESP32 drone with MPU6050 stabilization, height hold, and Wi-Fi control.

## Tools, utilities & libraries

### Frameworks & languages

- [ESP-IDF](https://github.com/espressif/esp-idf) - Espressif's official development framework.
- [esp-hal](https://github.com/esp-rs/esp-hal) - Bare-metal Rust for ESP32 chips.
- [MicroPython](https://github.com/micropython/micropython) - Python on the chip, with first-class ESP32 support.
- [ESPHome](https://github.com/esphome/esphome) - Describe a device in YAML, get firmware; the default way ESP32s enter Home Assistant. `ecosystem`

### Utilities & SDKs

- [ESP Web Tools](https://github.com/esphome/esp-web-tools) - Flash firmware from the browser over WebSerial, no toolchain installed.
- [openHASP](https://github.com/HASwitchPlate/openHASP) - Build custom touchscreen control panels for home automation, driven over MQTT.
- [psiop](https://github.com/aap/psiop) - A compact software 3D rendering library for the ESP32. ([demo](https://x.com/Alacritic_Super/status/2089987821352403387))
- [openai-realtime-embedded](https://github.com/openai/openai-realtime-embedded) - OpenAI's official SDK for talking to the Realtime API over WebRTC from an ESP32-S3.

### Emulators & simulators

- [Wokwi](https://github.com/wokwi) - Simulate ESP32 boards, sensors and displays in the browser; the fastest way to try firmware with no hardware on the desk. ([simulator](https://wokwi.com))
- [espressif/qemu](https://github.com/espressif/qemu) - Espressif's QEMU fork: full-system ESP32 emulation for CI and debugging.
- [puck](https://github.com/s0lness/puck) - Convention and emulator for apps that travel between tiny computers (RP2350 and ESP32-S3), with harness-verified pixel-exact ports.

## License

[CC0 1.0](LICENSE). Descriptions belong to their projects' authors where quoted.
