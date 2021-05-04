# Alternate-KiCad-Library

Alternate KiCad Library

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

About:
The aim of this library is to provide a different way of utilizing the silkscreen layer to maximize the
amount of information per component. This library consists mostly of modified footprints from KiCad
library and some brand new footprints that match the new style and philosophy.
• Different types of components can now be distinguished more easily (e.g. axial capacitors and
resistors).
• Directional components have more pronounced polarity (diodes, tantalum capacitors etc.).
• Integrated circuits have marks that make counting pins easier (for example when you need to
test a specific pin on a large IC during troubleshooting).
• Different visual style – SMD parts have a rectangular outline and a dot marking pin 1.
Parts of this library deliberately violate the original KiCad Library Convention by including silkscreen
drawings under some of the components. Additionaly some SMD footprints might take more physical
space that original KiCad ones.
This should make the PCB easier to ‘read’ and reduce errors during hand-soldering and
troubleshooting at a cost of lower layout density.

Compatibility:
Alternate KiCad Library 1.0 is known to work with KiCad 5.1.9 but should be cross-compatible with all
KiCad 5 versions.
Footprint library should be forward-compatible with the upcoming KiCad 6 (tested on nightly build
r22263).

Disclaimer:
Alternate KiCad Library as a modification of KiCad Libraries is a work of a single person and is not
guaranteed to be correct.
If you find any errors please send me an e-mail with the details (footprint name, link to datasheet,
screenshots showing the error) here: dawid_cislo@o2.pl
It might take months between updates, because I’m making this project in my spare time, but more
features are coming.

Changelog:
Version 1.1
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

Version 1.0
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




