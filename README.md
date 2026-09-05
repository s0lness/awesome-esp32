# awesome-esp32

Tiny computers are having a moment online, I figured making a list of cool projects people have built using the ESP32 chip would encourage folks to continue tinkering.

The ESP32 is a microcontroller and many packaged devices use it, such as Waveshare and LilyGO boards, M5Stack units, and shipped products like the Ulanzi pixel clock. The projects will state on which of these devices it runs to facilitate discoverability.

The document is organized like this:
- **Applications** are things people built and run;
- **Tools, utilities & libraries** is what you build them with.
- each entry ends with the device it runs on, in backticks, spelled as [devices.md](devices.md) spells it. Search that name and you get every project for the hardware you own.
- a handful of projects have no single device: they run on dozens of boards, or on a bare ESP32 plus parts you pick yourself. Those end with nothing, and [devices.md](devices.md) says what each one takes.

If you're getting started and wonder which device to get, the list of devices used in the repo is laid out in [devices.md](devices.md). 

This is a collaborative project, if you've built something cool see [CONTRIBUTING.md](CONTRIBUTING.md) and make a PR. I've also listed some ideas in [ideas/ideas.md](ideas/ideas.md).

## Guides

- [ESP32 development practices](guides/esp32-practices.md) - Board-agnostic lessons pulled from every listed project, each cited to the one that learned it: choosing a stack, holding a board matrix, memory discipline, watchdogs, OTA, connectivity, power.
- [Waveshare AMOLED 1.8 guide](guides/waveshare-amoled-18.md) - Field notes for the Waveshare ESP32-S3-Touch-AMOLED-1.8, measured on real hardware: pin map, CO5300 panel, touch, IMU, audio codec, power and battery, and a condensed do-not list.

Elsewhere, write-ups by @ardchain posted as threads on X (third-party, not repo documents, and X may show a login wall if you have no account):

- [Learn ESP32 from zero in one evening](https://x.com/ardchain/status/2087213058800099724) - Beginner path from nothing: install the toolchain, blink an external LED, add a button, then serve a Wi-Fi web page.
- [Give your ESP32 eyes: camera, local vision, and reactions](https://x.com/ardchain/status/2089396488656818438) - Camera boards, running vision on the device, and turning a detection into an action with debouncing and confidence thresholds.
- [Your $8 Gateway to Local AI: The ESP32 Masterclass](https://x.com/ardchain/status/2081775980650139929) - Splitting small local models across several ESP32-S3 nodes, with I2S microphone capture and execution over BLE.

## Applications

### Companions

- [chat-stick](https://github.com/steveruizok/chat-stick) - Hold-to-talk voice interface to Gemini Live, with persistent timers, server-side tools and OTA updates, running on either an M5StickS3 or a Waveshare ESP32-S3-Touch-AMOLED-1.8. ([demo](https://x.com/steveruizok/status/2081132808341176405)) `M5StickS3` or `Waveshare ESP32-S3-Touch-AMOLED-1.8`
- [xiaozhi-esp32](https://github.com/78/xiaozhi-esp32) - MCP-based AI chatbot firmware powering a whole ecosystem of talking desk companions, across dozens of boards it lists itself.
- [pixelcat](https://github.com/toddsherman/pixelcat) - Tamagotchi-style pixel cat on a Waveshare ESP32-S3-Touch-AMOLED-1.8 that learns your schedule, reacts to touch and sound, and can never irrecoverably die. ([demo](https://x.com/tdd/status/2088804262646288883)) `Waveshare ESP32-S3-Touch-AMOLED-1.8`
- [pocket-pet](https://github.com/frolic/pocket-pet) - Pocket-Pikachu-style virtual-pet watch on a Waveshare ESP32-S3-Touch-AMOLED-2.06: a pixel pet roams a grass field, counts your real steps, sleeps with the screen, and levels up as you walk. `Waveshare ESP32-S3-Touch-AMOLED-2.06`
- [InkSight](https://github.com/datascale-ai/inksight) - E-paper desk companion built from an ESP32-C3 board and a 4.2-inch panel: 24 display modes (weather, poetry, habit tracking), a community mode marketplace, and browser-based flashing.
- [ESP32 Codex Agent Device](https://github.com/mso96/ESP32-Codex-agent-device) - Physical Codex task-status companion for a Waveshare ESP32-S3-Touch-AMOLED-1.8, with lifecycle tracking, runtime and token metrics, and a procedural avatar. ([demo](https://github.com/mso96/ESP32-Codex-agent-device/blob/main/docs/hardware-demo.jpg)) `Waveshare ESP32-S3-Touch-AMOLED-1.8`
- [Vibe Watch](https://github.com/GOROman/vibewatch) - Wrist-worn M5Stack StopWatch controller for parallel AI coding agents, with physical approve/reject, haptics, and BLE HID. ([demo](https://x.com/GOROman/status/2094369107781283991)) `M5Stack StopWatch`
- [esp32-ai TinyPoems](https://github.com/jeonghopark/esp32-ai) - Runs a tiny poem language model locally on an M5Stack StickS3 and displays generated poems on its LCD. `M5StickS3`

### Displays & ambient

- [awtrix3](https://github.com/Blueforcer/awtrix3) - Turns an Ulanzi Smart Pixel Clock TC001 into a scriptable smart display with a large community of apps. `Ulanzi Smart Pixel Clock TC001`
- [HomePoint](https://github.com/sieren/HomePoint) - Switches MQTT and HomeKit devices from a small screen, shipped as prebuilt binaries for a generic ESP32 module or an M5Stack.
- [esp32-lvgl-watchface](https://github.com/fbiego/esp32-lvgl-watchface) - Renders smartwatch binary watchfaces on any board carrying a 240x240 LVGL screen, with a converter that turns watchface files into compilable code. ([demo](https://www.youtube.com/watch?v=lvRsTp9v6_k))
- [OpenEPaperLink](https://github.com/OpenEPaperLink/OpenEPaperLink) - Repurposes electronic shelf labels into a wireless e-paper display network with an ESP32 access point.
- [trmnl firmware](https://github.com/usetrmnl/firmware) - Firmware behind the TRMNL e-ink dashboard, an ESP32-C3 driving a battery-friendly plugin ecosystem. `TRMNL`
- [esp32-vertical-card-compass](https://github.com/austinbirch/esp32-vertical-card-compass) - Simulates an aviation vertical-card magnetic compass on an M5Stack CoreS3: the card swings, overshoots, and reproduces the real instrument's errors. ([demo](https://x.com/austinbirch/status/2086535581773828169)) `M5Stack CoreS3`
- [stripe-business-metrics-monitor](https://github.com/cosjef/stripe-business-metrics-monitor) - Desk display for a Stripe subscription business, rotating eight screens of MRR and its 30-day trend, signup pace, ARPU compared across joining and leaving cohorts, and failed payments with the revenue at risk. `Waveshare ESP32-C6-Touch-AMOLED-2.16`

### Play

- [tinydraw](https://github.com/aliceisjustplaying/tinydraw) - Finger-drawing app for the Waveshare ESP32-S3-Touch-AMOLED-1.8 and RP2350-Touch-AMOLED-1.8, with variable-width ink, zoom, undo, and SVG/PNG export. ([demo](https://x.com/aliceisplaying/status/2087153749240217805)) `Waveshare ESP32-S3-Touch-AMOLED-1.8` or `Waveshare RP2350-Touch-AMOLED-1.8`
- [infinite-golf](https://github.com/MikeWilson/infinite-golf) - Procedurally generated mini-golf on a Waveshare ESP32-S3-Touch-AMOLED-1.8; you physically swing the device and the IMU measures the shot. ([demo](https://x.com/mk_wlsn/status/2087389762042958242)) `Waveshare ESP32-S3-Touch-AMOLED-1.8`
- [esp32-gameos](https://github.com/MikeWilson/esp32-gameos) - A handheld gaming OS for the Waveshare ESP32-S3-Touch-AMOLED-1.8: launcher plus six fully procedural games at 60 fps, no engine, no asset files. ([demo](https://x.com/mk_wlsn/status/2089740913195274284)) `Waveshare ESP32-S3-Touch-AMOLED-1.8`
- [esp32-fluidbox](https://github.com/V4C38/esp32-fluidbox) - A 3D particle fluid living inside the case of a Waveshare ESP32-S3-Touch-AMOLED-1.8: ~900 particles slosh with the accelerometer as if liquid sat behind the screen. ([demo](https://x.com/JohannesTscharn/status/2085248949061922855)) `Waveshare ESP32-S3-Touch-AMOLED-1.8`
- [puck apps](https://github.com/s0lness/puck/tree/master/apps) - Clock, connect 4, and friends: small apps written once against the puck convention, each running on both the Waveshare ESP32-S3-Touch-AMOLED-1.8 and the RP2350-Touch-AMOLED-1.8. ([live gallery](https://puck.sylve.org)) `Waveshare ESP32-S3-Touch-AMOLED-1.8` and `Waveshare RP2350-Touch-AMOLED-1.8`
- [67](https://github.com/canwar-dj/67) - Throw-and-catch party game for a Waveshare ESP32-S3-Touch-AMOLED-2.06; the screen flickers random numbers while airborne and locks in on catch, landing on a red 67 one time in five to pick a loser. ([demo](https://x.com/kanwardigvijay/status/2090090888659898500)) `Waveshare ESP32-S3-Touch-AMOLED-2.06`

### Robots

- [MicroLink Crawler](https://github.com/GEH00073/MicroLink_Crawler) - Pocket FPV exploration rover on 7 mm 3D-printed linked tracks, needing all four of an M5Stamp Pico for the motors, an M5Stack AtomS3R-CAM for live video and red-object detection, an M5Stack Atom JoyStick to drive it, and an M5Stack Core2 as the monitor. ([demo](https://www.hackster.io/user2729037/microlink-crawler-379ff1)) `M5Stamp Pico` and `M5Stack AtomS3R-CAM` and `M5Stack Atom JoyStick` and `M5Stack Core2`

### Home & control

- [Tasmota](https://github.com/arendst/Tasmota) - Flash-and-forget firmware giving off-the-shelf smart plugs and lights local MQTT control, on a device list of its own that runs to thousands.
- [WLED](https://github.com/Aircoookie/WLED) - The addressable-LED firmware, with effects, segments, and an ecosystem of controllers built around it.
- [The Lantern Project](https://github.com/Northstrix/Lantern) - Addressable RGB LED strip controller you build as a pair: an ESP32 remote with 32 modes and 14 lock screens, talking to an ESP8266 that drives the strip. ([demo](https://www.instructables.com/DIY-Addressable-RGB-LED-Strip-Controller/))

### Radio & comms

- [Meshtastic](https://github.com/meshtastic/firmware) - Off-grid, encrypted LoRa mesh messaging on the LoRa boards it lists itself; the reference ESP32 radio project.
- [Waycast](https://github.com/alviso/waycast) - Car-to-car LoRa mesh on a Waveshare ESP32-P4-Module-DEV-KIT with a 7-inch touch panel, a USB LoRa dongle and a USB GPS: geo-ephemeral hazard reports, convoy position sharing, and offline maps, with no cellular dependency. ([site](https://waycast.io)) `Waveshare ESP32-P4-Module-DEV-KIT`
- [familybox](https://github.com/F86Pilot/familybox) - Photo and voice messages between a travelling parent and a child too young to read: the phone sends, a Waveshare ESP32-S3-Touch-AMOLED-1.8 shows the photo, and two buttons play the note or record a reply. ([demo](https://x.com/pmtiegs/status/2090134879875051709)) `Waveshare ESP32-S3-Touch-AMOLED-1.8`

### Audio & music

- [squeezelite-esp32](https://github.com/sle118/squeezelite-esp32) - Multi-room audio player and AirPlay/Spotify/Bluetooth endpoint on a bare ESP32.
- [esp32_basic_synth](https://github.com/marcel-licence/esp32_basic_synth) - A polyphonic MIDI synthesizer from one chip and a DAC.
- [esp32-spotify-remote](https://github.com/seichris/esp32-spotify-remote) - A touchscreen Spotify playback controller with previous, play/pause, and next controls, now-playing metadata, album artwork, and PKCE authorization. `Waveshare ESP32-S3-Touch-AMOLED-2.06`

### Utilities & appliances

- [ESP-KVM](https://github.com/espkvm/espkvm) - IP-KVM on a Waveshare ESP32-P4-ETH and a TC358743 HDMI bridge: captures the target machine's screen, presents itself to that machine as a USB keyboard and mouse, and puts both in a browser, down to the BIOS of a box with no working OS. ([demo](https://espkvm.io/demo/)) `Waveshare ESP32-P4-ETH`
- [Midbar](https://github.com/Northstrix/Midbar) - Hardware data vault for credentials and notes, built across a dozen MCUs including the ESP32: keys derive from the boot-time master password, joined by RFID cards on some versions.
- [HomeworkTimer](https://github.com/doublemarkpro/HomeworkTimer-ESP32-S3-Touch-LCD-3.49) - Homework timer for children with per-subject tracking, weekly reports, schedules, alarms, weather, Wi-Fi time sync and a low-power lock screen. ([demo](https://github.com/doublemarkpro/HomeworkTimer-ESP32-S3-Touch-LCD-3.49/blob/main/docs/hardware/home-screen.jpg)) `Waveshare ESP32-S3-Touch-LCD-3.49B`
- [open-bike-computer](https://github.com/seichris/open-bike-computer) - Garmin-mounted bike computer paired with its iPhone and Apple Watch app: Apple Maps navigation, live workout stats, Apple Health and Strava sync, power-meter and cadence sensors. `Waveshare ESP32-S3-Touch-AMOLED-1.75` or `Waveshare ESP32-S3-Touch-AMOLED-2.06`

## Tools, utilities & libraries

### Frameworks & languages

- [ESP-IDF](https://github.com/espressif/esp-idf) - Espressif's official development framework.
- [esp-hal](https://github.com/esp-rs/esp-hal) - Bare-metal Rust for ESP32 chips.
- [MicroPython](https://github.com/micropython/micropython) - Python on the chip, with first-class ESP32 support.
- [ESPHome](https://github.com/esphome/esphome) - Describe a device in YAML, get firmware; the default way ESP32s enter Home Assistant.

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
