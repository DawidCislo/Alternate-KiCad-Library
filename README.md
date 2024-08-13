# Alternate-KiCad-Library

Alternate KiCad Library is a symbol and footprint library for KiCad EDA Software. Symbol libraries contain various analog integrated circuits, discrete semiconductors, LEDs and passive components. Footprint libraries contain passives, diode, LED, transistor and IC packages. All symbols and footprints are either edited versions of standard KiCad components or have been created from scratch.

## Version 4.0 is out now, get it via KiCad's PCM or download directly from this repository.

[Documentation](https://alternatekicadlibrary.com/rc_images/akl_user_manual.pdf)

[Installation Instructions](https://alternatekicadlibrary.com/setup.html)

## List of changes:

New symbol libraries:
- Crystal_AKL - symbols for crystal resonators and oscillators with pre-assigned footprints
- LED_AKL - colorful symbols for LEDs with pre-assigned footprints (disable 'override individual item colors' in preferences -> colors)
- Voltage_Regulator_AKL - symbols for linear voltage regulators with pre-assigned footprints based on part numbers.

Some symbols have new Alternate Body Styles. Go to symbol properties and check the "Alternate symbol (deMorgan)" checkbox
- 2-pin resistors, diodes and capacitors have a 45-degree rotated version with pins still on the 50 mil grid
- Dual common anode, common cathode and series diodes have an alternative symbol.
- Analog ICs with resistors in their symbols have a US-style resistor version.
![image](https://github.com/DawidCislo/Alternate-KiCad-Library/assets/48568748/327ff410-a5ca-45b5-af7f-f3d73abfbcc6)

Most NC pins were changed to Free unless explicitly indicated as 'Do not connect" by the manufacturer. In some cases having an ability to route through the NC pads or tie them to a heat-sink plane is useful. Now KiCad will allow connecting tracks to these pins, unless they already have an assigned net (i.e. there is already a track running through it)

New symbols for existing symbol libraries:
- Diode_AKL: 1141 new symbols
- Diode_Current_Limiting_AKL: 16 new symbols
- Diode_Schottky_AKL: 396 new symbols
- Diode_TVS_AKL: 137 new symbols
- Diode_Zener_AKL: 476 new symbols
- Diode_Bridge_AKL: 6 new symbols

New footprint libraries:
- LED_SMD_AKL and LED_SMD_Handsoldering_AKL - surface-mount LED footprints used by the LED_AKL symbol library
- LED_THT_AKL and LED_THT_AKL_Double - through-hole LED footprints used by the LED_AKL symbol library

New ThermalVias2 footprints for devices with heatsink pads. These footprint variants use standard untented vias surrounded by soldermask instead of expensive via-in-pad. Thermal transfer efficiency is lower but soldering is more repeatable
![image](https://github.com/user-attachments/assets/2bab1a59-5488-46cc-b884-e96baac72fea)

Crystal_AKL footprint library and it's variants:
- Added Crystal_SMD_8.7x3.8_P5.50mm

Diode_THT_AKL footprint library and it's variants:
- Added DO-7 (DO-204AA) series
- Added 7.3x22mm package used by BY4 series high voltage diodes
- Added SOD-23 - old plastic rectangular diode package
- Added SOD-61 series
- Added SOD-61A series
- Added CASE-194 series

Package_DFN_QFN_AKL footprint library:
- Added DFN-8-1EP_3x2mm_P0.5mm_EP1.7x1.6mm

Package_SO_AKL footprint library:
- Added SOIC-8-1EP_3.9x4.9mm_P1.27mm_EP2.29x2.29mm and thermal vias variants
- Added Infineon_PG-SSOP-14 and thermal vias variants
- Added ST_PowerSSO-12 and thermal vias variants

Package_TO_SOT_SMD_AKL footprint library:
- Added 1.27mm pin pitch variants for TO-252-4 and TO-252-5 footprints
- Added Diodes_SOT-89-5

Package_TO_SOT_THT_AKL footprint library and it's variants:
- Added 'BigPads' handsoldering-friendly versions for most metal-can packages (TO-3, TO-5, TO-18, TO-39, TO-46, TO-78, TO-99 and TO-100)
- Added TO-71-6 amd TO-71-8 along with BigPads variands
- Added two-pin TO-3PF and KA variants
- Added SOT-33 and SOT-33_Inline with pin variants
- Added SOT-25 with pin variants

Bugfixes (see [commit list](https://github.com/DawidCislo/Alternate-KiCad-Library/commits/main/)

## Installation instructions for Plugin and Content Manager:

KiCad 8 automatically adds third-party libraries to library tables, by default it also adds the `PCM_` prefix to their names.
If you have the defauly `PCM_` prefix in `Preferences` -> `Packages and Updates`, simply choose the defauly 4.0.1 version.

If you want no prefixes, simply leave the `Library nickname prefix` blank and chose version 4.0 in package manager.

Refer to [Installation Instructions](https://alternatekicadlibrary.com/setup.html) for more detailed guide

## Manual installation:

Extract the downloaded AKL files into any folder you want.

KiCad uses library tables to keep track of installed libraries.
To install libraries manually, go to `Manage Footprint Libraries` in the preferences tab.
 
Press the Folder icon below the table and locate the folder with the extracted footprint library files

Multiple folders ending in `.Pretty` should be visible. Each of these is a separate footprint library. Select all the libraries that you want to install and press `Select Folder`

Next, go to `Manage Symbol Libraries` in the preferences tab. 
 
Press the Folder icon below the table and locate the folder with the extracted symbol library files

Multiple files ending in `.kicad_sym` should be visible. Each of these is a separate symbol library. Select all the libraries that you want to install and press `Open`.

All the installed libraries should be now accessible.

# File description

`Footprints` folder contains AKL footprint libraries.

`Symbols` folder contains AKL symbol libraries.

`AKL User Manual.pdf` is a comprehensive guide with detailed description of each added library.

`KiCad Files` folder contains original license and readme files from the first-party KiCAD library.

`Sources` Contains catalgues and data sheets that are no longer widely accessible that were used for reference.

`PCM_Releases` folder contains legacy 2.0 package used by KiCad's content manager.

License:

Alternate KiCad Library by Dawid Cisło is a derivative of KiCad Library made by KiCad community
(see: KiCad library GitLab: https://gitlab.com/kicad/libraries), used under Creative Commons CC-BY-SA 4.0 License (https://creativecommons.org/licenses/by-sa/4.0/legalcode), with the following
exception:

To the extent that the creation of electronic designs that use 'Licensed Material' can be considered to
be 'Adapted Material', then the copyright holder waives article 3 of the license with respect to these
designs and any generated files which use data provided as part of the 'Licensed Material'.


What does this mean?
You can freely use Alternate KiCad Library data for commercial, closed and non-commercial projects
without any restrictions. There is no need to attribute this library or original KiCad libraries within your
design and no obligation to share any project files under this or any other license agreement.
If you wish to redistribute the Alternate KiCad Library, or its parts (including in modified form) as a
collection you need to share it under the same license agreement. Libraries must also retain attribution
information and license documents which are distributed with the library files.

### Compatibility:

Alternate KiCad Library 4.0 works with KiCad 8

Alternate KiCad Library 3.0 works with KiCad 6

Alternate KiCad Library 2.0 is known to work with KiCad 6.0.0-rc-1 but should be cross-compatible with all KiCad 6 versions.
Footprint library should be backwards compatible with KiCad 5


## Changelog:

## Version 4.0
NEW SYMBOLS:

- Crystal_AKL - symbols for crystal resonators and oscillators with pre-assigned footprints
- LED_AKL - colorful symbols for LEDs with pre-assigned footprints (disable 'override individual item colors' in preferences -> colors)
- Voltage_Regulator_AKL - symbols for linear voltage regulators with pre-assigned footprints based on part numbers.

Some symbols have new Alternate Body Styles. Go to symbol properties and check the "Alternate symbol (deMorgan)" checkbox
- 2-pin resistors, diodes and capacitors have a 45-degree rotated version with pins still on the 50 mil grid
- Dual common anode, common cathode and series diodes have an alternative symbol.
- Analog ICs with resistors in their symbols have a US-style resistor version.

Most NC pins were changed to Free unless explicitly indicated as 'Do not connect" by the manufacturer. In some cases having an ability to route through the NC pads or tie them to a heat-sink plane is useful. Now KiCad will allow connecting tracks to these pins, unless they already have an assigned net (i.e. there is already a track running through it)

New symbols for existing symbol libraries:
- Diode_AKL: 1141 new symbols
- Diode_Current_Limiting_AKL: 16 new symbols
- Diode_Schottky_AKL: 396 new symbols
- Diode_TVS_AKL: 137 new symbols
- Diode_Zener_AKL: 476 new symbols
- Diode_Bridge_AKL: 6 new symbols

NEW FOOTPRINTS:
- LED_SMD_AKL and LED_SMD_Handsoldering_AKL - surface-mount LED footprints used by the LED_AKL symbol library
- LED_THT_AKL and LED_THT_AKL_Double - through-hole LED footprints used by the LED_AKL symbol library

New ThermalVias2 footprints for devices with heatsink pads. These footprint variants use standard untented vias surrounded by soldermask instead of expensive via-in-pad. Thermal transfer efficiency is lower but soldering is more repeatable

Crystal_AKL footprint library and it's variants:
- Added Crystal_SMD_8.7x3.8_P5.50mm

Diode_THT_AKL footprint library and it's variants:
- Added DO-7 (DO-204AA) series
- Added 7.3x22mm package used by BY4 series high voltage diodes
- Added SOD-23 - old plastic rectangular diode package
- Added SOD-61 series
- Added SOD-61A series
- Added CASE-194 series

Package_DFN_QFN_AKL footprint library:
- Added DFN-8-1EP_3x2mm_P0.5mm_EP1.7x1.6mm

Package_SO_AKL footprint library:
- Added SOIC-8-1EP_3.9x4.9mm_P1.27mm_EP2.29x2.29mm and thermal vias variants
- Added Infineon_PG-SSOP-14 and thermal vias variants
- Added ST_PowerSSO-12 and thermal vias variants

Package_TO_SOT_SMD_AKL footprint library:
- Added 1.27mm pin pitch variants for TO-252-4 and TO-252-5 footprints
- Added Diodes_SOT-89-5

Package_TO_SOT_THT_AKL footprint library and it's variants:
- Added 'BigPads' handsoldering-friendly versions for most metal-can packages (TO-3, TO-5, TO-18, TO-39, TO-46, TO-78, TO-99 and TO-100)
- Added TO-71-6 amd TO-71-8 along with BigPads variands
- Added two-pin TO-3PF and KA variants
- Added SOT-33 and SOT-33_Inline with pin variants
- Added SOT-25 with pin variants

BUGFIXES:

Amplifier_Difference_AKL symbol library: 
- AD626 – corrected +VS pin’s electrical type to “Power Input”.
- AD8209 – fixed datasheet link.
- INA132 – fixed resistor values.

Analog_AKL symbol library:
- AD8307 – fixed symbol graphics.
- AD604 – fixed datasheet links.

Amplifier_Operational_AKL symbol library:
- AD8008 – fixed parent symbol.
- AD8012 – fixed parent symbol and updated datasheet links.
- AD8048 – fixed parent symbol and description.
- AD8513 – fixed parent symbol.
- AD8534 – fixed parent symbol.
- AD8539 – fixed parent symbol.
- AD8554 – fixed parent symbol.
- AD8594ACPZ – fixed pinout.
- AD8608 – fixed parent symbol.
- AD8618 – fixed parent symbol.
- AD8664 – fixed parent symbol.
- ADA4522-4ARZ – fixed parent symbol.
- ADA4638-1ARZ – fixed parent symbol.
- ADA4891-1 – fixed parent symbol.
- LMC6042 and LMC6044 – fixed datasheet links
- LMP7716  – fixed parent symbol, description and datasheet links. 
- LTC2050 – renamed shutdown pin. 
- MCP6H82T-E-MNY and MCP6H92T-E-MNY removed duplicate NC pins.
- MCP617 – fixed parent symbol.
- MCP6044 – fixed parent symbol.
- MCP6144 – fixed parent symbol.
- MCP6232 – fixed parent symbol.
- MCP6234 – fixed parent symbol.
- MCP6242 – fixed parent symbol.
- MCP6244 – fixed parent symbol.
- MCP6274 – fixed parent symbol.
- MCP6284 – fixed parent symbol.
- MCP6294 – fixed parent symbol.
- NE5534 – fixed datasheet link.
- OP221 – fixed datasheet link.
- OP293 – fixed datasheet link.
- OP413 – fixed footprint.
- OP491 – fixed parent symbol.
- OP495GSZ – fixed datasheet link
- OPA227AIDRM – fixed pinout.
- OPA551PA’s – fixed FLAG’s pin electrical type.
- OPA606 – fixed datasheet link.
- OPA683ID’s – fixed pinout.
- OPA2337 and OPA2338 – fixed parent symbol.
- TSX634 – fixed parent symbol.
- TSV734IP – fixed parent symbol.
- TS9224 – fixed parent symbol.
- TLV2464 – fixed parent symbol.
- TLE2144 – fixed parent symbol.
- TLC271 – fixed datasheet links.
- OPA4350UA – fixed parent symbol.
- OPA4277 – fixed parent symbol.
- OPA4241 and OPA4251 – fixed parent symbols.
- OPA4227 and OPA4228 – fixed parent symbols.

Analog_Comparator_AKL symbol library:
- MAX999 – fixed pinout.
- MCP6548 – fixed datasheet link.
- TLV350 – removed incorrect hidden NC pins.
- TLC374 – fixed parent symbol.
- MAX9034 – fixed symbol names.

Diode_AKL symbol library:
- DTV1500MD – fixed footprint.
- Quad Common cathode and anode generic symbols (and derived symbols) now have their pins aligned to 1.27mm grid.
- BAS678 – fix symbol name.
- RS3xB series – fixed footprinds.

Diode_Schottky_AKL symbol library:
- MBRF10200CT – updated datasheet link.
- MBR40250 – changed to a correct parent symbol.
- BAT40V – added separated symbol.
- BAT17-07 – added separated symbol.

Diode_TVS_AKL symbol library:
- TSMPxxA series TVS diode – fixed footprints (SMP_Reverse)
- DT1140-04LP – fixed symbol graphics.
- D_TVS_Array_Generic_4xLine_L1NL2L3xL4 – fixed pinout.

Diode_Zener_AKL symbol library:
- BZX79 series – updated datasheet links.
- MMSZ5221 series – updated datasheet links.
- MMBZxxxBS series – added additional separated symbols.
- All specific Zener diode symbols are now derived from their respective generic symbols.

Optocoupler_AKL symbol library:
- VOM617A and VOM618A series – fixed footprints.

Optocoupler_Gate_Driver_AKL symbol library:
- VOL3120 – fixed pinout.

Optocoupler_Logic_AKL symbol library:
- VO0630T, VO0631T and VO661T – added additional separated symbols.

Optocoupler_Triac_AKL symbol library:
- 5-pin Phototriacs no longer generate missing pin errors while updating PCB from schematic.

Transistor_MOSFET_AKL symbol library:
- Dual Gate MOSFETs now have the correct mode indicated on the symbol graphics (depletion instead of enhancement)

Transistor_BJT_AKL symbol library:
- BC212, BC213 and BC214 – fixed parent symbol.

Transistor_BJT_Darlington_AKL symbol library:
- MJ3000/3001 and MJ2500/2501 – fixed parent symbol.

Transistor_BJT_Pre-Biased symbol library:
- MUN211x series, MUN213x series, MUN221x series, MUN223x series, MUN511x series, MUN531x series, MUN521x series, MUN523x series – fixed symbol names.

Diode_AKL and Diode_AKL_Double footprint libraries:
- D_SOD-57_P12,70mm_Horizontal_Zener renamed to D_SOD-57_P12.70mm_Horizontal_Zener ( , replaced with . ) because the old name was not consistent with the naming convention. 

Package_TO_SOT_THT_AKL and Package_TO_SOT_THT_AKL_Double footprint libraries:
- TO-18-2_Zener footprint now has a reversed symbol on the silkscreen layer to match the BZP630 Zener diode series.

Package_TO_SOT_SMD_AKL footprint libray:
- SOT-563 now has narrower pads and larger pad-to-pad clearance

## Version 3.0

NEW SYMBOLS:

- Amplifier_Operational_AKL - Over 4250 operational amplifiers and OTAs with assigned footprints and datasheet links.
- Amplifier_Instrumentation_AKL - 245 Instrumentation amplifiers (IN-AMP) with assigned footprints and datasheet links.
- Amplifier_Difference_AKL - 98 Difference amplifiers (differential input, single-ended output) with assigned footprints and datasheet links.
- Amplifier_Differential_AKL - 50 Fully Differential Drivers and Amplifiers (differential input, differential output) with assigned footprints and datasheet links.
- Amplifier_Programmable_AKL - 66 Programmable Gain Amplifiers (PGA) or Selectable Gain Amplifiers (SGA) with assigned footprints and datasheet links.
- Amplifier_Isolation_AKL - 37 Isolated Amplifiers with assigned footprints and datasheet links.
- Analog_Comparator_AKL - 800 Analog Comparators with assigned footprints and datasheet links.

NEW FOOTPRINTS:
Nearly all SMD footprints have been revamped:
- All pads are rounded rectangles with either 25% or 0.25mm corner radius (wichever is smaller).
- Updated FAB Layer for better assembly drawings.
- Silkscreen outline snaps to 0.1mm (or 0.05mm for small footprints) outside the courtyard.

- Package SIP_AKL - New footprint library containing both new and modified KiCad Single-in-Line Packages.

- Package_DFN_QFN_AKL:
Added DFN-8-1EP_3x3mm_P0.5mm_EP1.2x2mm
Added Texas_RSV_UQFN16_1.8x2.6mm_P0.4mm
Added DFN-6_1.3x1.6_P0.4mm
Added QFN-16_3x3mm_P0.5mm
Added Diodes_UDFN-6_1.4x1.0mm_P0.5mm
Added Texas_X2QFN-8_1.5x1.5mm

- Package_SO_AKL:
Added TSSOP-14-1EP_4.4x5mm_P0.65mm_EP2.31x2.46mm
Added TSSOP-20-1EP_4.4x6.5mm_P0.65mm_EP2.4x3.4mm
Added SSOP-8_4.4x3.5mm_P0.65mm
Added SO-8_5x5mm_P1.27mm

- Package_SON_AKL:
Added Texas_X2SON-6_1x1mm_P0.35mm

- Capacitor_THT_AKL (Capacitor_THT_AKL_Double):
Added C_Rect_L15mm_W15mm_P10x10mm
Added C_Rect_L17mm_W8.5mm_P12.50mm
Added C_Rect_L36.5mm_W15mm_P32.50mm

- Resistor_THT_AKL:
Added R_Array_SIP4_BigPads
Added R_Array_SIP5_BigPads
Added R_Array_SIP6_BigPads
Added R_Array_SIP7_BigPads
Added R_Array_SIP8_BigPads
Added R_Array_SIP9_BigPads
Added R_Array_SIP10_BigPads
Added R_Array_SIP11_BigPads
Added R_Array_SIP12_BigPads
Added R_Array_SIP13_BigPads
Added R_Array_SIP14_BigPads


## Version 2.1
Footprint libraries:
- Footprints now load default KiCad's 3D models when available.
- No-Connect Pads will now have empty net name instead of '~'.
- Most SMD trimmers have new directional marks with rotor being connected to pad 2 (Usually connected to a low impedance net).
- All THT trimmers now have proper directional marks with rotor being connected to pin 2.
- SIP Resistor networks now have more pronounced pin 1 marks.

## Version 2.0 (Symbol Library Update)
NEW SYMBOL LIBRARIES: 
- Diode_AKL – SMD and THT diodes with assigned footprints and data sheet links.
- Diode_Schottky_AKL – SMD and THT Si and SiC Schottky diodes with assigned footprints and data sheet links.
- Diode_Capacitance_AKL – SMD and THT variable capacitance diodes with assigned footprints and data sheet links.
- Diode_Zener_AKL – SMD and THT Zener diodes with assigned footprints and data sheet links.
- Diode_TVS_AKL –TVS and ESD protection diodes and arrays with assigned footprints and data sheet links.
- Diode_Bridge_AKL – single and three-phase bridge rectifiers with assigned footprints and data sheet links.
- Diode_Current_Limiting – Current limiting diodes (CLD/CRD) with assigned footprints and data sheet links.
- Diac_AKL – Diacs (AC Trigger diodes) with assigned footprints and data sheet links.
- Transistor_BJT_AKL – bipolar transistors and arrays with assigned footprints and data sheet links.
- Transistor_BJT_Darlington – Darlington transistors with assigned footprints and data sheet links.
- Transistor_BJT_Pre-Biased – Pre-biased (BRT) bipolar transistors and arrays with assigned footprints and data sheet links.
- Transistor_MOSFET_AKL – MOSFETs and arrays with assigned footprints and data sheet links.
- Transistor_JFET_AKL – JFETs and matched pairs with assigned footprints and data sheet links.
- Transistor_IGBT_AKL – IGBTs (Insulated Gate Bipolar Transistors) with assigned footprints and data sheet links.
- Thyristor_AKL – SMD and THT thyristors with assigned footprints and data sheet links.
- Triac_AKL – SMD and THT Triacs with assigned footprints and data sheet links.
- Optocoupler_AKL – transistor-output optocouplers with assigned footprints and data sheet links.
- Optocoupler_Gate_Driver_AKL – optically isolated MOSFET/IGBT gate drivers with assigned footprints and data sheet links.
- Optocoupler_Logic_AKL – logic-output optocouplers with assigned footprints and data sheet links.
- Optocoupler_Triac_AKL – phototriacs with assigned footprints and data sheet links.
- Optocoupler_Misc_AKL – miscellaneous devices (isolated error amplifiers, linear optocouplers, photovoltaic-output optocouplers) with assigned footprints and data sheet links.
- Device_AKL – New generic ferrite bead and fuse symbols.

NEW FOOTPRINTS:
- Diode_SMD_AKL (Diode_SMD_AKL_Handsoldering):
Added SOD-882 Package and a TVS variant with no polarity marks
Added SMP (DO220AA) Package
Added MicroSMP (DO219AD) Package
Added SMAFL (SMA – Flat Lead) Package
Added SMBFL (SMB – Flat Lead) Package
Added MBF Diode Bridge Package

- Diode_THT_AKL:
5W Series – Added Zener variants, compatibility with CASE-017AA is now highlighted in the name.
DO-35 Series – Added Diac variants.
Diode_Bridge_32.0x5.6x17.0mm_P10.0mm_P7.5mm – Corrected silkscreen labels and reversed pin order to be compatible with the new symbols.
Diode_Bridge_19.0x3.5x10.0mm_P5.0mm – Corrected silkscreen labels and reversed pin order to be compatible with the new symbols. Added a new pinout variant.
Added Diode_Bridge_28.6x28.6x7.3mm_P5.08mm_Vertical – Rectifier bridge package, vertical mount variant.
Added Diode_Bridge_3F_35x25x5.5mm_P7.5mm – Three phase rectifier bridge.
Added Diode_Bridge_3F_40x21.5x5.4mm_P7.5mm – Three phase rectifier bridge.

- Package_DFN_QFN_AKL: 
Added DFN-4_2x2mm_P0.45mm_EP1x1.35mm
Added DFN-6_1.6x1.6mm_P0.5mm
Added DFN-6-1EP_1.6x1.6mm_P0.5mm_EP0.6x1mm
Added DFN-6-2EP_2x2mm_P0.65mm_EP1.15x0.95mm_EP0.8x0.48mm
Added DFN-8-1EP_3x3mm_P0.5mm_EP1.55x1.85mm
Added DFN-8-1EP_3x3mm_P0.5mm_EP1.7x1.7mm
Added DFN-8-1EP_3x3mm_P0.5mmEP1.45x2.4mm
Added DFN-10-1EP-2.6x2.6mm_P0.5_EP1.26x2.35mm
Added DFN-10-1EP-2x2mm_P0.4mm_EP0.9x1.5mm
Added Linear_DJC_DFN22_6x3mm
Added OnSemi_WQFN-10_2.6x2.6mm_P0.5mm

- Package_DIP_AKL:
Added DIP-4-8_W7.62mm – Used by some optocouplers
Added DIP-4-8_W7.62mm_LongPads
Modified DIP-8-16_W7.62mm – Overall package length increased to 21.34mm
Modified DIP-8-16_W7.62mm_LongPads – Overall package length increased to 21.34mm
Modified DIP-8-16_W7.62mm_Socket – Overall package length increased to 21.34mm
Modified DIP-8-16_W7.62mm_Socket_LongPads – Overall package length increased to 21.34mm
Modified DIP-14_W7.62mm – Overall package length increased to 20.32mm
Modified DIP-14_W7.62mm_LongPads – Overall package length increased to 20.32mm
Modified DIP-14_W7.62mm_ Socket – Overall package length increased to 20.32mm
Modified DIP-14_W7.62mm_Socket_Longpads – Overall package length increased to 20.32mm
Modified DIP-14_W10.16mm – Overall package length increased to 20.32mm
Modified DIP-14_W10.16mm_LongPads – Overall package length increased to 20.32mm
Modified DIP-18_W7.62mm - Overall package length increased to 24.13mm
Modified DIP-18_W7.62mm_LongPads - Overall package length increased to 24.13mm
Modified DIP-18_W7.62mm_Socket - Overall package length increased to 24.13mm
Modified DIP-18_W7.62mm_Socket_LongPads - Overall package length increased to 24.13mm
Modified DIP-20_W7.62mm - Overall package length increased to 27.18mm
Modified DIP-20_W7.62mm_LongPads - Overall package length increased to 27.18mm
Modified DIP-20_W7.62mm_Socket - Overall package length increased to 27.18mm
Modified DIP-20_W7.62mm_Socket_LongPads - Overall package length increased to 27.18mm
Modified DIP-24_W7.62mm - Overall package length increased to 32.51mm
Modified DIP-24_W7.62mm_LongPads - Overall package length increased to 32.51mm
Modified DIP-24_W7.62mm_Socket - Overall package length increased to 32.51mm
Modified DIP-24_W7.62mm_Socket_LongPads - Overall package length increased to 32.51mm
Modified DIP-24_W10.16mm - Overall package length increased to 32.51mm
Modified DIP-24_W10.16mm_LongPads - Overall package length increased to 32.51mm
Modified DIP-24_W10.16mm_Socket - Overall package length increased to 32.51mm
Modified DIP-24_W10.16mm_Socket_LongPads - Overall package length increased to 32.51mm
Modified DIP-24_W15.24mm - Overall package length increased to 32.51mm
Modified DIP-24_W15.24mm_LongPads - Overall package length increased to 32.51mm
Modified DIP-24_W15.24mm_Socket - Overall package length increased to 32.51mm
Modified DIP-24_W15.24mm_Socket_LongPads - Overall package length increased to 32.51mm
Modified DIP-28_W7.62mm - Overall package length increased to 36.83mm
Modified DIP-28_W7.62mm_LongPads - Overall package length increased to 36.83mm
Modified DIP-28_W7.62mm_Socket - Overall package length increased to 36.83mm
Modified DIP-28_W7.62mm_Socket_LongPads - Overall package length increased to 36.83mm
Modified DIP-28_W15.24mm - Overall package length increased to 36.83mm
Modified DIP-28_W15.24mm_LongPads - Overall package length increased to 36.83mm
Modified DIP-28_W15.24mm_Socket - Overall package length increased to 36.83mm
Modified DIP-28_W15.24mm_Socket_LongPads - Overall package length increased to 36.83mm
Modified DIP-32_W15.24mm - Overall package length increased to 41.91mm
Modified DIP-32_W15.24mm_LongPads - Overall package length increased to 41.91mm
Modified DIP-32_W15.24mm_Socket - Overall package length increased to 41.91mm
Modified DIP-32_W15.24mm_Socket_LongPads - Overall package length increased to 41.91mm
Modified DIP-40_W15.24mm - Overall package length increased to 53.09mm
Modified DIP-40_W15.24mm_LongPads - Overall package length increased to 53.09mm
Modified DIP-40_W15.24mm_Socket - Overall package length increased to 53.09mm
Modified DIP-40_W15.24mm_Socket_LongPads - Overall package length increased to 53.09mm
Modified DIP-40_W25.4mm - Overall package length increased to 53.09mm
Modified DIP-40_W25.4mm_LongPads - Overall package length increased to 53.09mm
Modified DIP-40_W25.4mm_Socket - Overall package length increased to 53.09mm
Modified DIP-40_W25.4mm_Socket_LongPads - Overall package length increased to 53.09mm
Modified DIP-48_W15.24mm - Overall package length increased to 62.23mm
Modified DIP-48_W15.24mm_LongPads - Overall package length increased to 62.23mm
Modified DIP-48_W15.24mm_Socket - Overall package length increased to 62.23mm
Modified DIP-48_W15.24mm_Socket_LongPads - Overall package length increased to 62.23mm

- Package_SON_AKL:
Added Infineon_PG-TDSON-8
Added Infineon_PG-TDSON-8_FL
Added Infineon_PG-TDSON-8_Dual
Added Infineon_PG-TSDSON-8
Added Infineon_PG-TSDSON-8_FL
Added Texas_S-PWSON-N8_EP2.2x3mm
Added Texas_S-PWSON-N8_EP2.2x3mm_ThermalVias
Added WSON-8-1EP_3x3mm_P0.5mm_EP1.45x2.4mm

- Package_SO_AKL:
Added SO-5_4.4x4.1mm_P1.27mm
Added SO-6_6.8x4.6mm_P1.27mm
Added SO-6_6.8x4.6mm_P1.27mm_Wide
Added SO-6_7.5x3.84mm_P1.27mm
Added SO-6_7.5x3.84mm_P1.27mm_Wide
Added SO-8_4.4x5mm_P1.27mm
Added SOIC-28W-8_7.5x17.9mm_P1.27mm – High isolation SMD package for ISO122U/JU

- Package_TO_SOT_THT_AKL:
Added TO-3-8_Isolated Package
Added TO-262-2 Package
Added TO-66 Package
Added more pin indicator variants

- Optocoupler_AKL – new footprint library containing non-standard optocoupler footprints to match the new Optocoupler_xxx_AKL symbol libraries:
Added Vishay_CNY64
Added Vishay_CNY64ST (SMD variant of CNY64)
Added Vishay_CNY65
Added Vishay_CNY65ST (SMD variant of CNY65)
Added Vishay_CNY66

- Package_CSP_AKL – new modified version of the Package_CSP Library from standard KiCAD with modified silkscreen layer and new original footprints:
Added LFCSP-VD-8_1EP_3x3mm_P0.5mm_EP1.89x1.6mm
Added LFCSP-VQ-16_4x4mm_P0.65mm
Added WLCSP-5_1.33x0.9mm_P0.5mm
Added WLCSP-8_1.825x1.48mm_P0.5mm

- Ferrite_THT_AKL – new footprint library containing most common THT ferrite beads and filters with the new ferrite symbol printed on the silkscreen.

- Ferrite_SMD_AKL – new footprint library containing most common SMD ferrite beads and filters.

- Ferrite_SMD_Handsoldering_AKL – variant of the Ferrite_SMD_AKL library with the new ferrite symbol printed on the silkscreen under the parts.

- Fuse_AKL – new modified KiCAD Fuse footprint library with fuse symbol indicated on all THT parts.

- Fuse_AKL_Double – variant of the Fuse_AKL  library with silkscreen on both sides of the parts.

- Fuse_Handsoldering_AKL – variant of the Fuse_AKL library containing SMD parts with fuse symbols indicated on the silkscreen under the part intended for hand soldering projects.

- Capacitor_THT_AKL_Double – new variant of the Capacitor_THT_AKL library with silkscreen on both sides of the PCB.

- Diode_THT_AKL_Double – new variant of the Diode_THT_AKL library with silkscreen on both sides of the PCB.

- Inductor_AKL_Double – variant of the Inductor_AKL  library with silkscreen on both sides of the parts.

- Jumper_AKL – new footprint library with wire jumpers in multiples of 0.1 inch pin pitches. Useful for single-sided routing.

- Jumper_AKL_Double – variant of the Jumper_AKL library with silkscreen on both sides of the parts.

- Package_TO_SOT_THT_AKL_Double – variant of the TO_SOT_THT_AKL library with silkscreen on both sides of the parts.

- Resistor_AKL_Double – variant of the Resistor_AKL  library with silkscreen on both sides of the parts.


## Version 1.1
- SMD Diode, Capacitor and Inductor footprint libraries have been split into standard and hand soldering variants.
Capacitor_SMD_Handsoldering_AKL
Capacitor_Tantalum_SMD_Handsoldering_AKL
Diode_SMD_Handsoldering_AKL
Inductor_SMD_Handsoldering_AKL
- Standard libraries are suitable for machine soldering and have no silkscreen under the parts.
- Hand soldering libraries have silkscreen under the part to improve readability of the PCB and reduce component placement errors.
- Footprints (included in those libraries) with bigger pads that used to be called the ‘HandSoldering’ variants have been renamed to ‘BigPads’ to reduce confusion.
- Footprint names between standard and hand soldering libraries are consistent. You can easily swap the footprint by using ‘change footprint’ option and renaming the library in PCBNew.
- Minor improvements to SMD inductor library.
- Some SMD TVS diode footprints had unnecessary polarity marks.
- Crystal and SMD resistor libraries have no silkscreen under the SMD parts.

## Version 1.0
- Modified KiCad Libraries:
Capacitor_SMD_AKL
Capacitor_Tantalum_AKL
Capacitor_THT_AKL
Crystal_AKL
Diode_SMD_AKL
Diode_THT_AKL
Inductor_SMD_AKL
Inductor_THT_AKL
Package_DFN_QFN_AKL
Package_DIP_AKL
Package_LCC_AKL
Package_QFP_AKL
Package_SO_AKL
Package_SON_AKL
Package_TO_SOT_SMD_AKL
Package_TO_SOT_THT_AKL
Resistor_SMD_AKL
Resistor_THT_AKL
These libraries inherit KiCad’s pad layout and footprint names so you can easily swap footprints using ‘change footprint’ option and renaming the library in PCBNew.
Some new footprints have been added, see the showcase folder for details.
- New footprint library:
Jumper_AKL
Adds THT jumpers with multiple pin pitch and two wire diameters variants. Helpful during single-sided PCB layout.




