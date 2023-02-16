## Available precompiled firmware files.
All preconfigured firmewares are based on [VIAL](https://get.vial.today), and with the most common options enabled, more or less the way I use the keyboard myself (Some minor tweaks, as I'm Swedish, so I'm using a few characters that isn't used in English). Feel free to edit or re-invent the firmware as you please, its available as source [here](https://github.com/TweetyDaBird/vial-qmk).
#### Notice!
Compiling from source in Vial-QMK is slightly more advanced than QMK, and likely unnecessary as Vial's intended use is through the app. For this reason most normal users, it is recommended to flash a precompiled firmware. 

### lotus58_vial_caterina.hex
VIAL firmware for a standard Pro Micro with a Caterina Bootloader

### lotus58_vial_nanoBoot.hex
VIAL firmware for a Pro Micro with a nanoBoot bootloader already flashed. (Note that this is too big to flash onto a Pro Micro with a Caterina bootloader)

### PRODUCTION_lotus58_vial_nanoBoot.hex
This needs to be flashed using an ISP programmer, as it contains BOTH the nanoBoot boot-loader and firmware in one Single .HEX file.

## Why nanoBoot?
nanoBoot is a tiny (512k) HID type bootloader derived from the LUFA project, and it gives a whole lot more usable memory compared to the more full featured bootloaders at five times the size or more. This is important overall using the Atmega32u4 as it is limited on memory to start with, but even more so when using [VIAL](https://get.vial.today), as that takes a bit more memory than QMK for the dynamic, realtime remapping available [here](https://vial.rocks).

## I want to use QMK instead.
Well... Go [here](https://github.com/TweetyDaBird/qmk_firmware) then, and have fun!

#### Notice!
Since Lotus 58 Glow currently isnt merged into QMK's main branch, flashing/compiling from source is slightly more advanced, and requires some basic knowledge yourself. The published source is as-is, with no expressed warranty, and no promised timeline on maintaining updates with QMK's updates. If you find errors, feel free to update and fix them, and i will happily test and merge them for all to use. 

## Flashing the production firmware

This is best flashed with avrdude or similar and requires either a dedicated hardware ICSP or a second Arduino acting as one.  

#### Fuse Settings:

- lfuse memory = 0xFF or 0x7F (CKDIV8=1 or 0, 16CK+65ms)
- hfuse memory = 0xD6 (EESAVE=0, BOOTRST=0)
- efuse memory = 0xC7 (=0xF7, No BOD)

#### Example of fuse command

-U lfuse:w:0x7F:m -U hfuse:w:0xD6:m -U efuse:w:0xC7:m

