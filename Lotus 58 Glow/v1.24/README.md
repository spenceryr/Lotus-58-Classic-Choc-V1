# Lotus 58 v1.24

Starting with simple tweaks to the Lily58 Glow before ordering a set of PCB's it quickly spiraled out of control, and I ended up with what wasn't quite a Lily58 anymore, and although very similar in layout, it is no longer compatible with plate and case design. 

Because of this, it was renamed Lotus58, referencing another flower much like the lily in the name Lily58.

# Lotus 58 Glow

![Lotus 58 Glow](https://preview.redd.it/7apgomy67qf61.jpg?width=4032&format=pjpg&auto=webp&s=ce1f045339149a99311582d44b458c88c2b167a3)
(photo from reddit by u/bduzik)


**v1.24 - The third major release of the PCB and plates.** 

- Added Silkscreen build instructions
- Added TRRS ESD protection
- Removed i2c resistors
- Repositioned reset for easier access
- Minor cleanup of routing and silkscreen

v1.23 uses winged SK6812mini-E RGB for easier build, along with SK6812 mini RGB for underglow. Revamped RGB to allow easier use of underglow and per-key separate or combined. Added support for battery cut-off switch for easy wireless builds with nice!nano. Several minor tweaks.

Fully compatabile with v1.11 & v1.23, physically identical outline for plates etc. and identical Firmware.


# Parts needed



| Name of part | Qty. | Optional | Remarks | Aliexpress |
| ------------ | ---- | -------- | ------- | --------------- |
| PCB          | 2    | X        | 1,6mm thick | X           |
| Top plate         | 2 | X        | Optional layouts for OLED or encoder in top position. | X |
| Bottom plate         | 2 | X        | X | X |
| Kailh hotswap socket | 56-58 | X | Qty. depends on layout. | [link](https://www.aliexpress.com/item/-/4001051840976.html?spm=a2g0s.8937460.0.0.6f132e0eKYB5RQ&_ga=2.174414626.1036705865.1612730332-979734211.1611132916&_gac=1.119713146.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |
| Diodes 1N4841 (TH) or 1N4148W (SMD) | 56-58 | X | Qty. depends on layout. TH recommended for beginners. | [link(TH)](https://www.aliexpress.com/item/HOT-SELL-100-PCS-1N4148-DO-35-IN4148-Silicon-Switching-Diode-FREE-SHIPPMENT/32660088529.html?spm=a2g0s.8937460.0.0.c1b82e0edjrOT3&_ga=2.216963734.1036705865.1612730332-979734211.1611132916&_gac=1.53192282.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) or [link(SMD)](https://www.aliexpress.ru/item/-/1005002059571417.html?spm=a2g0s.8937460.0.0.c1b82e0edjrOT3&_ga=2.216963734.1036705865.1612730332-979734211.1611132916&_gac=1.53192282.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |
| Capacitors 100 nF | 0-4 | ✔ | Qty. depends on layout. 2 needed for each encoder installed. | [link](https://www.aliexpress.com/item/-/32971478818.html?spm=a2g0s.8937460.0.0.6f132e0eKYB5RQ&_ga=2.149198518.1036705865.1612730332-979734211.1611132916&_gac=1.48473428.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |
| Resistor 4.7 kOhm | 0-4 | ✔ | Qty. depends on layout. 2 needed for each OLED installed. | [link](https://www.aliexpress.com/item/-/32847047012.html?spm=a2g0s.8937460.0.0.c1b82e0edjrOT3&_ga=2.241041155.1036705865.1612730332-979734211.1611132916&_gac=1.219449963.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |
| 0.91" OLED Display | 0-2 | ✔ | Qty. depends on layout. | [link](https://www.aliexpress.com/item/-/4001028384269.html?spm=a2g0s.8937460.0.0.c1b82e0edjrOT3&_ga=2.241041155.1036705865.1612730332-979734211.1611132916&_gac=1.219449963.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |
| TRRS jack PJ-320A | 2 | X | X | [link](https://www.aliexpress.com/item/-/4000114275750.html?spm=a2g0s.8937460.0.0.c1b82e0edjrOT3&_ga=2.148895671.1036705865.1612730332-979734211.1611132916&_gac=1.262958974.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |
| SRV05-4 ESD | 1 | ✔ | SOT-23-6 IC package |  |
| M2 * 10 mm standoff | 10 | X | Rounded, max 3.7 mm in diameter | [link](https://www.aliexpress.com/item/-/32863484622.html?spm=a2g0s.8937460.0.0.c1b82e0edjrOT3&_ga=2.215809815.1036705865.1612730332-979734211.1611132916&_gac=1.26395343.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |
| M2 * 4 mm screw | 20 | X | 4-8 mm length fits, low profile hex head recommended | [link](https://www.aliexpress.com/item/-/32966917947.html?spm=a2g0s.8937460.0.0.c1b82e0edjrOT3&_ga=2.246923140.1036705865.1612730332-979734211.1611132916&_gac=1.263439230.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |
| TRRS cable | 1 | X | Needs to be 4 poles, more common 3 poles cable creates a shortcircuit | [link](https://www.aliexpress.com/item/32905903526.html?spm=a2g0o.productlist.0.0.1ea55b40PsHOY6&algo_pvid=74ac6da4-21fa-4152-a7a7-805ba558a2d8&algo_expid=74ac6da4-21fa-4152-a7a7-805ba558a2d8-1&btsid=2100bb4c16148500192992030ee115&ws_ab_test=searchweb0_0,searchweb201602_,searchweb201603_) |
| Silicon pads | 10 | X | X | [link](https://www.aliexpress.com/item/-/32912066603.html?spm=a2g0s.8937460.0.0.6f132e0eKYB5RQ&_ga=2.145547188.1036705865.1612730332-979734211.1611132916&_gac=1.57255896.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |
| Pro Micro | 2 | X | Can be built with various ProMicro clones as well as Elite C (Or nice!nano for a wireless keyboard) | [link](https://www.aliexpress.com/item/-/32849563958.html?spm=a2g0s.8937460.0.0.c1b82e0edjrOT3&_ga=2.175422242.1036705865.1612730332-979734211.1611132916&_gac=1.225165928.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |
| MillMax low profile sockets | 1 | Purchased as 1x64 pin and split | [link] (https://eu.mouser.com/ProductDetail/575-641503)|
| Rotary Encoder | 0-2 | ✔ | Qty. depends on layout. | [link](https://www.aliexpress.com/item/10000056483250.html?spm=a2g0o.productlist.0.0.64951c5fKcPiug&algo_pvid=b530d9b1-fbd2-4598-bf53-bece1343826f&algo_expid=b530d9b1-fbd2-4598-bf53-bece1343826f-2&btsid=2100bdd016135510210168102eefcc&ws_ab_test=searchweb0_0,searchweb201602_,searchweb201603_) |
| Rotary Encoder Knob | 0-2 | ✔ | One needed for each encoder. Clearance for max 24 mm diameter, pick halfshaft or spline according to encoder choice.  | [link](https://www.aliexpress.com/item/10000056483250.html?spm=a2g0o.productlist.0.0.64951c5fKcPiug&algo_pvid=b530d9b1-fbd2-4598-bf53-bece1343826f&algo_expid=b530d9b1-fbd2-4598-bf53-bece1343826f-2&btsid=2100bdd016135510210168102eefcc&ws_ab_test=searchweb0_0,searchweb201602_,searchweb201603_) |
| SK6812 mini-E (3535) | 56-58 | ✔ | Qty. depends on layout. Mini E are winged for easier soldering. | [link](https://www.aliexpress.com/item/4000475685852.html?spm=a2g0o.productlist.0.0.3ec76d0aSbZSMy&algo_pvid=c175ec6d-d797-4bad-885d-dd7ab2025889&algo_expid=c175ec6d-d797-4bad-885d-dd7ab2025889-1&btsid=0b0a01f816148497094017930e33f7&ws_ab_test=searchweb0_0,searchweb201602_,searchweb201603_) |
| SK6812 mini (3535) | 12 | ✔ | For underglow, note that Mini E version does not fit here. | [link](https://www.aliexpress.com/item/-/4001361956752.html?spm=a2g0s.8937460.0.0.6f132e0eCg84IE&_ga=2.137862832.1036705865.1612730332-979734211.1611132916&_gac=1.14797764.1611132916.CjwKCAiAxp-ABhALEiwAXm6IyZF-HtTdP3MQioG5GOxLvsaJfBbhqTGIQbmV0LXKDx2MZSDJJJTbaBoCPkoQAvD_BwE) |

## Things to note when ordering PCB's
### Finding the Gerber files
If you are not aiming at modifying things, don't look for the gerber files in the folders, pretty please!</BR>
And please don't open yet another issue about it! </BR>
The gerber files are where they belong, zipped up in releases, look under that header for the version you want.

### Tips & Tricks
- Most PCB manufacturers have a MOQ of 5 PCB's, meaning you end up with 2½ keyboards when finished.
- The recommended PCB thickness is 1.6 mm, both for the main PCB and plates to allow the keyswitches to grip the plate and lock in place securely.

If ordering from [JLPCB](https://www.jlpcb.com) the plate Gerber files include a reference putting the added serial etc on a breakaway part for a clean look with minimal cost, if using another manufacturer it's possible they have additional fee's for removing the extra text, or you should consider plotting the Gerber files yourself with the correct reference for your manufacturer. Otherwise use the standard settings from JLPCB.
