# Description

A Kicad project for a JTAG Programmer. Compatible with Lattice Diamond Programmer, Radiant Programmer and iCEcube2.

# How to use

## One-time setup

Once assembled, a one-time setup need to be done:
(TODO: Add images)
1. Download and install [FT_Prog from FTDI](https://ftdichip.com/utilities/#ft_prog)
1. Connect the JTAG-Programmer to your PC with a USB cable.
1. Do a scan: DEVICE > Scan and parse.<br /><a align="center"><img src="/resources/ScanParse.png" style="width: 480px"/></a>
1. Go to FILE > Open Template and select "JTAG_PROGRAMMER.xml".<br /><a align="center"><img src="/resources/OpenTemplate.png" style="width: 480px"/></a>
1. Go to DEVICE > Program, and click Program.<br /><a align="center"><img src="/resources/FTProgProgram.png" style="width: 480px"/></a>
1. Make sure the JTAG-Programmer has been correctly programmed by quitting FT_Prog and re-opening it, then doing a scan again. Check that the template has been applied to the JTAG-Programmer ("Product Desc" should be "JTAG Program").

## Example of Programming a MACHXO2 FPGA with Lattice Diamond Programmer

This shows an example of how the JTAG-Programmer can be used to program a FPGA. This example suppose you already have installed the Lattice Diamond Programmer (As standalone or as part of the [Lattice Diamond Toolchain](https://www.latticesemi.com/Products/DesignSoftwareAndIP/FPGAandLDS/LatticeDiamond)
1. Make sure the JTAG-Programmer is connected to the PC.
1. Run the Lattice Diamond Programmer, select "Create a new blank project" is selected, and click "OK".<br /><a align="center"><img src="/resources/BlankProject.png" style="width: 480px"/></a>
1. Click on the "Generic JTAG Device" under Device Family, and select the FPGA family.<br /><a align="center"><img src="/resources/FPGA_Family.png" style="width: 480px"/></a>
1. Click on the element under "Device" and select the correct device.<br /><a align="center"><img src="/resources/FPGA_Device.png" style="width: 480px"/></a>
1. Make sure the Operation is "Flash Erase,Program,Verify".
1. Under File Name, select the programming file. In our case, it's the generated JEDEC file (*.jed).
1. Connect the JTAG cable to the device and click "Program".<br /><a align="center"><img src="/resources/JTAG_Program.png" style="width: 480px"/></a>
1. Once Diamond Programmer finishes, your FPGA should now be programmed.

# An overview of the JTAG-Programmer
(TODO: Add a description of the pins)

<a align="center">
    <img src="/resources/render.png" style="width: 480px"/>
</a>
<p><i>A rendering of the programmer</i></p>
