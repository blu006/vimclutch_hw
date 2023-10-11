# vimclutch_hw
vimclutch hardware

## Description
This is a vim clutch implementation. This project uses the Arduino ProMicro, three tactile switches, and two LEDs.  The top two tactile switches are for switching modes.  The LEDs to show which layer the clutch is in.  The foot pedal is soldered onto the board.

## References
[Link to QMK keyboard](https://github.com/qmk/qmk_firmware/tree/master/keyboards/blu/vimclutch)

## BOM
The following is a bill of materials for this build.

Note that the selected vendors provide a suggestion of the component and the maker may choose to substitute with equivalent components.  Cheaper, less reputable vendors often provide parts that are more than acceptable for use in this non-critical project.

### 3D
The components below comprise the mechanical components of the vim clutch.
#### Prints
All 3d printable components are designed to be printable without supports.  The "flat bottom" may need to be aligned to print on your build plate in your favorite 3d printing slicer.
| Component | Material | Special Instructions |
| -- | -- | -- |
|`Top Housing.stl`|Clear-ish|Optionally print using the transparent parts printing techniques discussed [in this article](https://www.cnckitchen.com/blog/transparent-fdm-3d-prints-are-clearly-stronger)|
|`Bottom Housing.stl`|Your choice of color|N/A|
|`Button Left.stl`|Your choice of color|May exclude if you are using tactile switches that are long enough|
#### Vitamins
| Component | Comments | Selected Vendors |
| -- | -- | -- | 
|M3 x 12mm Socket Head Screw |It may be possible to use only two instead of four.|[McMaster Carr 91290A117](https://www.mcmaster.com/91290A117/) <br /> [Bolt Depot 13637](https://www.boltdepot.com/Product-Details.aspx?product=13637)|
|M3 Nut|"" |[McMaster Carr 98676A100](https://www.mcmaster.com/98676A100/)|
|Cable Tie 2.5mm|For holding the foot pedal cable onto the PCB| [Digikey 2162-AL-04-18-9-C-ND](https://www.digikey.com/en/products/detail/advanced-cable-ties-inc/AL-04-18-9-C/10380608)|
|Foot Pedal|Any SPDT or SPST foot pedal should work. |[Adafruit 423](https://www.adafruit.com/product/423) <br /> [Digi-Key 1528-1137-ND](https://www.digikey.com/en/products/detail/adafruit-industries-llc/423/5353597) |
|Ferrite Bead| May be optional. See [interference](README.md#interference)|[Digi-Key 1934-1375-ND](https://www.digikey.com/en/products/detail/fair-rite-products-corp/0431167281/8593997) <br /> [Digi-Key 240-2077-ND](https://www.digikey.com/en/products/detail/laird-signal-integrity-products/28A2029-0A2/242805) <br /> [Digi-Key 240-2076-ND](https://www.digikey.com/en/products/detail/laird-signal-integrity-products/28A2029-0A0/242804)|
|Micro USB Cable|Should have this already|Select a preferred vendor.  Local convenience stores or general stores will likely carry this part.|

### PCB
Since the PCB was originally designed to be made on a makerspace CNC with readily-available parts, the components necessary are generic and substitutable.  These components can also be seen on the PCB BOM included in the PCB directory.

The PCB is fabbable using any online PCB fab.  The designed thickness is **1.6mm** and your mechanical components will fit best at this board thickness.
| Component | Value | Quantity | Description | Selected Vendors |
| -- | -- | -- | -- | -- |
|D\*|RED|2|Wide Angle LED.  Note that this LED is height constrained.  It's possible to sand down a normal 5mm LED to fit in this position.|[Digi-Key 754-2141-ND](https://www.digikey.com/en/products/detail/kingbright/WP9294SECK-J3/7318908)|
|R\*|2.7k|2|LED Current Limiting Resistor|[Digi-Key CR0805-FX-2701ELFCT-ND](https://www.digikey.com/en/products/detail/bourns-inc/CR0805-FX-2701ELF/3784809)|
|SW1|H4.3mm|1|Reset switch.  4.3mm actuator length to keep it recessed into the housing.  A longer switch is also acceptable if it's what you have.  Tested successfully with 5mm.|[Digi-Key 2223-TS02-66-43-BK-260-SCR-D-ND](https://www.digikey.com/en/products/detail/cui-devices/TS02-66-43-BK-260-SCR-D/15634273)|
|SW(2,3)|H5mm or H10mm|2|Layer toggle switch.  Pair with the `Button Left.stl` if 5mm high switches are used.  Other lengths will likely work fine but have not been tested. |[Digi-Key TS02-66-100-BK-260-SCR-D](https://www.digikey.com/en/products/detail/cui-devices/TS02-66-100-BK-260-SCR-D/15634307)|
|U1|ProMicro|1|Arduino Pro Micro 5v/16Mhz.  Possible to purchase from other, less reputable sources.  Breakaway header pins may be needed if the promicro does not already come with them.|[Digi-Key 1568-1060-ND](https://www.digikey.com/en/products/detail/sparkfun-electronics/DEV-12640/5140825)|

## Assembly
1. Assemble the PCB and the foot pedal
2. Assemble the 3d printed enclosure
3. Plug in, program
4. Enjoy

### Interference
Board revision A and its relatives had problems with interference.

Board revision B does not because it uses direct pull-down keys.

## Tools
* KiCAD 6.0
* Fusion 360
* Soldering Iron
* Hex Wrench
* (Optional) CNC

## Next Steps
Consider the possibility of using a microcontroller with a USB-C port instead.

## Project Expectations
This project is provided as a form of weblogging (see: blogging).  The designs provided are not guaranteed for mercantability or quality beyond the occasional one-off production from enthusiasts.

### Tolerances
The tolerances from the SLA files and f360 should be sized for reasonably accurate FDM 3d printers and nothing more.  Do not expect them to be right for MSLA, injection molding, or subtractive manufacturing.

### Expected Support for the Project
Feel free to start a conversation in the Issues on GitHub or on any other social media sites.

The author may be willing to adjust some tolerances if the files are not editable enough for potential users.

## History
Rev B was released which changed all keys to be directly driven by the keyboard controller.

## Contributing
Please leave feedback in the Issues tab on the ease of assembly and similar items.  Minor updates on "I had to file this part in this way" could potentially improve the assembly for other people.

## Acknowledgements
The author's local makerspace provided the 3d printers and CNC to make this project possible.  Thank you [MAG Laboratory!](https://www.maglaboratory.org/)
