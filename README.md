# awesome-esp32

Hand-picked ESP32 projects worth building, copying, or just watching run. Every entry links to a working repository; demo links are kept when the demo is the point.

Scope: the ESP32 family first, and close cousins (RP2350 and friends) when a project ports across chips instead of living on one.

Two top-level sections: **Applications** are actual things people have built and run on an ESP32; **Tools, utilities & libraries** is what you build them with. Inside Applications, the tree answers one question only, what a project is for; the tags answer the other one, what it runs on. Available tags: `e-ink`, `s3-amoled`, `led-matrix`, `p4`, `c3`, `headless`, `battery`, `ecosystem`. They ride at the end of an entry line, and they mark the exception: an entry with no tag is an ordinary ESP32 with an ordinary screen.

`s3-amoled` mostly means one board, the [Waveshare ESP32-S3 Touch AMOLED 1.8](https://www.waveshare.com/esp32-s3-touch-amoled-1.8.htm), a pocket-size touchscreen with IMU, speaker and battery support. One purchase runs most of the Play section; building for it yourself starts with its field guide in [Guides](#guides).

What gets in, in short: public source you can build, evidence it ran on real hardware (a photo, a video, or a live demo, not a render), and enough in the README that someone else can reproduce it. Stars are not a criterion. The full version, and how to submit, are in [CONTRIBUTING.md](CONTRIBUTING.md). Things waiting to be built are in [ideas/ideas.md](ideas/ideas.md).

## Guides

In this repo, distilled from how the listed projects are built:

- [ESP32 development practices](guides/esp32-practices.md) - Board-agnostic lessons pulled from every listed project, each cited to the one that learned it: choosing a stack, holding a board matrix, memory discipline, watchdogs, OTA, connectivity, power.
- [Waveshare AMOLED 1.8 guide](guides/waveshare-amoled-18.md) - Field notes for the `s3-amoled` board, measured on real hardware: pin map, CO5300 panel, touch, IMU, audio codec, power and battery, and a condensed do-not list.

Elsewhere, write-ups by @ardchain posted as threads on X (third-party, not repo documents, and X may show a login wall if you have no account):

- [Learn ESP32 from zero in one evening](https://x.com/ardchain/status/2087213058800099724) - Beginner path from nothing: install the toolchain, blink an external LED, add a button, then serve a Wi-Fi web page.
- [Give your ESP32 eyes: camera, local vision, and reactions](https://x.com/ardchain/status/2089396488656818438) - Camera boards, running vision on the device, and turning a detection into an action with debouncing and confidence thresholds.
- [Your $8 Gateway to Local AI: The ESP32 Masterclass](https://x.com/ardchain/status/2081775980650139929) - Splitting small local models across several ESP32-S3 nodes, with I2S microphone capture and execution over BLE.

## Applications

### Companions

- [chat-stick](https://github.com/steveruizok/chat-stick) - Hold-to-talk voice interface to Gemini Live on an ESP32-S3 stick, with persistent timers, server-side tools, and OTA updates. ([demo](https://x.com/steveruizok/status/2081132808341176405)) `s3-amoled`
- [xiaozhi-esp32](https://github.com/78/xiaozhi-esp32) - MCP-based AI chatbot firmware powering a whole ecosystem of talking desk companions. `ecosystem`
- [pixelcat](https://github.com/toddsherman/pixelcat) - Tamagotchi-style pixel cat on an ESP32-S3 AMOLED handheld that learns your schedule, reacts to touch and sound, and can never irrecoverably die. ([demo](https://x.com/tdd/status/2088804262646288883)) `s3-amoled` `battery`
- [pocket-pet](https://github.com/frolic/pocket-pet) - Pocket-Pikachu-style virtual-pet watch on an ESP32-S3 AMOLED dev kit: a pixel pet roams a grass field, counts your real steps, sleeps with the screen, and levels up as you walk. `s3-amoled` `battery`
- [InkSight](https://github.com/datascale-ai/inksight) - E-paper desk companion on an ESP32-C3: 24 display modes (weather, poetry, habit tracking), a community mode marketplace, and browser-based flashing. `e-ink` `c3` `ecosystem`

### Displays & ambient

- [awtrix3](https://github.com/Blueforcer/awtrix3) - Turns an Ulanzi pixel clock into a scriptable smart display with a large community of apps. `led-matrix` `ecosystem`
- [HomePoint](https://github.com/sieren/HomePoint) - A small ESP32 screen for switching MQTT and HomeKit devices.
- [esp32-lvgl-watchface](https://github.com/fbiego/esp32-lvgl-watchface) - Renders smartwatch binary watchfaces on a 240x240 LVGL screen, with a converter that turns watchface files into compilable code. ([demo](https://www.youtube.com/watch?v=lvRsTp9v6_k))
- [OpenEPaperLink](https://github.com/OpenEPaperLink/OpenEPaperLink) - Repurposes electronic shelf labels into a wireless e-paper display network with an ESP32 access point. `e-ink` `ecosystem`
- [trmnl firmware](https://github.com/usetrmnl/firmware) - Firmware behind the TRMNL e-ink dashboard, an ESP32-C3 driving a battery-friendly plugin ecosystem. `e-ink` `c3` `battery` `ecosystem`

### Play

- [tinydraw](https://github.com/aliceisjustplaying/tinydraw) - Finger-drawing app for ESP32-S3/RP2350 touch AMOLED handhelds, with variable-width ink, zoom, undo, and SVG/PNG export. ([demo](https://x.com/aliceisplaying/status/2087153749240217805)) `s3-amoled`
- [infinite-golf](https://github.com/MikeWilson/infinite-golf) - Procedurally generated mini-golf on an ESP32-S3 AMOLED handheld; you physically swing the device and the IMU measures the shot. ([demo](https://x.com/mk_wlsn/status/2087389762042958242)) `s3-amoled`
- [esp32-gameos](https://github.com/MikeWilson/esp32-gameos) - A handheld gaming OS for the same AMOLED device: launcher plus six fully procedural games at 60 fps, no engine, no asset files. ([demo](https://x.com/mk_wlsn/status/2089740913195274284)) `s3-amoled`
- [esp32-fluidbox](https://github.com/V4C38/esp32-fluidbox) - A 3D particle fluid living inside the device's case: ~900 particles slosh with the accelerometer as if liquid sat behind the screen. ([demo](https://x.com/JohannesTscharn/status/2085248949061922855)) `s3-amoled`
- [puck apps](https://github.com/s0lness/puck/tree/master/apps) - Clock, connect 4, and friends: small apps written once against the puck convention, each running on both of its boards. ([live gallery](https://puck.sylve.org)) `s3-amoled`
- [67](https://github.com/canwar-dj/67) - Throw-and-catch party game for an ESP32-S3 AMOLED handheld; the screen flickers random numbers while airborne and locks in on catch, landing on a red 67 one time in five to pick a loser. ([demo](https://x.com/kanwardigvijay/status/2090090888659898500)) `s3-amoled`

### Home & control

- [Tasmota](https://github.com/arendst/Tasmota) - Flash-and-forget firmware giving off-the-shelf smart plugs and lights local MQTT control. `ecosystem`
- [WLED](https://github.com/Aircoookie/WLED) - The addressable-LED firmware, with effects, segments, and an ecosystem of controllers built around it. `ecosystem`

### Radio & comms

- [Meshtastic](https://github.com/meshtastic/firmware) - Off-grid, encrypted LoRa mesh messaging; the reference ESP32 radio project. `ecosystem`
- [Waycast](https://github.com/alviso/waycast) - Car-to-car LoRa mesh on an ESP32-P4 touchscreen dashboard: geo-ephemeral hazard reports, convoy position sharing, and offline maps, with no cellular dependency. ([site](https://waycast.io)) `p4`

### Audio & music

- [squeezelite-esp32](https://github.com/sle118/squeezelite-esp32) - Multi-room audio player and AirPlay/Spotify/Bluetooth endpoint on a bare ESP32. `headless`
- [esp32_basic_synth](https://github.com/marcel-licence/esp32_basic_synth) - A polyphonic MIDI synthesizer from one chip and a DAC. `headless`

### Utilities & appliances

- [ESP-KVM](https://github.com/espkvm/espkvm) - IP-KVM on an ESP32-P4 and a TC358743 HDMI bridge: captures the target machine's screen, presents itself to that machine as a USB keyboard and mouse, and puts both in a browser, down to the BIOS of a box with no working OS. ([demo](https://espkvm.io/demo/)) `p4` `headless`

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
