# Project  Cirrus Logic 542x ISA video card
This project is a fork of [542x_ISA](https://github.com/matt1187/542x_ISA) with some tweaks
and additions to the PCB. Notable changes compared to original project:
- made room on PCB to place the RAMs in SMT sockets
- added Monitor ID option (static or by attached Monitor)

Remaking from Cirrus Logic Databook  "CL-GD542X_Technical_Reference_Manual_Jan1994"
![grafik](https://github.com/HenrykRichter/CL-GD542x_ISA/blob/main/Pics/CL-GD542xISA_1280.jpg)

# PCB Revision History 
- forked from revision 001
- CL-GD542x-003 initial upload

# Features
- Cirrus Logic (CL-GD5422-5429) video chipset (5420 is not recommend for this design)
- good chocie video card for ISA bus platform
- up to 2 MB DRAM
- 80 MHz integrated RAMDAC (GD5429: 86 MHz )
- Win 3.1, Win9x, Win NT 3.51 & 4 driver available
- cheap GD542x VLB card as compoment donor.
- cheap 2 layer PCB layout 
  
# Issues 
- some 542x chip has vertical noise/stripe on TFT. (It is not pcb issuses)
- ROM from  cirrus logic video card as donor is not usable (hi/lo byte is seperated to difference address space, like address line "A0 and A14" is swapped)
- in some cases, the GD542x will boot in Monochrome mode. See [here](https://forum.vcfed.org/index.php?threads/trident-card-that-thinks-colour-monitor-is-monochrome.79054) for a fix.

# notes
- GD5420/22/24 support only 1 MB DRAM
- U11 & U12  is first 1 MB , U13/14 is seconds MB (except 5420, only U12 and U14 )
- all component with  followed ID is config strap (R55, R57, R59, R61, R63, R69, R73) place all **except** R55, R69
- R15 don't place, if you using interal XTAL oscillator (Y1/Y2 , C39,C40)
- Place only one of Y1/Y2 (either SMD **or** HC-49)
- SPI-EEPROM is optional.

 

# Bill of material

- [![csv-file 001 ](https://github.com/matt1187/542x_ISA/blob/main/Gerber/542xISA-001.csv)]
- [![csv-file 002(not tested)](https://github.com/matt1187/542x_ISA/blob/main/Gerber/542xISA-002.csv)]
- [Config strap (R55, R57, R59, R61, R63, R69, R73) Place all resistor except R69
- [![Gerber file 001](https://github.com/matt1187/542x_ISA/blob/main/Gerber/542xISA-001.zip)]
- [![Gerber file 002(not tested)](https://github.com/matt1187/542x_ISA/blob/main/Gerber/542xISA-002.zip)]

# driver & ROM 
- [![Cirrus Logic ROM generic for all GD542x,](https://github.com/matt1187/542x_ISA/blob/main/ROM/cirrus%205428.zip)]




# License
The project is free for non-commercial reproduction. Do not sell it on Ebay or other platforms for profit. Do not make a closed source derivative. Share your experiences and ideas with the community.

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png


