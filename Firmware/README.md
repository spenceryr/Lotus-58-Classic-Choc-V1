## What firmware do I want to use? QMK or Vial? And what is nanoBoot?
### Vial - user friendly, easier for a beginner.
[VIAL](https://get.vial.today) allows you to dynamically remap and change settings on the keyboard from a GUI both [app](https://get.vial.today) and [online](https://vial.rocks), without re-flashing it. It however requires that the keyboard is first flashed with a dedicated firmware for Vial. 

Unfortunately, since the GUI functions add some size and complexity to the firmware, and with recent memory bloat from upstream QMK, requiring more and more memory for essentially the same functions, **it is no longer a viable option to supply a full featured binary for using Vial on a Atmega32u4 based Pro Micro.** 

You can still use Vial on a Pro Micro based on the Atmega32u4, but with the limited memory, you will have to remove features and select/enable the features you deem important. **As such, no Atmega32u4 based binary will be supplied!**

**Vial source:** [https://github.com/TweetyDaBird/vial-qmk](https://github.com/TweetyDaBird/vial-qmk)

### QMK - The most powerful and flexible option, but requires a bit more knowledge.
In most cases you can use [QMK Configurator](https://config.qmk.fm/#/tweetydabird/lotus58/promicro/LAYOUT) to build your firmware, as Lotus is included in the main QMK git branch. However if you are using a RP2040 based controller, you need to build from source and use the appropriorate [converter](https://docs.qmk.fm/#/feature_converters?id=converters) for your exact controller (since there are multiple different options, supplying pre-compiled binaries is not a good option).  

**QMK source:** [https://github.com/qmk/qmk_firmware/tree/master/keyboards/tweetydabird/lotus58](https://github.com/qmk/qmk_firmware/tree/master/keyboards/tweetydabird/lotus58)

### What is nanoBoot and why should I use it?
nanoBoot is a tiny (512kB) HID type bootloader derived from the LUFA project, and it gives a whole lot more usable memory compared to the more full featured (legacy) bootloaders at five times the size or more. This is important overall using the Atmega32u4 as it is limited on memory. It's very useful both for vanilla QMK and if you compile a custom Vial firmware. **At this point, trying to use an Atmega32u4 without nanoBoot is not recommended.** 

* If you are using QMK, once the bootloader has been flashed, you can use QMK configurator as normal by simply selecting the nanoBoot option in the GUI.
* If you use Vial and nanoBoot/Atmega32u4, you need to compile from source.

You can find more information about how to flash nanoBoot in the `bootloader` folder.

## Available precompiled firmware files.
Coming soon!
