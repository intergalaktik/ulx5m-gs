# ULX5M-GS
ULX5M with GateMate with SDRAM

![Layers_v001](/pic/ulx5m-gs-routed.png)
![TOP](/pic/ulx5m-gs-top.png)
![BOTTOM](/pic/ulx5m-gs-bottom.png)

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
  * [X] 8 LEDs (8)
  * [X] 3 BTNs (3)  
  * [X] SD Card (4 data lines)
  * [X] RPi 26 GPIO + 2 I2C GPIOs
  * [X] HDMI0 ( 3 diff data lines + diff clock )
  * [X] MIPI0 ( 4 diff data lines + diff clock )
  * [X] MIPI1 ( 3 diff data lines + diff clock )
  * [X] USB-C ( 1 diff data line + USBID )
  * [X] PCIe  ( 2 diff data lines + diff clock )