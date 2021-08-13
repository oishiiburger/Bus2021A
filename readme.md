# Bus 2021A

This is a quick n' dirty bus design for a hobbyist computer system based around the [WD65C02](https://en.wikipedia.org/wiki/WDC_65C02). It is not meant to be fancy, but it should be functional. Features of the 65C02 which are unique to the WDC version are not exposed to the bus (i.e. VPB Vector-Pull Output, MLB Memory-Lock Output, and BE Bus Enable input). 4 pins (USER1 through USER4) are provided for peripheral expansion / experimentation / whatever.

The purpose of the bus is to allow for the use of a custom backplane so that several small boards to be easily connected.

The bus layout is as follows:

```
PIN     LABEL   DEF
1       A15     Address lines
2       A14     |
3       A13     |
4       A12     |
5       A11     |
6       A10     |
7       A9      |
8       A8      |
9       A7      |
10      A6      |
11      A5      |
12      A4      |
13      A3      |
14      A2      |
15      A1      |
16      A0      |
17      NMIB    Non-maskable interrupt
18      IRQB    Interrupt request
19      SOB     Set Overflow
20      GND     Vss
21      5V      Vcc
22      RDY     Ready
23      RESB    Reset
24      RWB     Read/Write
25      CLK     Clock (Phase 2 input)
26      Φ1O     Phase 1 out
27      Φ2O     Phase 2 out
28      SYNC    Synchronize
29      D0      Data lines
30      D1      |
31      D2      |
32      D3      |
33      D4      |
34      D5      |
35      D6      |
36      D7      |
37      USER1   User space
38      USER2   |
39      USER3   |
40      USER4   |
```