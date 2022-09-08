***	INTRODUCTION

Pasting provided library table fragments into your own library table can be a fast an relatively easy way to customize the Alternate KiCad Library.

Description_Footprints.txt
Description_Symbols.txt

These files contain library table entries for AKL footprints and symbols respectively, linking to the locations as per standard installation via KiCad's Plugin and Content Manager. (${KICAD6_3RD_PARTY}/symbols/com_github_dawidcislo_alternate-kicad-library/...)
"Description" signifies that these entries have additional descriptions added to the library table (the description field for any new libraries is blank by default).

Prefix_Footprints.txt
Prefix_Symbols.txt

These table entries change the nickname of the libraries so that the "AKL" part is a prefix, not a suffix. (Example: AKL_Diode instead of Diode_AKL)
This naming results in AKL libraries being grouped in one place when browsing libraries, since libraries are sorted alphabetically:

...		<- standard KiCad libraries starting with numbers
AKL_Lib1
AKL_Lib2
AKL_Lib3
...		<- standard KiCad libraries starting with B
...


***	MODIFYING LIBRARY TABLE FILES

Library files are located (on windows machines) in this directory:
C:\Users\<username>\AppData\Roaming\kicad\6.0

To access the appdata folder you need to either:
- Type '%appdata%' in windows search.
- Enable “Show Hidden Files” in windows explorer options.

Library table files have no file extension but can be edited with any text editor (Notepad):
fp-lib-table: Footprint library table
sym-lib-table: Symbol library table

Typical library table entry:
(lib (name "Filter")(type "KiCad")
(uri "${KICAD6_FOOTPRINT_DIR}/Filter.pretty")(options "")
(descr "Filter footprints"))

name “<library name>” is the Nickname field.
uri “<library path>” is the path to the library file.
descr “<description>” is the description field.

You can paste multiple entries into the library table directly to edit multiple fields at once.
Make sure to delete any duplicate entries during pasting (Previously installed AKL libraries).

Footprint library table contents:

(fp_lib_table
 Entry 1
 Entry 2
 …
 Entry x
 <- Paste Here
)