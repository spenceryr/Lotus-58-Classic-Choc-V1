### lotus58_vial_caterina.hex
VIAL firmware for a standard Pro Micro with a Caterina Bootloader

### lotus58_vial_nanoBoot.hex
VIAL firmware for a Pro Micro with a nanoBoot bootloaer.

This needs to be flashed using an ISP programmer, as it contains BOTH the bootloader and firmware in one Single .HEX file.

Best flashed with avrdude.

#### Fuse Settings:

- lfuse memory = 0xFF or 0x7F (CKDIV8=1 or 0, 16CK+65ms)
- hfuse memory = 0xD6 (EESAVE=0, BOOTRST=0)
- efuse memory = 0xC7 (=0xF7, No BOD)

##### -U lfuse:w:0x7F:m -U hfuse:w:0xD6:m -U efuse:w:0xC7:m

