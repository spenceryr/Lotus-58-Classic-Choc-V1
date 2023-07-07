## Available precompiled firmware files.
All preconfigured firmewares are based on [VIAL](https://get.vial.today), and with the most common options enabled, more or less the way I use the keyboard myself (Some minor tweaks, as I'm Swedish, so I'm using a few characters that isn't used in English). Feel free to edit or re-invent the firmware as you please, its available as source [here](https://github.com/TweetyDaBird/vial-qmk).

**Notice!** *Compiling from source in Vial-QMK is slightly more advanced than QMK, and likely unnecessary as Vial's intended use is through the app. For this reason, for most normal users it is recommended to flash a precompiled firmware.*

### Atmel-DFU
VIAL firmware for Elite C or equivalent with an Atmel-DFU Bootloader

### Caterina
VIAL firmware for Pro Micro with an Caterina Bootloader (This is the default boot-loader for a Pro Micro!)

### nanoBoot
VIAL firmware for Pro Micro with an nanoBoot bootloader already flashed. (Note that this should NOT be flashed onto a Pro Micro with a Caterina bootloader!)

## Why nanoBoot?
nanoBoot is a tiny (512k) HID type bootloader derived from the LUFA project, and it gives a whole lot more usable memory compared to the more full featured bootloaders at five times the size or more. This is important overall using the Atmega32u4 as it is limited on memory to start with, but even more so when using [VIAL](https://get.vial.today), as that takes a bit more memory than QMK for the dynamic, realtime remapping available [here](https://vial.rocks).

## I want to use QMK instead.
Well... Go [here](https://github.com/TweetyDaBird/qmk_firmware) then, and have fun!
