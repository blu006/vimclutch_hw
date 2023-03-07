# vimclutch_hw
vimclutch hardware

## Description
This is a VIM clutch which uses the Arduino ProMicro and a few tactile switches.  The top two tactile switches are for switching modes.  There are LEDs to show which state the board is in.  There is a solder-on connection for the foot pedal.

## BOM
The following is a bill of materials for this build.

Note that the selected vendors provide a suggestion of the component and the maker may choose to substitute with equivalent components.
### 3D
#### Prints
All 3d printable components are designed to be printable without supports.  The "flat bottom" may need to be aligned to print on your build plate in your favorite 3d printing slicer.
| Component | Material | Special Instructions |
| -- | -- | -- |
|Top Housing.stl|Clear-ish|Print using the transparent parts printing techniques discussed [in this article](https://www.cnckitchen.com/blog/transparent-fdm-3d-prints-are-clearly-stronger)|
|Bottom Housing.stl|Your choice of color|N/A|
#### Vitamins
| Component | Comments | Selected Vendors |
| -- | -- |
|M3 x 12mm Socket Head Screw |[McMaster Carr 91290A117](https://www.mcmaster.com/91290A117/) <br /> [Bolt Depot 13637](https://www.boltdepot.com/Product-Details.aspx?product=13637)|
|M3 Nut| |TODO|
|Cable Tie 2.5mm| | |
|Foot Pedal| | |
|Ferrite Bead| May be optional? | |

### PCB
| Component | PCB Refs | Quantity | Description | Selected Vendors |
| -- | -- | -- | -- | -- |
|TODO|

## Assembly
1. Assemble the PCB and the foot pedal
2. Assemble the 3d printed enclosure
3. Plug in, program
4. Enjoy

## Tools
* KiCAD 6.0
* Fusion 360

## Next Steps
Consider the possibility of using a microcontroller with a USB-C port instead.

Update to KiCAD 7.0

## Project Expectations
This project is provided as a form of weblogging (see: blogging).  The designs provided are not guaranteed for mercantability or quality beyond the occasional one-off production from enthusiasts.

### Tolerances
The tolerances from the SLA files and f360 should be sized for reasonably accurate FDM 3d printers and nothing more.  Do not expect them to be right for MSLA, injection molding, or subtractive manufacturing.

### Expected Support for the Project
Feel free to start a conversation in the Issues on GitHub or on any other social media sites.

The author may be willing to adjust some tolerances if the files are not editable enough for potential users.

## Contributing
Please leave feedback in the Issues tab on the ease of assembly and similar items.  Minor updates on "I had to file this part in this way" could potentially improve the assembly for other people.
