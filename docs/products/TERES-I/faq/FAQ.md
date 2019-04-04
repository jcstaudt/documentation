# Frequently Asked Questions (FAQ)

## General

* [Where does the name TERES come from?](name-origin.md)
* [What makes this laptop so different?](what-is-unique.md)
* [Why does open-source matter so much?](importance-of-open-source.md)
* [Where are the open-source materials?](sources.md)
* [How may I contribute to this project?](https://github.com/OLIMEX/DIY-LAPTOP/blob/master/CONTRIBUTING.md)
* I have a question or feedback that does not constitute opening up a ticket. Where do I go?
  * Check out the [user forum](https://www.olimex.com/forum/index.php?board=39.0)!

## Hardware

* Where are the design files for a 3D-printed laptop enclosure?
  * A 3D-printed case design has been developed by [Fork Sand, Inc.](https://www.forksand.com) and the design files may be found [here](https://code.forksand.com/forksand/olimex-teres-case).
* Are there alternative keyboard options available?
  * None are currently available. Please test compatibility, design a 3-D printed keyboard bezel, and it may get implemented!

## Software

* Does the TERES-I have an upstream mainline kernel? Upstream u-boot?
  * "It works with mainline kernel. There is a debian image with mainline u-boot and kernel." [as of linux-image-4.16.0-rc6-arm64]
  * References:
    * [Olimex Teres-A64: Current Status](http://linux-sunxi.org/Olimex_Teres-A64#Current_status)
    * [Linux mainlining effort](https://linux-sunxi.org/Linux_mainlining_effort)
    * [A64](https://linux-sunxi.org/A64)
    * [lkml.org patch](https://lkml.org/lkml/2018/4/30/288)
    * [Debian bug report](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=892786)
* How do I install operating system _____?
  * Please reference the [software documentation](https://github.com/OLIMEX/DIY-LAPTOP/tree/master/SOFTWARE/README.md) section for details.
If your desired operating system is not listed, it is most likely not yet supported.
We'd love your help getting it to run on the TERES-I!
