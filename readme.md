# Bus 2021A

This is a quick n' dirty bus design for a hobbyist computer system based around the [WD65C02](https://en.wikipedia.org/wiki/WDC_65C02). It is not meant to be fancy, but it should be functional. Features of the 65C02 which are unique to the WDC version are not exposed to the bus (i.e. VPB Vector-Pull Output, MLB Memory-Lock Output, and BE Bus Enable input). 4 pins (USER1 through USER4) are provided for peripheral expansion / experimentation / whatever.

The purpose of the bus is to allow for the use of a custom backplane so that several small boards to be easily connected. The backplane design is below, and protoboards intended for this bus are to come.

The bus mapping is [here](./Bus2021A.txt), but also printed on the backplane board.

## Bus 2021A backplane - 5 slot

![Bus 2021A Rev0 PCB](./images/Bus2021A_5Slot_PCB.png)

All kicad files, gerber files, etc. are [in the repo](./Bus2021A_5Slot). The schematic is below.

The backplane features spots for 5 female pin headers, a DJ jack for 5v power and a power jumper (which can be broken out to a switch), a power LED, and a reset switch which is tied into the bus. 

A future revision might include blinkenlights on the backplane, but for now there will be space for those to be easily put on one of the protoboards.

![Bus 2021A backplane - 5 slot schematic](./images/Bus2021A_Backplane_Rev0_Schematic.png)