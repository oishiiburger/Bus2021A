# Bus 2021A

This is a quick n' dirty bus design for a hobbyist computer system based around the [WD65C02](https://en.wikipedia.org/wiki/WDC_65C02). It is not meant to be fancy, but it should be functional. Some features of the 65C02 which are unique to the WDC version are not exposed to the bus (e.g. VPB Vector-Pull Output, MLB Memory-Lock Output, and BE Bus Enable input). Additionally, the SOB Set-OverFlow flag is unconnected, as is the Φ1 clock.

The purpose of the bus is to allow for the use of a custom backplane to allow for several small boards to be easily connected.