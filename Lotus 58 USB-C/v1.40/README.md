# Lotus 58 v1.32

Starting with simple tweaks to the Lily58 Glow before ordering a set of PCB's it quickly spiraled out of control, and I ended up with what wasn't quite a Lily58 anymore, and although very similar in layout, it is no longer compatible with plate and case design. 

Because of this, it was renamed Lotus58, referencing another flower much like the lily in the name Lily58.

# Lotus 58 Glow

![Lotus 58 Glow](https://preview.redd.it/7apgomy67qf61.jpg?width=4032&format=pjpg&auto=webp&s=ce1f045339149a99311582d44b458c88c2b167a3)
(photo from reddit by u/bduzik)


**The third mayor release of the PCB.** 
This release adds an USB type C link between handsm which can be hotswapped without damage to the controller. 
Uses winged SK6812 mini-E RGB for easier build, now both under each key and for the underglow. Revamped RGB allow all RGB LED's to be soldered in place, and a switch enables power to EITHER Glow or Keys, but not both at the same time (which overpowers the USB)
Removed support for battery cut-off switch, since a nice!nano cannot be combined with USB C (Please use v1.24 for wirless builds). Several minor tweaks.

Fully compatabile with v1.11, physically identical outline for plates etc. and identical Firmware.


## Things to note when ordering PCB's
### Finding the Gerber files
If you are not aiming at modifying things, don't look for the gerber files in the folders, pretty please!</BR>
And please don't open yet another issue about it! </BR>
The gerber files are where they belong, zipped up in releases, look under that header for the version you want.

### Tips & Tricks
- Most PCB manufacturers have a MOQ of 5 PCB's, meaning you end up with 2½ keyboards when finished.
- The recommended PCB thickness is 1.6 mm, both for the main PCB and plates to allow the keyswitches to grip the plate and lock in place securely.

If ordering from [JLPCB](https://www.jlpcb.com) the plate Gerber files include a reference putting the added serial etc on a breakaway part for a clean look with minimal cost, if using another manufacturer it's possible they have additional fee's for removing the extra text, or you should consider plotting the Gerber files yourself with the correct reference for your manufacturer. Otherwise use the standard settings from JLPCB.
