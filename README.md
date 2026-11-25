# Easy Bitx Mono Band

**Configurable Single-Band VFO/BFO Firmware for Easy Bitx HF Transceivers**

Arduino Nano-based VFO/BFO firmware using the Si5351 clock generator and a 10 MHz IF architecture.

Originally developed for EasyBitx kits by Sunil Lakhani (VU3SUA), the firmware supports configurable 80m, 40m and 20m operation, with one band selected at a time through compile-time frequency settings.

## Features

- Configurable 80m, 40m and 20m operation.
- Si5351-based VFO and BFO generation.
- Automatic USB/LSB selection.
- Rotary encoder frequency tuning.
- Five selectable tuning steps (1 Hz to 10 kHz).
- Adjustable BFO frequency.
- EEPROM storage for BFO calibration.
- 16×2 LCD frequency display.
- LCD heartbeat indicator.

## Hardware

- Arduino Nano (ATmega328P)
- Si5351 clock generator
- 16×2 parallel LCD
- Rotary encoder with push button
- VU3SUA VFO/BFO board

## Band Configuration

The operating band is selected by changing the frequency limits in the source code and uploading the firmware again.

```cpp
#define fMax 14500000UL
#define fMin 14000000UL
```

The above configuration selects the 20m frequency range. Corresponding frequency limits can be configured for 40m and 80m.

## Installation

1. Install Arduino IDE.
2. Install the required libraries: Si5351Arduino, Rotary, EEPROMex and EasyButton.
3. Open `EasyBitx_vu3gao_v1.5.ino`.
4. Select Arduino Nano (ATmega328P).
5. Compile and upload.

## Development Credits

- **J. CesarSound** – Original VFO/BFO code (2020).
- **Nitin William (VU3GAO)** – EasyBitx Mono Band firmware, Version 1.5 (2021).
- **Sunil Lakhani (VU3SUA)** – EasyBitx kit developer and distributor for which this firmware was created.

This firmware is released under the **GNU General Public License v3.0 (GPL-3.0)**.

## 73!

**73 de VU3HZW**

*Keeping the spirit of DIY amateur radio alive.*
