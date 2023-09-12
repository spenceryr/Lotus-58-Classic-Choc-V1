# How do I burn nanoBoot to my (ATmega32u4-based) Pro Micros?

1. Install Arduino IDE 1.8.19 and Pro Micro support:
  - Go to Files -> Preferences;
  - Paste `https://raw.githubusercontent.com/sparkfun/Arduino_Boards/master/IDE_Board_Manager/package_sparkfun_index.json` into "Additional Boards Manager URLs", press OK;
  - Go to Tools -> Board -> Boards Manager;
  - Search for `SparkFun AVR Boards`, install that, close the dialog window.
2. Burn the ArduinoISP sketch (through the normal USB connection):
  - Connect one of your two Pro Micros (we will call it `A` from now on);
  - In Arduino IDE, go to Tools -> Board -> SparkFun AVR Boards -> SparkFun Pro Micro;
  - As Processor choose the 5V 16MHz version;
  - As Port choose whatever the Arduino IDE gives you as an option (If you have more than 1 serial device connected, figure out which port is your Pro Micro by plugging and unplugging it)
  - In Arduino IDE, go to File -> Examples -> ArduinoISP -> ArduinoISP;
  - Hit Upload (either the arrow to the right next to the checkmark, or in Sketch -> Upload);
  - Close the Arduino IDE.
3. Connect the two Pro Micros:
  - Disconnect the Pro Micro `A` from the computer, get 6 jumper wires;
  - Connect the GND pin to GND pin, VCC to VCC, 15 to 15, 14 to 14, 16 to 16;
  - PAY ATTENTION: Connect the pin 10 of the Pro Micro `A`, to RST of the Pro Micro `B`;
  - Plug the Pro Micro `A` back into the computer.
4. Burn the supplied `nanoBoot-bootloader.hex` to the Pro Micro `B` (using `A´ as the ISP):
  - Now we will use `avrdude` included in the Arduino as a standalone executable (These instructions assume you use a terminal for your OS);
  - In the terminal go to the location where you downloaded the supplied `nanoBoot_ArduinoISP.hex` (use the `cd` command to jump between directories, `ls` (MacOS/Linux) or `dir` (Windows) displays content)
  - Run this command: `avrdude -c stk500v1 -p atmega32u4 -P /dev/ttyACM0 -b 19200 -U flash:w:nanoBoot-ArduinoISP.hex:i -U lfuse:w:0x7F:m -U hfuse:w:0xD6:m -U efuse:w:0xC7:m`  **WARNING: This command sets fuses on the board and wrong values of the fuses can brick the board beyond repair. This is done at your own responsibility!!** *Note: you might need to change the serial port given after -P from what is shown here, it should be the same you used when uploading the sketch through Arduino IDE.*
  - This flashes the same ArduinoISP sketch, but with the nanoBoot bootloader already included.
5. Burn the nanoBoot bootloader to the Pro Micro `A`:
  - Disconnect the Pro Micro `A` from the computer;
  - Swap the connections between the Pro Micros, since you will now swap the roles of the Pro Micros - Connect Pro Micro `A`'s RST to Pro Micro `B`'s pin 10;
  - Connect the Pro Micro `B` to the computer;
  - Run the same command as in step 4 (**the same warning applies**);
  - Congratulations! Now you have two Pro Micros with nanoBoot bootloaders!
6. Flash the Lotus58 firmware:
  - Open QMK Toolbox (if you're on Windows or macOS);
  - Select the `lotus58_nanoboot_vial.hex` firmware;
  - Select auto-flash;
  - Plug in either of your Pro Micros;
  - Reset to bootloader by quickly bridging the GND and RST pins with something like a screwdriver;
  - Wait until the firmware is flashed;
  - Unplug the Pro Micro and plug in the other one;
  - Repeat;
  - Close QMK Toolbox, open [VIAL](https://get.vial.today/) (either as an app or in browser);
  - Plug in your Pro Micro, if the layout of Lotus58 appears, then flashing worked;
  - Check the other Pro Micro in VIAL as well.
7. Celebrate!
