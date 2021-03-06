# A20-OLinuXino

Copyright (C) 2012-2018, OLIMEX Ltd

![OLIMEX Company Logo](../../images/logo-olimex.png "OLIMEX Company Logo")

## Overview

OLinuXino is a Free/Open Source Software ([FOSS](../../resources/Glossary.md)) and Free/Open Source Hardware ([FOSH](../../resources/Glossary.md)) line of products.
They are low cost (starting from EUR 24) Linux and Android Single Board Computers (SBC) in both commercial and industrial temperature range.
Board variants with extra flash memory are also available.

## Comparisons

OLinuXino is commonly compared to the Raspberry Pi and BeagleBone project.
The projects are generally similar but have different goals and implementations, so we would like to state some of the differences here:

OLinuXino models are completely open source in both hardware and software.
This means you have access to all CAD files and sources and you can reuse them for your own personal or commercial project.
There are **no** restrictions to manufacture and sell these board for your own use or resale.

The iMX233-OLINUXINO leverages the widely available iMX233 microcontroller, which only costs USD $5.50 for 100 pieces.
This means that people can spin off their own boards and manufacture them relatively cheaply as the processor is in TQFP (a package easy for hobbyist assembly).

The Raspberry Pi boards are **not** open-source.
The Raspberry Pi Foundation has not released any CAD files nor complete schematics.
Proprietary code is even required to boot the boards.
The Raspberry Pi uses a Broadcom processor, which is not available for sale in small quantities.
It also uses BGA packages which require expensive setup for assembly.
The Raspberry Pi is designed to be a home gadget, whereas OLinuXino models can work in industrial environments (-25C to +85C) and are designed to be low-cost and highly noise-tolerant.

BeagleBone have open source schematics and CAD hardware files but use a BGA processor.
The BeagleBone board is complex and difficult to manufacture in small quantities.

iMX233-OLINUXINO uses processor on 454Mhz and have less memory and will not allow fancy graphics, but this is not our intention.

## Applications

- 3D rep-rap printer controller including G-code interpreter: all 3D printers currently use PCs/Laptops connected to Arduino stepper driver; this board will handle both without problem
- Low cost PLC running open source PLC porgramming languages
- Home Automation: connecting GSM module or Zigbee sensors would be easy with the existing UEXT connector
- Most OLinuXino models only have an Ethernet port for network connectivity, but there are many low cost $10 WIFI USB modules with Linux drivers like RTL8192 which enable wireless connectivity and may control relays and sensors without need for LAN wiring
- Having a small GNU/Linux module with GPIOs would be handy even to embed it in other products.
The BeagleBone license does not allow the board to be used in commercial projects, whereas there are no restrictions with OLinuXino models

## Development

### Step 1

The OLinuXino project began with the Freescale iMX233 for several reasons: this is a 454MHz ARM9 processor with enough power to run Linux while still hand-solder-friendly TQFP package, allowing for a hobby DIY approach.
The Olimex iMX233-OLinuXino-MICRO is even on a 2-layer PCB and running at full speed.
The maximum memory of 64MB though limited the applications with it, so we were looking around for something more powerful when A13 from Allwinner came along.

### Step 2

A13 is Cortex-A8 processor which can address up to 512MB RAM and run at 1GHz.
The best of all it again comes in the hand-solder-friendly TQFP package (actually it's the first and the only Cortex-A8 in TQFP package).
Designing the A13-OLinuXino was the next logical step.
The first prototypes are already produced and everything works as expected.
A13-OLinuXino production is scheduled for September.
A13-OLinuXino have 512MB RAM, 4 USB hosts (1 dedicated for WIFI), 1 USB-OTG, Audio out, Audio in, SD-card, VGA, buttons, 72 GPIOs, and an LCD connector.

### Step 3

A10 is the big brother of A13.
It's also Cortex-A8 running at 1Ghz (many Chinese tablet/set-top-box vendors write it's 1.2 or 1.5GHz but this is overclocking and same is possible with A13 too, but not recommended for normal operation).
It can address up to 2GB of RAM, and on top of A13 have SATA, HDMI, VGA and composite video outputs) + much more GPIOs as it's in BGA442 package.
While we developed A13-OLinuXino we got many requests for hackable A10 board as all current solutions are tablets or set-top-boxes which are not designed to have GPIO connectors and to allow hardware hacking.
A10-OLinuXino will have same as A13 but including more GPIOs, 1GB RAM, HDMI, SATA and 100MBit Ethernet.

### Step 4

A10S is new processor from Allwinner with Ethernet and HDMI.
Low cost board with A10S Cortex-A8 @ 1GHz + 512MB RAM + Ethernet 100Mbit + USB Host/USB-OTG + SD-card + SD-MMC card + HDMI is released.

### Step 5

A20 is Dual Core Cortex-A7 processor which is almost pin to pin compatible, so A10 board can work with A20 processors too.
We have low cost A20 board prototypes working and A20-SOM work in progress.

### Step 6

Texas Instruments Sitara AM3352 processor is necessary for Industrial customers who want longivity supply program, TI as Freescale guarantee that when start producing processor continue the production at least 5-10 years, this way customers are not forced to change their designs every year.
So we work on AM3352 module with: AM3352 720Mhz, Cortex-A8 processor, 512MB DDR3 RAM (optional we will make 1GB RAM version also), power supply 6-16VDC, x4 USB 2.0 hosts, 100Mbit Ethernet, SD-card, VGA, CAN, GPIO connector, LCD connector with touchscreen to work with A13-LCD7TS and A13-43TS LCDs, UEXT connector, JTAG.

### Step 7

Allwinner A64 chip into A64-OLinuXino development board.

### Step 8

DYI laptop TERES-I with A64 chip.

### Step 9

Expanded the A20 portfolio with more convenient A20-SOM204 board.

### Step 10

... we don't know yet, there are lot of candidates.

## Web Resources

- [OLIMEX Ltd website](http://www.olimex.com) where the OLinuXino board info is available
- [GitHub project repository](https://github.com/OLIMEX/OLINUXINO) for Hardware and Software resources
- [Olimex forum](https://www.olimex.com/forum/index.php) for OLinuXino project discussions
- OLinuXino IRC channel: join #olimex on [irc.freenode.net](irc.freenode.net)
  - Alternatively use [web IRC chat](http://webchat.freenode.net/?channels=olimex)

## License

### Hardware

- The Hardware project is released under the Creative Commons Attribution-Share Alike 3.0 United States License.
- You may reproduce it for both your own personal use, and for commercial use. 
- You will have to provide a link to the original creator of the project ([http://www.olimex.com](http://www.olimex.com)) on any documentation or website.
- You may also modify the files, but you must then release them as well under the same terms.
- Credit can be attributed through a link to the [creator website](http://www.olimex.com).

### Software

- The software is released under GPL.
