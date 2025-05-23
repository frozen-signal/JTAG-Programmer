# Description

A Kicad project for a JTAG Programmer. Compatible with Lattice Diamond Programmer, Radiant Programmer and iCEcube2.

# How to use

## One-time setup

Once assembled, a one-time setup need to be done:
(TODO: Add images)
1. Download and install [FT_Prog from FTDI](https://ftdichip.com/utilities/#ft_prog)
1. Connect the JTAG-Programmer to your PC with a USB cable.
1. Do a scan: DEVICE > Scan and parse
1. Go to FILE > Open Template and select "JTAG_PROGRAMMER.xml"
1. Go to DEVICE > Program, and click Program
1. Make sure the JTAG-Programmer has been correctly programmed by quitting FT_Prog and re-opening it, then doing a scan again. Check that the template has been applied to the JTAG-Programmer.

## Programming a FPGA

... TODO ...

<a align="center">
    <img src="/resources/render.png" style="width: 480px"/>
</a>
<p><i>A rendering of the programmer</i></p>