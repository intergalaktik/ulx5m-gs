# Work in progress!!! 

# V003 should be good enough for all experiments you need!

# Please check the list of confirmed working

# ULX5M-GS
ULX5M with GateMate with SDRAM

![Layers_v001](/pic/ulx5m-gs-routed.png)
![TOP](/pic/ulx5m-gs-top.png)
![BOTTOM](/pic/ulx5m-gs-bottom.png)

#### ULX5M-GS V001

![Assembled](/pic/v1-assembled.jpg)

#### V001 LED ON

![Green](/pic/v1-green.jpg)

#### ULX5M-v02 bringup

#### Blink LED

[![ULX5M blinks LEDs on its own](/pic/ulx5m-gs.v02.4.debug.jpg)](https://www.youtube.com/watch?v=LA20pfW7X00 "ULX5M is counting!")

#### DVI OUT

![V002](/pic/ULX5M-GS-v002.jpg)

#### SDRAM working with LiteX

![V002 Litex](/pic/LiteX_SDRAM_ULX5M.png)

![V002 Litex full memtest](/pic/LiteX_ULX5M-memtest.png)

#### VGA over GPIO

While testing LVDS I wanted to check if we can have VGA over GPIO and it looks OK 

![V002 VGA](/pic/VGA_LVDS.jpg)

For now only possible over VGA

![V002 Invaders_VGA](/pic/Invaders_ULX5M.jpg)

![V002 ZX_VGA](/pic/ZX_ULX5M.jpg)

![V002 Colevision_VGA](/pic/Colevision_ULX5M.jpg)

* Power regulators
  * [MPM3833C](https://www.monolithicpower.com/en/mpm3833c.html) 0.9V..1.1V V_core, 3A
  * [TI62569](https://www.ti.com/lit/ds/symlink/tlv62569.pdf?ts=1709559273755) 1.2V, 1.8V, 2.5V, 3.3V V_io, 2A

* GateMate
  * compatibility to A1
  * ext. clock: 100 MHz lvds (can be used for both serdes and pll)
  * ext. clock: 25MHz
  * programmer interface
  * usb-c connector
  * select between flash and jtag config (DIP switch)

* Gigabit Ethernet
  * KSZ9031RNXCA

* SDRAM 1V8/2.5V/3.3V selectable in production

* Interfaces
  * [X] 8 LEDs ( 8 )
  * [X] 3 BTNs ( 3 )  
  * [X] SD Card (4 data lines)
  * [X] RPi 26 GPIO + 2 I2C GPIOs ( 12 diff pairs + 2 routed no diff )
  * [X] DDMI0 ( 3 diff data lines + diff clock )
  * [X] LVDS0 ( 4 diff data lines + diff clock )
  * [X] LVDS1 ( 3 diff data lines + diff clock )
  * [X] USB-C ( 1 diff data line + USBID )
  * [X] PCIe  ( 2 diff data lines + diff clock )
  * [X] SDRAM
  * [X] Gigabit Ethernet
  * [X] FLASH

 * Tested and confirmed working ov V002 ( with patches ) 
  * [X] LEDs
  * [X] BTNs - work on v002 but better use v003
  * [X] Video output ( DVI )
  * [X] GPIO output
  * [X] USB-C TinyDFU USB Bootloader
  * [X] Serial Over GPIO
  * [X] VGA Over GPIO
  * [X] JTAG
  * [X] LVDS - rapicam*
  * [X] DIP SW - they work as FLASH BOOT SELECT
  * [X] FLASH - I can put bitstream in flash and boot from flash
  * [X] SDRAM - tested with LiteX works from v002
  * [X] SD - tested with LiteX works from v002
  * [ ] Ethernet - not tested - needs V003
  * [ ] PCIe - not tested

*DVI - only with nextpnr and with many tries with SEED= - so HW is OK but we have timming issues
   
*LVDS I can get cam stream not to trow any error but without and output 
  if I add output cam trows errors - there are some timming issues in the core... 

## References

https://github.com/OLIMEX/GateMateA1-EVB

https://github.com/intergalaktik/Extension_Boards_for_Olimex_GateMate

https://github.com/YosysHQ/prjpeppercorn-test-cases

https://github.com/YosysHQ/prjpeppercorn
  
https://github.com/chili-chips-ba/openCologne

https://www.chili-chips.xyz/open-cologne

## Acknowledgements

This project was done in collaboration with Chili Chips*Ba team. 
They have put enormes effort in making all cores to work on GateMate even before we have our own board!
Thanks to them now we have big set of cores that can be used to check and improve opensource toolchain!
They are proven to be reliable partners that solves problem quickly and on side works on educating younger generations!

Also big thanks goes to YosysHQ as they are doing miracles with open source tooling, and we now finaly have one that works for GateMate!

From YosysHQ special thanks to Micko and Lofty that are helping in real time on Discord!

Special thanks to Patrick from Cologne, as without him and rest of Cologne team we would not be able to get this project done.

## Work on this board is financed by NLnet foundation

![NLnet](/pic/banner-320x120.png)

https://nlnet.nl/project/openCologne/

This project was funded through the NGI0 Entrust Fund, a fund established by NLnet with financial support from the European Commission's Next Generation Internet programme, under the aegis of DG Communications Networks, Content and Technology under grant agreement No 101069594.

## Check up our blogposts
Comming soon!!!

## Contact us

Discord: https://discord.gg/qwMUk6W
