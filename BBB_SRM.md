![](docs/media/image1.jpg){width="6.236805555555556in"
height="4.170138888888889in"}

> **BeagleBone Black**
>
> **System Reference Manual **

**Revision C.1**

**May 22, 2014**

> **Author: Gerald Coley *gerald@beagleboard.org***

**Contributing Editor: Robert P J Day**

**THIS DOCUMENT **

**This work is licensed under the Creative Commons Attribution-Share
Alike 3.0 Unported License. To view a copy of this license, visit
[http://creativecommons.org/licenses/bysa/3.0/](http://creativecommons.org/licenses/by-sa/3.0/)**
**or send a letter to Creative Commons, 171 Second Street, Suite 300,
San Francisco, California, 94105, USA. **

**All derivative works are to be attributed to Gerald Coley of
BeagleBoard.org. **

**For more information, see
[http://creativecommons.org/license/resultsone?license\_code=by-sa](http://creativecommons.org/license/results-one?license_code=by-sa)**

**Send all comments and errors concerning this document to the author at
*gerald@beagleboard.org* **

**For other questions you may contact Gerald at: **

**Gerald Coley **

**Texas Instruments **

> **12500 TI Blvd. Dallas, Tx 75243 *g-coley1@ti.com* **

**All information in this document is subject to change without notice.
**

**For an up to date version of this document refer to: **

[***http://circuitco.com/support/index.php?title=BeagleBoneBlack\#LATEST\_PRODUC***](http://circuitco.com/support/index.php?title=BeagleBoneBlack#LATEST_PRODUCTION_FILES_.28A5A.29)

[***TION\_FILES\_.28A5A.29***
](http://circuitco.com/support/index.php?title=BeagleBoneBlack#LATEST_PRODUCTION_FILES_.28A5A.29)

**BEAGLEBONE DESIGN **

These design materials referred to in this document are **\*NOT
SUPPORTED\*** and **DO NOT** constitute a reference design. Only
“community” support is allowed via resources at
[*BeagleBoard.org/discuss.*](http://beagleboard.org/discuss)

THERE IS NO WARRANTY FOR THE DESIGN MATERIALS, TO THE EXTENT PERMITTED
BY APPLICABLE LAW. EXCEPT WHEN OTHERWISE STATED IN WRITING THE COPYRIGHT
HOLDERS AND/OR OTHER PARTIES PROVIDE THE DESIGN MATERIALS “AS IS”
WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING,
BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND
FITNESS FOR A PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND
PERFORMANCE OF THE DESIGN MATERIALS IS WITH YOU. SHOULD THE DESIGN
MATERIALS PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY
SERVICING, REPAIR OR CORRECTION.

This board was designed as an evaluation and development tool. It was
not designed with any other application in mind. As such, the design
materials that are provided which include schematic, BOM, and PCB files,
may or may not be suitable for any other purposes. If used, the design
material becomes your responsibility as to whether or not it meets your
specific needs or your specific applications and may require changes to
meet your requirements.

> **BEAGLEBONE BLACK ADDITIONAL TERMS **
>
> BeagleBoard.org, Circuitco, LLC, and BeagleBoard.org (Supplier)
> provide the enclosed BeagleBone under the following conditions:
>
> The user assumes all responsibility and liability for proper and safe
> handling of the goods. Further, the user indemnifies Supplier from all
> claims arising from the handling or use of the goods.
>
> Should the BeagleBone not meet the specifications indicated in the
> System Reference Manual, the BeagleBone may be returned within 90 days
> from the date of delivery to the distributor of purchase for a full
> refund. THE FOREGOING LIMITED WARRANTY IS THE EXCLUSIVE WARRANTY MADE
> BY SELLER TO BUYER AND IS IN LIEU OF ALL OTHER WARRANTIES, EXPRESSED,
> IMPLIED, OR STATUTORY, INCLUDING ANY WARRANTY OF MERCHANTABILITY OR
> FITNESS FOR ANY PARTICULAR PURPOSE. EXCEPT TO THE EXTENT OF THE
> INDEMNITY SET FORTH ABOVE, NEITHER PARTY SHALL BE LIABLE TO THE OTHER
> FOR ANY INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES.
>
> Please read the System Reference Manual and, specifically, the
> Warnings and Restrictions notice in the Systems Reference Manual prior
> to handling the product. This notice contains important safety
> information about temperatures and voltages.
>
> No license is granted under any patent right or other intellectual
> property right of Supplier covering or relating to any machine,
> process, or combination in which such Supplier products or services
> might be or are used. The Supplier currently deals with a variety of
> customers for products, and therefore our arrangement with the user is
> not exclusive. The Supplier assume no liability for applications
> assistance, customer product design, software performance, or
> infringement of patents or services described herein.

##### **UNITED STATES FCC AND CANADA IC REGULATORY COMPLIANCE INFORMATION** 

> **The BeagleBone is annotated to comply with Part 15 of the FCC
> Rules**. Operation is subject to the following two conditions: (1)
> This device may not cause harmful interference, and (2) this device
> must accept any interference received, including interference that may
> cause undesired operation. Changes or modifications not expressly
> approved by the party responsible for compliance could void the user’s
> authority to operate the equipment.
>
> This Class A or B digital apparatus complies with Canadian ICES-003.
> Changes or modifications not expressly approved by the party
> responsible for compliance could void the user’s authority to operate
> the equipment. Cet appareil numérique de la classe A ou B est conforme
> à la norme NMB-003 du Canada. Les changements ou les modifications pas
> expressément approuvés par la partie responsible de la conformité ont
> pu vider l’autorité de l'utilisateur pour actionner l'équipement.

**BEAGLEBONE WARNINGS, RESTRICTIONS AND DISCLAIMERS**

> ***For Feasibility Evaluation Only, in Laboratory/Development
> Environments**. The* *BeagleBone Black is not a complete product. It
> is intended solely for use for preliminary* *feasibility evaluation in
> laboratory/development environments by technically qualified*
> *electronics experts who are familiar with the dangers and application
> risks associated with* *handling electrical mechanical components,
> systems and subsystems. It should not be* *used as all or part of a
> finished end product.*

**Your Sole Responsibility and Ris**k you acknowledge, represent, and
agree that:

1.  You have unique knowledge concerning Federal, State and local
    regulatory requirements (including but not limited to Food and Drug
    Administration regulations, if applicable) which relate to your
    products and which relate to your use (and/or that of your
    employees, affiliates, contractors or designees) of the BeagleBone
    for evaluation, testing and other purposes.

2.  You have full and exclusive responsibility to assure the safety and
    compliance of your products with all such laws and other applicable
    regulatory requirements, and also to assure the safety of any
    activities to be conducted by you and/or your employees, affiliates,
    contractors or designees, using the BeagleBone. Further, you are
    responsible to assure that any interfaces (electronic and/or
    mechanical) between the BeagleBone and any human body are designed
    with suitable isolation and means to safely limit accessible leakage
    currents to minimize the risk of electrical shock hazard.

3.  Since the BeagleBone is not a completed product, it may not meet all
    applicable regulatory and safety compliance standards which may
    normally be associated with similar items. You assume full
    responsibility to determine and/or assure compliance with any such
    standards and related certifications as may be applicable. You will
    employ reasonable safeguards to ensure that your use of the
    BeagleBone will not result in any property damage, injury or death,
    even if the BeagleBone should fail to perform as described or
    expected.

> ***Certain Instructions**. It is important to operate the BeagleBone
> Black within Supplier’s* *recommended specifications and environmental
> considerations per the user guidelines.* *Exceeding the specified
> BeagleBone ratings (including but not limited to input and output*
> *voltage, current, power, and environmental ranges) may cause property
> damage, personal* *injury or death. If there are questions concerning
> these ratings please contact the Supplier* *representative prior to
> connecting interface electronics including input power and intended*
> *loads. Any loads applied outside of the specified output range may
> result in unintended* *and/or inaccurate operation and/or possible
> permanent damage to the BeagleBone and/or* *interface electronics.
> Please consult the System Reference Manual prior to connecting any*
> *load to the BeagleBone output. If there is uncertainty as to the load
> specification, please* *contact the Supplier representative. During
> normal operation, some circuit components* *may have case temperatures
> greater than 60 C as long as the input and output are* *maintained at
> a normal ambient operating temperature. These components include but
> are* *not limited to linear regulators, switching transistors, pass
> transistors, and current sense* *resistors which can be identified
> using the BeagleBone schematic located at the link in the* *BeagleBone
> System Reference Manual. When placing measurement probes near these*
> *devices during normal operation, please be aware that these devices
> may be very warm to* *the touch. As with all electronic evaluation
> tools, only qualified personnel knowledgeable in* *electronic
> measurement and diagnostics normally found in development
> environments* *should use the BeagleBone.*
>
> ***Agreement to Defend, Indemnify and Hold Harmless**. You agree to
> defend, indemnify* *and hold the Suppliers, its licensors and their
> representatives harmless from and against* *any and all claims,
> damages, losses, expenses, costs and liabilities (collectively,*
> *"Claims") arising out of or in connection with any use of the
> BeagleBone that is not in* *accordance with the terms of the
> agreement. This obligation shall apply whether Claims* *arise under
> law of tort or contract or any other legal theory, and even if the
> BeagleBone* *fails to perform as described or expected.*
>
> ***Safety-Critical or Life-Critical Applications**. If you intend to
> evaluate the components for possible* *use in safety critical
> applications (such as life support) where a failure of the Supplier’s
> product* *would reasonably be expected to cause severe personal injury
> or death, such as devices which are* *classified as FDA Class III or
> similar classification, then you must specifically notify Suppliers
> of* *such intent and enter into a separate Assurance and Indemnity
> Agreement.*

Mailing Address:

BeagleBoard.org

1380 Presidential Dr. \#100

Richardson, TX 75081 U.S.A.

**WARRANTY:** *The BeagleBone Black Assembly as purchased is warranted
against defects in materials and workmanship for a period of 90 days
from purchase. This warranty does not cover any problems occurring as a
result of improper use, modifications, exposure to water, excessive
voltages, abuse, or accidents. All boards will be returned via standard
mail if an issue is found. If no issue is found or express return is
needed, the customer will pay all shipping costs*.

Before returning the board, please visit

*BeagleBoard.org/support*

For up to date SW images and technical information refer to
[*http://circuitco.com/support/index.php?title=BeagleBoneBlack*
](http://circuitco.com/support/index.php?title=BeagleBoneBlack)

All support for this board is provided via community support at
[*www.beagleboard.org/discuss*](http://www.beagleboard.org/discuss)

To return a defective board for repair, please request an RMA at
[*http://beagleboard.org/support/rma*](http://beagleboard.org/support/rma)

**Please DO NOT return the board without approval from the RMA team
first. **

> All boards received without RMA approval will not be worked on.

Table of Contents

##### **FIGURES .....................................................................................................................................................10** **TABLES .......................................................................................................................................................12** **1.0** **INTRODUCTION..............................................................................................................................13** **2.0** **CHANGE HISTORY .........................................................................................................................13** 2.1 DOCUMENT CHANGE HISTORY ........................................................................................................14 2.2 BOARD CHANGES .............................................................................................................................15 

> *2.2.1* *Rev C
> .....................................................................................................................................15*
> *2.2.2* *Rev B
> ......................................................................................................................................15*
>
> *2.2.3* *Rev A6A
> .................................................................................................................................15*
> *2.2.4* *Rev A6
> ....................................................................................................................................15*
> *2.2.5* *Rev A5C
> .................................................................................................................................15*
> *2.2.6* *Rev A5B
> .................................................................................................................................16*

*2.2.7* *Rev A5A
.................................................................................................................................16*

##### **3.0** **CONNECTING UP YOUR BEAGLEBONE BLACK ...................................................................17** 3.1 WHAT’S IN THE BOX ........................................................................................................................17 3.2 MAIN CONNECTION SCENARIOS.......................................................................................................18 3.3 TETHERED TO A PC .........................................................................................................................18 

*3.3.1* *Connect the Cable to the Board
.............................................................................................19*

*3.3.2* *Accessing the Board as a Storage
Drive................................................................................20*

#####  3.4 STANDALONE W/DISPLAY AND KEYBOARD/MOUSE ........................................................................21 

> *3.4.1* *Required Accessories
> .............................................................................................................21*
> *3.4.2* *Connecting Up the Board
> ......................................................................................................22*

*3.4.3* *Apply Power
..........................................................................................................................24*

##### **4.0** **BEAGLEBONE BLACK OVERVIEW ...........................................................................................27** 4.1 BEAGLEBONE COMPATIBILITY ........................................................................................................28 4.2 BEAGLEBONE BLACK FEATURES AND SPECIFICATION.....................................................................30 4.3 BOARD COMPONENT LOCATIONS.....................................................................................................31 

*4.3.1* *Connectors, LEDs, and Switches
...........................................................................................31*

*4.3.2* *Key Components
....................................................................................................................32*

##### **5.0** **BEAGLEBONE BLACK HIGH LEVEL SPECIFICATION ........................................................33** 5.1 BLOCK DIAGRAM .............................................................................................................................33 5.2 PROCESSOR ......................................................................................................................................33 5.3 MEMORY..........................................................................................................................................34 

> *5.3.1* *512MB DDR3L
> ......................................................................................................................34*
> *5.3.2* *4KB EEPROM
> .......................................................................................................................34*
> *5.3.3* *4GB Embedded MMC
> ............................................................................................................34*
> *5.3.4* *MicroSD Connector
> ...............................................................................................................34*
>
> *5.3.5* *Boot Modes
> ............................................................................................................................34*
> 5.4 POWER
> MANAGEMENT.....................................................................................................................35
>
> 5.5 PC USB INTERFACE
> .........................................................................................................................36
> 5.6 SERIAL DEBUG PORT
> .......................................................................................................................36
> 5.7 USB1 HOST PORT
> ............................................................................................................................36
> 5.8 POWER SOURCES
> .............................................................................................................................36
> 5.9 RESET BUTTON
> ................................................................................................................................37
> 5.10 POWER BUTTON
> ..........................................................................................................................37
> 5.11 INDICATORS
> ................................................................................................................................37
> 5.12 CTI JTAG HEADER
> .....................................................................................................................38
> 5.13 HDMI INTERFACE
> .......................................................................................................................38

##### 5.14 CAPE BOARD SUPPORT................................................................................................................38 **6.0** **DETAILED HARDWARE DESIGN ...............................................................................................40** 6.1 POWER SECTION ..............................................................................................................................41 

> *6.1.1* *TPS65217C PMIC
> .................................................................................................................41*
> *6.1.2* *DC Input
> ................................................................................................................................44*
> *6.1.3* *USB Power
> ............................................................................................................................45*
>
> *6.1.4* *Power Selection
> .....................................................................................................................45*
> *6.1.5* *Power Button
> .........................................................................................................................45*
> *6.1.6* *Battery Access Pads
> ...............................................................................................................46*
> *6.1.7* *Power Consumption
> ..............................................................................................................47*
> *6.1.8* *Processor Interfaces
> ..............................................................................................................47*
> *6.1.9* *Power Rails
> ...........................................................................................................................49*
>
> *6.1.10* *Power LED
> .......................................................................................................................52*
> *6.1.11* *TPS65217C Power Up Process
> ........................................................................................52*
> *6.1.12* *Processor Control Interface
> .............................................................................................53*

*6.1.13* *Low Power Mode Support
................................................................................................53*

#####  6.2 SITARA AM3358BZCZ100 PROCESSOR ..........................................................................................54 

> *6.2.1* *Description
> ............................................................................................................................54*
> *6.2.2* *High Level Features
> ..............................................................................................................56*
> *6.2.3*
> *Documentation.......................................................................................................................56*
> *6.2.4* *Crystal Circuitry
> ....................................................................................................................57*
> *6.2.5* *Reset Circuitry
> .......................................................................................................................58*
> *6.2.6* *Memory Device
> ......................................................................................................................59*
>
> *6.2.7* *DDR3L Memory Design
> ........................................................................................................59*
> *6.2.8* *Power Rails
> ...........................................................................................................................61*

*6.2.9* *VREF
.....................................................................................................................................61*

#####  6.3 4GB EMMC MEMORY .....................................................................................................................62 

*6.3.1* *eMMC Device
........................................................................................................................62*

*6.3.2* *eMMC Circuit
Design............................................................................................................63*

> 6.4 BOARD ID EEPROM
> .......................................................................................................................64
> 6.5 MICRO SECURE DIGITAL
> ..................................................................................................................65

*6.5.1* *microSD Design
.....................................................................................................................65*

##### 6.6 USER LEDS ......................................................................................................................................66 6.7 BOOT CONFIGURATION ....................................................................................................................67 

> *6.7.1* *Boot Configuration Design
> ....................................................................................................67*
> 6.8 DEFAULT BOOT OPTIONS
> .................................................................................................................68

#####  6.9 10/100 ETHERNET ............................................................................................................................69 

> *6.9.1* *Ethernet Processor Interface
> .................................................................................................69*
> *6.9.2* *Ethernet Connector Interface
> ................................................................................................70*
> *6.9.3* *Ethernet PHY Power, Reset, and Clocks
> ...............................................................................71*

*6.9.4* *LAN8710A Mode Pins
...........................................................................................................72*

#####  6.10 HDMI INTERFACE .......................................................................................................................73 

> *6.10.1* *Supported Resolutions
> ......................................................................................................73*
> *6.10.2* *HDMI Framer
> ...................................................................................................................74*
> *6.10.3* *HDMI Video Processor Interface
> .....................................................................................74*
> *6.10.4* *HDMI Control Processor Interface
> ..................................................................................75*
>
> *h6.10.6* *Audio Interface
> .................................................................................................................76*
> *6.10.7* *Power Connections
> ...........................................................................................................77*

*6.10.8* *HDMI Connector Interface
...............................................................................................78*

#####  6.11 USB HOST ..................................................................................................................................79 

> *6.11.1* *Power Switch
> ....................................................................................................................79*
> *6.11.2* *ESD Protection
> .................................................................................................................79*
> *6.11.3* *Filter Options
> ....................................................................................................................79*

#####  6.12 PRU-ICSS ..................................................................................................................................80

> *6.12.1* *PRU-ICSS Features
> ..........................................................................................................80*
> *6.12.2* *PRU-ICSS Block Diagram
> ................................................................................................80*

*6.12.3* *PRU-ICSS Pin Access
.......................................................................................................81*

##### **7.0** **CONNECTORS .................................................................................................................................82** 7.1 EXPANSION CONNECTORS ................................................................................................................82 

*7.1.1* *Connector P8
.........................................................................................................................83*

*7.1.2* *Connector P9
.........................................................................................................................85*

##### 7.2 POWER JACK ....................................................................................................................................87 7.3 USB CLIENT ....................................................................................................................................88 7.4 USB HOST .......................................................................................................................................89 7.5 SERIAL HEADER ...............................................................................................................................90 7.6 HDMI ..............................................................................................................................................92 7.7 MICROSD .........................................................................................................................................93 7.8 ETHERNET ........................................................................................................................................94 7.9 JTAG CONNECTOR ..........................................................................................................................94 **8.0** **CAPE BOARD SUPPORT ................................................................................................................95** 8.1 BEAGLEBONEBLACK CAPE COMPATIBILITY ....................................................................................96 

*8.1.1* *LCD Pins
...............................................................................................................................96*

*8.1.2* *eMMC Pins
............................................................................................................................97*

#####  8.2 EEPROM ........................................................................................................................................98 

> *8.2.1* *EEPROM Address
> .................................................................................................................99*
> *8.2.2* *I2C Bus
> ................................................................................................................................100*
>
> *8.2.3* *EEPROM Write Protect
> .......................................................................................................100*
> *8.2.4* *EEPROM Data Format
> .......................................................................................................101*

*8.2.5* *Pin Usage
............................................................................................................................102*

8.3 PIN USAGE CONSIDERATION
..........................................................................................................106

*8.3.1* *Boot Pins
.............................................................................................................................106*

#####  8.4 EXPANSION CONNECTORS ..............................................................................................................107 

> *8.4.1* *Non-Stacking Headers-Single Cape
> ...................................................................................107*
> *8.4.2* *Main Expansion Headers-Stacking
> .....................................................................................108*
> *8.4.3* *Stacked Capes w/Signal Stealing
> .........................................................................................110*
> *8.4.4* *Retention Force
> ...................................................................................................................110*

*8.4.5* *BeagleBone Black Female Connectors
................................................................................110*

##### 8.5 SIGNAL USAGE ..............................................................................................................................111 8.6 CAPE POWER..................................................................................................................................112 

*8.6.1* *Main Board Power
..............................................................................................................112*

*8.6.2* *Expansion Board External Power
.......................................................................................112*

#####  8.7 MECHANICAL .................................................................................................................................113 

> *8.7.1* *Standard Cape Size
> ..............................................................................................................113*
> *8.7.2* *Extended Cape Size
> .............................................................................................................114*

*8.7.3* *Enclosures
...........................................................................................................................115*

##### **9.0** **BEAGLEBONE BLACK MECHANICAL ...................................................................................116** 9.1 DIMENSIONS AND WEIGHT .............................................................................................................116 9.2 SILKSCREEN AND COMPONENT LOCATIONS ...................................................................................117 **10.0** **PICTURES ..................................................................................................................................120** **11.0** **SUPPORT INFORMATION .....................................................................................................122** 11.1 HARDWARE DESIGN ..................................................................................................................122 11.2 SOFTWARE UPDATES .................................................................................................................122 11.3 RMA SUPPORT..........................................................................................................................123 11.4 TROUBLE SHOOTING HDMI ISSUES ..........................................................................................124 

*11.4.1* *EDID
...............................................................................................................................124*

*11.4.2* *DISPLAY SOURCE SELECTION
...................................................................................125*

*11.4.3* *OUT OF SEQUENCE
.....................................................................................................125*

*11.4.4* *OVERSCAN
....................................................................................................................125*

*11.4.5* *Taking a Nap
...................................................................................................................125*

*11.4.6* *AUDIO
............................................................................................................................125*

*11.4.7* *Getting Help
....................................................................................................................126*

**Figures **
============

Figure 1. In The Box
....................................................................................................
17

Figure 2. Tethered Configuration
.................................................................................
18

Figure 3. USB Connection to the
Board.......................................................................
19

Figure 4. Board Power LED
.........................................................................................
19

Figure 5. Board Boot Status
.........................................................................................
20

Figure 6. Desktop Configuration
..................................................................................
21

Figure 7. Connect microHDMI Cable to the Monitor
.................................................. 22

Figure 8. DVI-D to HDMI
Adapter..............................................................................
22

Figure 9. Wireless Keyboard and Mouse Combo
........................................................ 23

Figure 10. Connect Keyboard and Mouse Receiver to the Board
.............................. 23

Figure 11. Keyboard and Mouse Hubs
.......................................................................
23

Figure 12. Ethernet Cable Connection
.......................................................................
24

Figure 13. External DC Power
...................................................................................
24

Figure 14. Connect microHDMI Cable to the Board
................................................. 25

Figure 15. Board Boot Status
.....................................................................................
25

Figure 16. Desktop Screen
.........................................................................................
26

Figure 17. Connectors, LEDs and Switches
............................................................... 31

Figure 18. Key Components
.......................................................................................
32

Figure 19. BeagleBone Black Key Components
........................................................ 33

Figure 20. BeagleBone Black Block Diagram
........................................................... 40

Figure 21. High Level Power Block Diagram
............................................................ 41

Figure 22. TPS65217C Block Diagram
..................................................................... 43

Figure 23. TPS65217 DC Connection
........................................................................
44

Figure 24. USB Power
Connections...........................................................................
45

Figure 25. Power Rails
...............................................................................................
49

Figure 26. Power Rail Power Up Sequencing
............................................................ 51

Figure 27. TPS65217C Power Sequencing Timing
................................................... 52

Figure 28. Power Processor Interfaces
.......................................................................
52

Figure 29. Sitara AM3358BZCZ Block Diagram
...................................................... 55

Figure 30. Processor Crystals
.....................................................................................
57

Figure 31. Board Reset Circuitry
...............................................................................
58

Figure 32. DDR3L Memory
Design...........................................................................
60

Figure 33. DDR3L VREF Design
..............................................................................
61

Figure 34. eMMC Memory Design
............................................................................
63

Figure 35. EEPROM Design Rev A5
.........................................................................
65

Figure 36. microSD Design
........................................................................................
65

  Figure 37.   User LEDs ................................................................................................. 66
  ------------ -----------------------------------------------------------------------------------------------------------------
  Figure 38.   Processor Boot Configuration Design ...................................................... 68
  Figure 39.   Processor Boot Configuration ................................................................... 68
  Figure 40.   Ethernet Processor Interface ..................................................................... 69
  Figure 41.   Ethernet Connector Interface .................................................................... 70
  Figure 42.   Ethernet PHY, Power, Reset, and Clocks ................................................. 71
  Figure 43.   Ethernet PHY Mode Pins .......................................................................... 72
  Figure 44.   HDMI Framer Processor Interface ............................................................ 75
  Figure 45.   24.576MHZ Oscillator .............................................................................. 76
  Figure 46.   HDMI Power Connections ........................................................................ 77
  Figure 47.   Connector Interface Circuitry ................................................................... 78
  Figure 48.   USB Host Circuitry ................................................................................... 79
  Figure 49.   PRU-ICSS Block Diagram ....................................................................... 80
  Figure 50.   Expansion Connector Location ................................................................. 82
  Figure 51.   5VDC Power Jack ..................................................................................... 87
  Figure 52.   USB Client Connector .............................................................................. 88
  Figure 53.   USB Host Connector................................................................................. 89
  Figure 54.   Serial Debug Header ................................................................................. 90
  Figure 55.   FTDI USB to Serial Adapter ..................................................................... 90
  Figure 56.   Serial Header ............................................................................................. 91
  Figure 57.   HDMI Connector ...................................................................................... 92
  Figure 58.   HDMI Cable.............................................................................................. 92
  Figure 59.   microSD Connector .................................................................................. 93
  Figure 60.   Ethernet Connector ................................................................................... 94
  Figure 61.   Expansion Board EEPROM Without Write Protect ................................. 99
  Figure 62.   Expansion Board EEPROM Write Protect ............................................. 100
  Figure 63.   Expansion Boot Pins ............................................................................... 106
  Figure 64.   Single Expansion Connector ................................................................... 107
  Figure 65.   Single Cape Expansion Connector.......................................................... 108
  Figure 66.   Expansion Connector .............................................................................. 108
  Figure 67.   Stacked Cape Expansion Connector ....................................................... 109
  Figure 68.   Stacked w/Signal Stealing Expansion Connector ................................... 110
  Figure 69.   Connector Pin Insertion Depth ................................................................ 111
  Figure 70.   Cape Board Dimensions ........................................................................ 114
  Figure 71.   Board Dimensions ................................................................................... 117
  Figure 72.   Component Side Silkscreen .................................................................... 118
  Figure 73.   Circuit Side Silkscreen ............................................................................ 119
  Figure 74.   Top Side .................................................................................................. 120
  Figure 75.   Bottom Side ............................................................................................ 121
  Figure 76.   Initial Serial Number and Revision Locations ........................................ 123
  Figure 77.   Second Phase Serial Number and Revision Location ............................. 123
  Figure 78.   Third Phase Serial Number and Revision Location ................................ 124

 **Tables **
============

  Table 1.    Change History ............................................................................................. 14
  ----------- -----------------------------------------------------------------------------------------------------------------
  Table 2.    BeagleBone Black Features .......................................................................... 30
  Table 3.    BeagleBone Black Battery Pins .................................................................... 46
  Table 4.    BeagleBone Black Power Consumption(mA@5V) ...................................... 47
  Table 5.    Processor Features ........................................................................................ 56
  Table 6.    eMMC Boot Pins .......................................................................................... 63
  Table 7.    EEPROM Contents ....................................................................................... 64
  Table 8.    User LED Control Signals/Pins .................................................................... 67
  Table 9.    HDMI Supported Monitor Resolutions ........................................................ 73
  Table 10.   TDA19988 I2C Address ............................................................................... 75
  Table 11.   PRU0 and PRU1 Access ............................................................................... 81
  Table 12.   Expansion Header P8 Pinout ........................................................................ 84
  Table 13.   Expansion Header P9 Pinout ........................................................................ 86
  Table 14.   J1 Serial Header Pins .................................................................................... 91
  Table 15.   P8 LCD Conflict Pins ................................................................................... 96
  Table 16.   P8 eMMC Conflict Pins ................................................................................ 97
  Table 17.   Expansion Board EEPROM ........................................................................ 101
  Table 18.   EEPROM Pin Usage ................................................................................... 103
  Table 19.   Single Cape Connectors .............................................................................. 108
  Table 20.   Stacked Cape Connectors ........................................................................... 109
  Table 21.   Expansion Voltages .................................................................................... 112

**1.0 Introduction **
=====================

This document is the **System Reference Manual** for the BeagleBone
Black and covers its use and design. The board will primarily be
referred to in the remainder of this document simply as the board,
although it may also be referred to as the BeagleBone Black as a
reminder. There are also references to the original BeagleBone as well,
and will be referenced as simply BeagleBone.

This design is subject to change without notice as we will work to keep
improving the design as the product matures based on feedback and
experience. Software updates will be frequent and will be independent of
the hardware revisions and as such not result in a change in the
revision number.

Make sure you check the support Wiki frequently for the most up to date
information.

[*http://circuitco.com/support/index.php?title=BeagleBoneBlack*
](http://circuitco.com/support/index.php?title=BeagleBoneBlack)

**2.0 Change History **
=======================

This section describes the change history of this document and board.
Document changes are not always a result of a board change. A board
change will always result in a document change.

### 2.1 Document Change History 

**Table 1. Change History **

  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  > **Rev **   > **Changes **         > **Date **                                                                                                              > **By **
  ------------ ---------------------- ------------------------------------------------------------------------------------------------------------------------ --------------------- ------
  > A4         > Preliminary          > January 4, 2013                                                                                                        > GC

  > A5         > Production release   > January 8.2013                                                                                                         > GC

  > A5.1       > 1.                   Added information on Power button and the battery access points.                                                         > April 1 2013
               >                                                                                                                                               
               > 2.                   Final production released version.                                                                                       

  > A5.2       > 1.                   Edited version.                                                                                                          > April 23 2013
               >                                                                                                                                               
               > 2.                   Added numerous pictures of the Rev A5A board.                                                                            

  > A5.3       > 1.                   Updated serial number locations.                                                                                         > April 30, 2013
               >                                                                                                                                               
               > 2.                   Corrected the feature table for 4 UARTS                                                                                  
               >                                                                                                                                               
               > 3.                   Corrected eMMC pin table to match other tables in the manual.                                                            

  > A5.4       > 1.                   Corrected revision listed in section 2. Rev A5A is the initial production release.                                       > May 12, 2013
               >                                                                                                                                               
               > 2.                   Added all the locations of the serial numbers Made additions to the compatibility list.                                  
               >                                                                                                                                               
               > 3.                   Corrected Table 7 for LED GPIO pins.                                                                                     
               >                                                                                                                                               
               > 4.                   Fixed several typos.                                                                                                     
               >                                                                                                                                               
               > 5\. 6.               Added some additional information about LDOs and StepDown converters.                                                    
               >                                                                                                                                               
               > 7.                   Added short section on HDMI.                                                                                             

  > A5.5       > 1.                   Release of the A5B version.                                                                                              > May 20, 2013
               >                                                                                                                                               
               > 2.                   The LEDS were dimmed by changing the resistors.                                                                          
               >                                                                                                                                               
               > 3.                   The serial termination mode was incorporated into the PCB.                                                               

  > A5.6       > 1.                   Added information on Rev A5C                                                                                             > June 16, 2013
               >                                                                                                                                               
               > 2.                   Added PRU/ICSS options to tables for P8 and P9. Added section on USB Host Correct modes on Table 15. Fixed a few typos   
               >                                                                                                                                               
               > 3.                                                                                                                                            
               >                                                                                                                                               
               > 4.                                                                                                                                            
               >                                                                                                                                               
               > 5.                                                                                                                                            

  > A5.7       > 1\. 2.               Updated assembly revision to A6.                                                                                         > August 9, 2013
               >                                                                                                                                               
               > 3.                   PCB change to add buffer to the reset line and ground the oscillator GND pin.                                            
                                                                                                                                                               
                                      Added resistor on PCB for connection of OSC\_GND to board GND.                                                           

  > A6         > 1.                   Added Rev A6 changes.                                                                                                    > October 11, 2013

  > A6A        > 1.                   Added Rev A6A changes                                                                                                    > December 17, 2013

  > B          > 1.                   Changed the processor to the AM3358BZCZ                                                                                  > January 20, 2013

  > C          > 1.                   Changed the eMMC from 2GB to 4GB.                                                                                        > March 21,2014
               >                                                                                                                                               
               > 2.                   Added additional supplier to DDR2 and eMMC.                                                                              

  > C.1        > 1.                   Added note to recommend powering off the board with the power button.                                                    > March 22.2014
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### 2.2 Board Changes 

#### 2.2.1 Rev C 

>  Changed the eMMC from 2GB to 4GB.

2GB devices are getting harder to get as they are being phased out. This
required us to move to 4GB. We now have two sources for the device. This
will however, require an increase in the price of the board.

#### 2.2.2 Rev B 

>  Changed the processor to the AM3358BZCZ100.

#### 2.2.3 Rev A6A 

-   Added connection from 32KHz OSC\_GND to system ground and changed
    C106 to 1uF.

-   Changes C25 to 2.2uF. This resolved an issue we were seeing in a few
    boards where the board would not boot in 1 in 20 tries.

-   Change required PCB revision to B6.

#### 2.2.4 Rev A6 

-   In random instances there could be a glitch in the SYS\_RESETn
    signal from the processor where the SYS\_RESETn signal was taken
    high for a momentary amount of time before it was supposed to. To
    prevent this, the signal was ORed with the PORZn (Power On reset).

-   Noise issues were observed in other design where the clock
    oscillator was getting hit due to a suspected issue in ground
    bounce. A zero ohm resistor was added to connect the OSC\_GND to the
    system ground.

There are no new features added as a result of these changes.

#### 2.2.5 Rev A5C 

We were seeing some fallout in production test where we were seeing some
jitter on the HDMI display test. It started showing up on out second
production run. R46, R47, R48 were changed to 0 ohm from 33 ohm. R45 was
taken from 330 ohm to 22 ohm.

We do not know of any boards that were shipped with this issue as this
issue was caught in production test. No impact on features or
functionality resulted from this change.

#### 2.2.6 Rev A5B 

There is no operational difference between the Rev A5A and the Rev A5B.
There were two changes made to the A5B version.

-   Due to complaints about the brightness of the LEDs keeping people
    awake at night, the LEDs were dimmed. Resistors were changed from
    820 ohms to 4.75K ohms.

-   The PCB revision was updated to incorporate the hand mod that was
    being done on the board during manufacturing. The resistor was
    incorporated into the next revision of the PCB.

The highest supported resolution is now listed as 1920x1080@24Hz. This
was not a result of any hardware changes but only updated software. The
A5A version also supports this resolution.

#### 2.2.7 Rev A5A 

This is the initial production release of the board. We will be tracking
changes from this point forward.

**3.0 Connecting Up Your BeagleBone Black **
============================================

This section provides instructions on how to hook up your board. Two
scenarios will be discussed:

1)  Tethered to a PC and

2)  As a standalone development platform in a desktop PC configuration.

### 3.1 What’s In the Box 

In the box you will find three main items as shown in **Figure 1**.

-   BeagleBone Black

-   miniUSB to USB Type A Cable

-   Instruction card with link to the support WIKI address.

This is sufficient for the tethered scenario and creates an out of box
experience where the board can be used immediately with no other
equipment needed.

![](docs/media/image7.jpg){width="5.983333333333333in"
height="4.160416666666666in"}

**Figure 1. In The Box **

### 3.2 Main Connection Scenarios 

This section will describe how to connect the board for use. This
section is basically a slightly more detailed description of the Quick
Start Guide that came in the box. There is also a Quick Start Guide
document on the board that should also be referred to. The intent here
is that someone looking t purchase the board will be able to read this
section and get a good idea as to what the initial set up will be like.

The board can be configured in several different ways, but we will
discuss the two most common scenarios as described in the Quick Start
Guide card that comes in the box.

-   Tethered to a PC via the USB cable o Board is accessed as a storage
    drive o Or a RNDIS Ethernet connection.

-   Standalone desktop o Display o Keyboard and mouse

> o External 5V power supply

Each of these configurations is discussed in general terms in the
following sections.

For an up-to-date list of confirmed working accessories please go to
[*http://circuitco.com/support/index.php?title=BeagleBone\_Black\_Accessories*](http://circuitco.com/support/index.php?title=BeagleBone_Black_Accessories)

### 3.3 Tethered To A PC 

In this configuration, the board is powered by the PC via the provided
USB cable--no other cables are required. The board is accessed either as
a USB storage drive or via the browser on the PC. You need to use either
Firefox or Chrome on the PC, IEx will not work properly. **Figure 2**
shows this configuration.

![](docs/media/image8.jpg){width="6.593055555555556in"
height="1.738888888888889in"}

######  Figure 2. Tethered Configuration 

All the power for the board is provided by the PC via the USB cable. In
some instances, the PC may not be able to supply sufficient power for
the board. In that case, an external 5VDC power supply can be used, but
this should rarely be necessary.

#### 3.3.1 Connect the Cable to the Board 

> 1\. Connect the small connector on the USB cable to the board as shown in
> **Figure 4**. The connector is on the bottom side of the board.

![](docs/media/image9.jpg){width="4.700001093613299in"
height="2.1534722222222222in"}

######  Figure 3. USB Connection to the Board 

2.  Connect the large connector of the USB cable to your PC or laptop
    USB port.

3.  The board will power on and the power LED will be on as shown in
    **Figure 4** below.

![](docs/media/image10.jpg){width="4.1819444444444445in"
height="2.786111111111111in"}

######  Figure 4. Board Power LED 

> 4\. When the board starts to the booting process started by the process
> of applying power, the LEDs will come on in sequence as shown in
> **Figure 5** below. It will take a few seconds for the status LEDs to
> come on, so be patient. The LEDs will be flashing in an erratic manner
> as it begins to boot the Linux kernel.

![](docs/media/image11.jpg){width="5.641666666666667in"
height="2.6479166666666667in"}

######  Figure 5. Board Boot Status 

#### 3.3.2 Accessing the Board as a Storage Drive 

The board will appear around a USB Storage drive on your PC after the
kernel has booted, which will take a round 10 seconds. The kernel on the
board needs to boot before the port gets enumerated. Once the board
appears as a storage drive, do the following:

1)  Open the USB Drive folder.

2)  Click on the file named **start.html**

3)  The file will be opened by your browser on the PC and you should get
    a display showing the Quick Start Guide.

4)  Your board is now operational! Follow the instructions on your PC
    screen.

### 3.4 Standalone w/Display and Keyboard/Mouse 

In this configuration, the board works more like a PC, totally free from
any connection to a PC as shown in **Figure 6**. It allows you to create
your code to make the board do whatever you need it to do. It will
however require certain common PC accessories. These accessories and
instructions are described in the following section.

> ![](docs/media/image12.jpg){width="3.713888888888889in"
> height="4.270138888888889in"}

######  Figure 6. Desktop Configuration 

Optionally an Ethernet cable can also be used for network access.

#### 3.4.1 Required Accessories 

In order to use the board in this configuration, you will need the
following accessories:

-   \(1) 5VDC 1A power supply

-   \(1) HDMI monitor or a DVI-D monitor. (**NOTE:** Only HDMI will give you
    audio capability).

-   \(1) Micro HDMI to HDMI cable or a Micro HDMI to DVI-D adapter.

-   \(1) USB wireless keyboard and mouse combo.

-   \(1) USB HUB (OPTIONAL). The board has only one USB host port, so you may
    need to use a USB Hub if your keyboard and mouse requires two ports.

For an up-to-date list of confirmed working accessories please go to
[*http://circuitco.com/support/index.php?title=BeagleBone\_Black\_Accessories*](http://circuitco.com/support/index.php?title=BeagleBone_Black_Accessories)

#### 3.4.2 Connecting Up the Board 

> 1\. Connect the big end of the HDMI cable as shown in **Figure 7** to
> your HDMI monitor. Refer to your monitor Owner’s Manual for the location
> of your HDMI port. If you have a DVI-D Monitor go to **Step 3**,
> otherwise proceed to **Step 4.**

![](docs/media/image13.jpg){width="2.716666666666667in"
height="0.9916666666666667in"}

######  Figure 7. Connect microHDMI Cable to the Monitor 

2.  If you have a DVI-D monitor you must use a DVI-D to HDMI adapter in
    addition to your HDMI cable. An example is shown in **Figure 8**
    below from two perspectives. If you use this configuration, you will
    not have audio support.

> ![](docs/media/image14.jpg){width="5.068694225721785in"
> height="2.930533683289589in"}

2.  If you have a single wireless keyboard and mouse combination such as
    seen in Figure **9** below, you need to plug the receiver in the USB
    host port of the board as shown in **Figure 10**.

![](docs/media/image16.jpg){width="2.475in"
height="1.1333333333333333in"}

######  Figure 9. Wireless Keyboard and Mouse Combo 

![](docs/media/image17.jpg){width="2.9069444444444446in"
height="2.316666666666667in"}

###### Figure 10. Connect Keyboard and Mouse Receiver to the Board 

If you have a wired USB keyboard requiring two USB ports, you will need
a HUB similar to the ones shown in **Figure 11**. You may want to have
more than one port for other devices. Note that the board can only
supply up to 500mA, so if you plan to load it down, it will need to be
externally powered.

![](docs/media/image18.jpg){width="5.309722222222222in"
height="1.5853062117235346in"}

###### Figure 11. Keyboard and Mouse Hubs 

> 4\. Connect the Ethernet Cable

If you decide you want to connect to your local area network, an
Ethernet cable can be used. Connect the Ethernet Cable to the Ethernet
port as shown in **Figure 12**. Any standard 100M Ethernet cable should
work.

> ![](docs/media/image24.jpg){width="4.511805555555555in"
> height="2.7583333333333333in"}

###### Figure 12. Ethernet Cable Connection 

#### 3.4.3 Apply Power 

The final step is to plug in the DC power supply to the DC power jack as
shown in **Figure 13** below.

![](docs/media/image25.jpg){width="6.441666666666666in"
height="3.1118055555555557in"}

###### Figure 13. External DC Power 

> 5\. The cable needed to connect to your display is a microHDMI to HDMI.
> Connect the microHDMI connector end to the board at this time. The
> connector is on the bottom side of the board as shown in **Figure 14**
> below.

![](docs/media/image26.jpg){width="5.626388888888889in"
height="2.370138888888889in"}

###### Figure 14. Connect microHDMI Cable to the Board 

The connector is fairly robust, but we suggest that you not use the
cable as a leash for your Beagle. Take proper care not to put too much
stress on the connector or cable.

> 6\. Booting the Board
>
> As soon as the power is applied to the board, it will start the
> booting up process. When the board starts to boot the LEDs will come
> on in sequence as shown in **Figure 15** below. It will take a few
> seconds for the status LEDs to come on, so be patient. The LEDs will
> be flashing in an erratic manner as it boots the Linux kernel.

![](docs/media/image11.jpg){width="5.641666666666667in"
height="2.6486111111111112in"}

###### Figure 15. Board Boot Status 

While the four user LEDS can be over written and used as desired, they
do have specific meanings in the image that is shipped with the board
once the Linux kernel has booted.  **USER0** is the heartbeat indicator
from the Linux kernel.

-   **USER1** turns on when the microSD card is being accessed

-   **USER2** is an activity indicator. It turns on when the kernel is
    not in the idle loop.

-   **USER3** turns on when the onboard eMMC is being accessed.

> 7\. A Booted System

1.  The board will have a mouse pointer appear on the screen as it
    enters the Linux boot step. You may have to move the physical mouse
    to get the mouse pointer to appear. The system can come up in the
    suspend mode with the HDMI port in a sleep mode.

2.  After a minute or two a login screen will appear. You do not have to
    do anything at this point.

3.  After a minute or two the desktop will appear. It should be similar
    to the one shown in **Figure 16**. HOWEVER, it will change from one
    release to the next, so do not expect your system to look exactly
    like the one in the figure, but it will be very similar.

4.  And at this point you are ready to go! **Figure 16** shows the
    desktop after booting.

![](docs/media/image27.jpg){width="5.346527777777778in"
height="3.0083333333333333in"}

###### Figure 16. Desktop Screen 

> 8\. Powering Down
>
> 1\. Press the power button momentarily 2. The system will power down
> automatically.
>
> 3\. Remove the power jack.

**4.0 BeagleBone Black Overview **
==================================

The BeagleBone Black is the latest addition to the BeagleBoard.org
family and like its predecessors, is designed to address the Open Source
Community, early adopters, and anyone interested in a low cost ARM
Cortex-A8 based processor.

It has been equipped with a minimum set of features to allow the user to
experience the power of the processor and is not intended as a full
development platform as many of the features and interfaces supplied by
the processor are not accessible from the BeagleBone Black via onboard
support of some interfaces. It is not a complete product designed to do
any particular function. It is a foundation for experimentation and
learning how to program the processor and to access the peripherals by
the creation of your own software and hardware.

It also offers access to many of the interfaces and allows for the use
of add-on boards called capes, to add many different combinations of
features. A user may also develop their own board or add their own
circuitry.

BeagleBone Black is manufactured and warranted by Circuitco LLC in
Richardson Texas for the benefit of the community and its supporters. In
addition, Circuitco provides the RMA support for the BeagleBone Black.

Jason Kridner of Texas Instruments handles the community promotions and
is the spokesman for BeagleBoard.org.

The board is designed by Gerald Coley, an employee of Texas Instruments
and a charter member of the BeagleBoard.org community.

The PCB layout was done by Circuitco and Circuitco is the sole funder of
its development and transition to production.

The Software is written and supported by the thousands of community
members, including Jason Kridner, employees of Texas Instruments,
DigiKey, and Circuitco.

.

### 4.1 BeagleBone Compatibility 

The board is intended to be compatible with the original BeagleBone as
much as possible. There are several areas where there are differences
between the two designs. These differences are listed below, along with
the reasons for the differences.

-   Sitara AM3358BZCZ100, 1GHZ, processor.

    -   Sorry, we just had to make it faster.

-   512MB DDR3L

    -   *Cost reduction* o Performance boost o Memory size increase o
        Lower power

-   No Serial port by default.

    -   *Cost reduction*

    -   Can be added by buying a TTL to USB Cable that is widely
        available o Single largest cost reduction action taken

-   No JTAG emulation over USB. o *Cost reduction.* JTAG header is not
    populated, but can easily be mounted.

-   EEPROM Reduced from 32KB to 4KB o Cost Reduction

-   Onboard Managed NAND (eMMC) o 4GB

    -   *Cost reduction*

    -   Performance boost x8 vs. x4 bits

    -   Performance boost due to deterministic properties vs. microSD
        card

-   GPMC bus may not be accessible from the expansion headers in some
    cases o Result of eMMC on the main board o Signals are still routed
    to the expansion connector

    -   If eMMC is not used, signals can be used via expansion if eMMC
        is held in reset

-   There may be 10 less GPIO pins available o Result of eMMC

    -   If eMMC is not used, could still be used

-   The power expansion header, for battery and backlight, has been
    removed o *Cost reduction, s*pace reduction o Four pins were added
    to provide access to the battery charger function.

-   HDMI interface onboard o Feature addition

    -   Audio and video capable

    -   Micro HDMI

-   No three function USB cable o *Cost reduction*

-   GPIO3\_21 has a 24.576 MHZ clock on it.

> o This is required by the HDMI Framer for Audio purposes. We needed to
> run a clock into the processor to generate the correct clock
> frequency. The pin on the processor was already routed to the
> expansion header. In order not to remove this feature on the expansion
> header, it was left connected. In order to use the pin as a GPIO pin,
> you need to disable the clock. While this disables audio to the HDMI,
> the fact that you want to use this pin for something else, does the
> same thing.

### 4.2 BeagleBone Black Features and Specification 

This section covers the specifications and features of the board and
provides a high level description of the major components and interfaces
that make up the board.

**Table 2** provides a list of the features.

#######  Table 2. BeagleBone Black Features 

  ---------------------------------------------------------------------------------------------------------------------------------------------------
                                **Feature **
  ----------------------------- --------------------------------------------------------------------------------------- -----------------------------
  **Processor **                > Sitara AM3358BZCZ100 1GHz, 2000 MIPS

  **Graphics Engine **          SGX530 3D, 20M Polygons/S

  **SDRAM Memory **             512MB DDR3L 800MHZ

  **Onboard Flash **            4GB, 8bit Embedded MMC

  **PMIC **                     TPS65217C PMIC regulator and one additional LDO.

  **Debug Support **            Optional Onboard 20-pin CTI JTAG, Serial Header

  **Power Source **             > miniUSB USB or DC Jack

  **PCB **                      3.4” x 2.1”

  **Indicators **               1-Power, 2-Ethernet, 4-User Controllable LEDs

  **HS USB 2.0 Client Port **   Access to USB0, Client mode via miniUSB

  **HS USB 2.0 Host Port **     Access to USB1, Type A Socket, 500mA LS/FS/HS

  **Serial Port **              UART0 access via 6 pin 3.3V TTL Header. Header is populated

  **Ethernet **                 10/100, RJ45

  **SD/MMC Connector **         microSD , 3.3V

  **User Input **               Reset Button
                                
                                Boot Button
                                
                                Power Button

  **Video Out **                16b HDMI, 1280x1024 (MAX)
                                
                                > 1024x768,1280x720,1440x900 ,1920x1080@24Hz w/EDID Support

  **Audio **                    Via HDMI Interface, Stereo

  **Expansion Connectors **     Power 5V, 3.3V , VDD\_ADC(1.8V)
                                
                                3.3V I/O on all signals
                                
                                McASP0, SPI1, I2C, GPIO(69 max), LCD, GPMC, MMC1, MMC2, 7
                                
                                AIN***(1.8V MAX)***, 4 Timers, 4 Serial Ports, CAN0,
                                
                                EHRPWM(0,2),XDMA Interrupt, Power button, Expansion Board ID (Up to 4 can be stacked)

  **Weight **                   1.4 oz (39.68 grams)

  **Power **                    Refer to Section 6.1.7
  ---------------------------------------------------------------------------------------------------------------------------------------------------

### 4.3 Board Component Locations 

This section describes the key components on the board. It provides
information on their location and function. Familiarize yourself with
the various components on the board.

#### 4.3.1 Connectors, LEDs, and Switches 

**Figure 17** below shows the locations of the connectors, LEDs, and
switches on the PCB layout of the board.

![](docs/media/image28.jpg){width="5.309722222222222in"
height="3.546527777777778in"}

####### Figure 17. Connectors, LEDs and Switches 

-   **DC Power** is the main DC input that accepts 5V power.

-   **Power Button** alerts the processor to initiate the power down
    sequence and is used to power down the board.

-   **10/100 Ethernet** is the connection to the LAN.

-   **Serial Debug** is the serial debug port.

-   **USB Client** is a miniUSB connection to a PC that can also power
    the board.

-   **BOOT switch** can be used to force a boot from the microSD card if
    the power is cycled on the board, removing power and reapplying the
    power to the board..

-   There are four blue **LED**S that can be used by the user.

-   **Reset Button** allows the user to reset the processor.

-   **microSD** slot is where a microSD card can be installed.

-   **microHDMI** connector is where the display is connected to.

-   **USB Host** can be connected different USB interfaces such as
    Wi-Fi, BT, Keyboard, etc.

#### 4.3.2 Key Components 

**Figure 18** below shows the locations of the key components on the PCB
layout of the board.

![](docs/media/image29.jpg){width="5.993055555555555in"
height="4.346527777777778in"}

####### Figure 18. Key Components 

-   **Sitara AM3358BZCZ100** is the processor for the board.

-   **Micron 512MB DDR3L** or **Kingston 512mB DDR3** is the Dual Data
    Rate RAM memory.

-   **TPS65217C PMIC** provides the power rails to the various
    components on the board.

-   **SMSC Ethernet PHY** is the physical interface to the network.

-   **Micron eMMC** is an onboard MMC chip that holds up to 4GB of data.

-   **HDMI** Framer provides control for an HDMI or DVI-D display with
    an adapter.

**5.0 BeagleBone Black High Level Specification **
==================================================

This section provides the high level specification of the BeagleBone
Black.

### 5.1 Block Diagram 

**Figure 19** below is the high level block diagram of the BeagleBone
Black.

![](docs/media/image30.jpg){width="5.341666666666667in"
height="4.738194444444445in"}

> **Figure 19. BeagleBone Black Key Components **

### 5.2 Processor 

The revision B board has moved to the Sitara AM3358BZCZ100 device.

### 5.3 Memory 

Described in the following sections are the three memory devices found
on the board.

#### 5.3.1 512MB DDR3L 

A single 256Mb x16 DDR3L 4Gb (512MB) memory device is used. The memory
used is is one of two devices:

-   MT41K256M16HA-125 from Micron

-   D2516EC4BXGGB from Kingston

It will operate at a clock frequency of 400MHz yielding an effective
rate of 800MHZ on the DDR3L bus allowing for 1.6GB/S of DDR3L memory
bandwidth.

#### 5.3.2 4KB EEPROM 

A single 4KB EEPROM is provided on I2C0 that holds the board
information. This information includes board name, serial number, and
revision information. This is the not the same as the one used on the
original BeagleBone. The device was changed for cost reduction reasons.
It has a test point to allow the device to be programmed and otherwise
to provide write protection when not grounded.

#### 5.3.3 4GB Embedded MMC 

A single 4GB embedded MMC (eMMC) device is on the board. The device
connects to the MMC1 port of the processor, allowing for 8bit wide
access. Default boot mode for the board will be MMC1 with an option to
change it to MMC0, the SD card slot, for booting from the SD card as a
result of removing and reapplying the power to the board. Simply
pressing the reset button will not change the boot mode. MMC0 cannot be
used in 8Bit mode because the lower data pins are located on the pins
used by the Ethernet port. This does not interfere with SD card
operation but it does make it unsuitable for use as an eMMC port if the
8 bit feature is needed.

#### 5.3.4 MicroSD Connector 

The board is equipped with a single microSD connector to act as the
secondary boot source for the board and, if selected as such, can be the
primary boot source. The connector will support larger capacity microSD
cards. The microSD card is not provided with the board. Booting from
MMC0 will be used to flash the eMMC in the production environment or can
be used by the user to update the SW as needed.

#### 5.3.5 Boot Modes 

As mentioned earlier, there are four boot modes:

-   **eMMC Boot…**This is the default boot mode and will allow for the
    fastest boot time and will enable the board to boot out of the box
    using the pre-flashed OS image without having to purchase an microSD
    card or an microSD card writer.

-   **SD Boot…**This mode will boot from the microSD slot. This mode can
    be used to override what is on the eMMC device and can be used to
    program the eMMC when used in the manufacturing process or for field
    updates.

-   **Serial Boot…**This mode will use the serial port to allow
    downloading of the software direct. A separate USB to serial cable
    is required to use this port.

-   **USB Boot…**This mode supports booting over the USB port.

***Software to support USB and serial boot modes is not provided by
beagleboard.org.* *Please contact TI for support of this feature.* **

A switch is provided to allow switching between the modes.

-   Holding the boot switch down during a removal and reapplication of
    power without a microSD card inserted will force the boot source to
    be the USB port and if nothing is detected on the USB client port,
    it will go to the serial port for download.

-   Without holding the switch, the board will boot try to boot from the
    eMMC. If it is empty, then it will try booting from the microSD
    slot, followed by the serial port, and then the USB port.

-   If you hold the boot switch down during the removal and
    reapplication of power to the board, and you have a microSD card
    inserted with a bootable image, the board will boot from the microSD
    card.

***NOTE: Pressing the RESET button on the board will NOT result in a
change of the* *boot mode. You MUST remove power and reapply power to
change the boot mode.* *The boot pins are sampled during power on reset
from the PMIC to the processor.* *The reset button on the board is a
warm reset only and will not force a boot mode* *change.* **

### 5.4 Power Management 

The **TPS65217C** power management device is used along with a separate
LDO to provide power to the system. The **TPS65217C** version provides
for the proper voltages required for the DDR3L. This is the same device
as used on the original BeagleBone with the exception of the power rail
configuration settings which will be changed in the internal EEPROM to
the **TPS65217C** to support the new voltages.

DDR3L requires 1.5V instead of 1.8V on the DDR2 as is the case on the
original BeagleBone. The 1.8V regulator setting has been changed to 1.5V
for the DDR3L. The LDO3 3.3V rail has been changed to 1.8V to support
those rails on the processor. LDO4 is still 3.3V for the 3.3V rails on
the processor. An external **LDOTLV70233** provides the 3.3V rail for
the rest of the board.

### 5.5 PC USB Interface 

The board has a miniUSB connector that connects the USB0 port to the
processor. This is the same connector as used on the original
BeagleBone.

### 5.6 Serial Debug Port 

Serial debug is provided via UART0 on the processor via a single 1x6 pin
header. In order to use the interface a USB to TTL adapter will be
required. The header is compatible with the one provided by FTDI and can
be purchased for about \$12 to \$20 from various sources. Signals
supported are TX and RX. None of the handshake signals are supported.

### 5.7 USB1 Host Port 

On the board is a single USB Type A female connector with full LS/FS/HS
Host support that connects to USB1 on the processor. The port can
provide power on/off control and up to 500mA of current at 5V. Under USB
power, the board will not be able to supply the full 500mA, but should
be sufficient to supply enough current for a lower power USB device
supplying power between 50 to 100mA.

You can use a wireless keyboard/mouse configuration or you can add a HUB
for standard keyboard and mouse interfacing.

### 5.8 Power Sources 

The board can be powered from four different sources:

-   A USB port on a PC

-   A 5VDC 1A power supply plugged into the DC connector.

-   A power supply with a USB connector.

-   Expansion connectors

The USB cable is shipped with each board. This port is limited to 500mA
by the Power Management IC. It is possible to change the settings in the
**TPS65217C** to increase this current, but only after the initial boot.
And, at that point the PC most likely will complain, but you can also
use a dual connector USB cable to the PC to get to 1A.

The power supply is not provided with the board but can be easily
obtained from numerous sources. A 1A supply is sufficient to power the
board, but if there is a cape plugged into the board or you have a power
hungry device or hub plugged into the host port, then more current may
needed from the DC supply.

Power routed to the board via the expansion header could be provided
from power derived on a cape. The DC supply should be well regulated and
5V +/-.25V.

### 5.9 Reset Button 

When pressed and released, causes a reset of the board. The reset button
used on the BeagleBone Black is a little larger than the one used on the
original BeagleBone. It has also been moved out to the edge of the board
so that it is more accessible.

### 5.10 Power Button 

A power button is provided near the reset button close to the Ethernet
connector. This button takes advantage of the input to the PMIC for
power down features. While a lot of capes have a button, it was decided
to add this feature to the board to ensure everyone had access to some
new features. These features include:

-   Interrupt is sent to the processor to facilitate an orderly shutdown
    to save files and to un-mount drives.

-   Provides ability to let processor put board into a sleep mode to
    save power.

-   Can alert processor to wake up from sleep mode and restore state
    before sleep was entered.

If you hold the button down longer than 8 seconds, the board will power
off if you release the button when the power LED turns off. If you
continue to hold it, the board will power back up completing a power
cycle.

****We recommend that you use this method to power down the board. It
will also help prevent contamination of the SD card or the eMMC. ****

If you do not remove the power jack, you can press the button again and
the board will power up.

### 5.11 Indicators 

There are a total of five blue LEDs on the board.

-   One blue power LED indicates that power is applied and the power
    management IC is up. If this LED flashes when applying power, it
    means that an excess current flow was detected and the PMIC has shut
    down.

-   Four blue LEDs that can be controlled via the SW by setting GPIO
    pins.

In addition, there are two LEDs on the RJ45 to provide Ethernet status
indication. One is yellow (100M Link up if on) and the other is green
(Indicating traffic when flashing).

### 5.12 CTI JTAG Header 

A place for an optional 20 pin CTI JTAG header is provided on the board
to facilitate the SW development and debugging of the board by using
various JTAG emulators. This header is not supplied standard on the
board. To use this, a connector will need to be soldered onto the board.

If you need the JTAG connector you can solder it on yourself. No other
components are needed. The connector is made by Samtec and the part
number is FTR-110-03-G-D-06. You can purchase it from
[*www.digikey.com*.](http://www.digikey.com/)

### 5.13 HDMI Interface 

A single HDMI interface is connected to the 16 bit LCD interface on the
processor. The 16b interface was used to preserve as many expansion pins
as possible to allow for use by the user. The NXP TDA19988BHN is used to
convert the LCD interface to HDMI and convert the audio as well. The
signals are still connected to the expansion headers to enable the use
of LCD expansion boards or access to other functions on the board as
needed.

The HDMI device does not support HDCP copy protection. Support is
provided via EDID to allow the SW to identify the compatible
resolutions. Currently the following resolutions are supported via the
software:

-   1280 x 1024

-   1440 x 900  1024 x 768

-   1280 x 720

### 5.14 Cape Board Support 

The BeagleBone Black has the ability to accept up to four expansion
boards or capes that can be stacked onto the expansion headers. The word
cape comes from the shape of the board as it is fitted around the
Ethernet connector on the main board. This notch acts as a key to ensure
proper orientation of the cape.

The majority of capes designed for the original BeagleBone will work on
the BeagleBone Black. The two main expansion headers will be populated
on the board. There are a few exceptions where certain capabilities may
not be present or are limited to the BeagleBone Black. These include:

-   GPMC bus may NOT be available due to the use of those signals by the
    eMMC. If the eMMC is used for booting only and the file system is on
    the microSD card, then these signals could be used.

-   Another option is to use the microSD or serial boot modes and not
    use the eMMC.

-   The power expansion header is not on the BeagleBone Black so those
    functions are not supported.

For more information on cape support refer to *Section 9.0*.

**6.0 Detailed Hardware Design **
=================================

This section provides a detailed description of the Hardware design.
This can be useful for interfacing, writing drivers, or using it to help
modify specifics of your own design.

**Figure 20** below is the high level block diagram of the board. For
those who may be concerned, **Figure 20** is the same figure as **Figure
19** back on page 31**.** It is placed here again for convenience so it
is closer to the topics to follow.

![](docs/media/image30.jpg){width="5.341666666666667in"
height="4.738194444444445in"}

> **Figure 20. BeagleBone Black Block Diagram **

### 6.1 Power Section 

**Figure 21** is the high level block diagram of the power section of
the board.

![](docs/media/image31.png){width="4.347305336832896in"
height="2.8976673228346455in"}

###### Figure 21. High Level Power Block Diagram 

This section describes the power section of the design and all the
functions performed by the **TPS65217C**.

#### 6.1.1 TPS65217C PMIC 

The main Power Management IC (PMIC) in the system is the **TPS65217C**
which is a single chip power management IC consisting of a linear
dual-input power path, three step-down converters, and four LDOs. LDO
stands for Low Drop Out. If you want to know more about an LDO, you can
go to
[*http://en.wikipedia.org/wiki/Low-*](http://en.wikipedia.org/wiki/Low-dropout_regulator)

[*dropout\_regulator*.](http://en.wikipedia.org/wiki/Low-dropout_regulator)
If you want to learn more about step-down converters, you can go to
[*http://en.wikipedia.org/wiki/DC-to-DC\_converter*
](http://en.wikipedia.org/wiki/DC-to-DC_converter)

The system is supplied by a USB port or DC adapter. Three
high-efficiency 2.25MHz step-down converters are targeted at providing
the core voltage, MPU, and memory voltage for the board.

The step-down converters enter a low power mode at light load for
maximum efficiency across the widest possible range of load currents.
For low-noise applications the devices can be forced into fixed
frequency PWM using the I2C interface. The step-down converters allow
the use of small inductors and capacitors to achieve a small footprint
solution size.

LDO1 and LDO2 are intended to support system standby mode. In normal
operation, they can support up to 100mA each. LDO3 and LDO4 can support
up to 285mA each.

By default only LDO1 is always ON but any rail can be configured to
remain up in SLEEP state. In particular the DCDC converters can remain
up in a low-power PFM mode to support processor suspend mode. The
**TPS65217C** offers flexible power-up and power-down sequencing and
several house-keeping functions such as power-good output, pushbutton
monitor, hardware reset function and temperature sensor to protect the
battery.

For more information on the **TPS65217C**, refer to
[*http://www.ti.com/product/tps65217C*.](http://www.ti.com/product/tps65217C)

> **Figure 22** is the high level block diagram of the **TPS65217C**.

![](docs/media/image37.png){width="5.733333333333333in" height="6.56in"}

###### Figure 22. TPS65217C Block Diagram 

#### 6.1.2 DC Input 

**Figure 23** below shows how the DC input is connected to the
**TPS65217C**.

> ![](docs/media/image38.png){width="4.78in" height="4.25in"}

###### Figure 23. TPS65217 DC Connection 

A 5VDC supply can be used to provide power to the board. The power
supply current depends on how many and what type of add-on boards are
connected to the board. For typical use, a 5VDC supply rated at 1A
should be sufficient. If heavier use of the expansion headers or USB
host port is expected, then a higher current supply will be required.

The connector used is a 2.1MM center positive x 5.5mm outer barrel. The
5VDC rail is connected to the expansion header. It is possible to power
the board via the expansion headers from an add-on card. The 5VDC is
also available for use by the add-on cards when the power is supplied by
the 5VDC jack on the board.

#### 6.1.3 USB Power 

The board can also be powered from the USB port. A typical USB port is
limited to 500mA max. When powering from the USB port, the VDD\_5V rail
is not provided to the expansion headers, so capes that require the 5V
rail to supply the cape direct, bypassing the **TPS65217C**, will not
have that rail available for use. The 5VDC supply from the USB port is
provided on the SYS\_5V, the one that comes from the **TPS65217C**, rail
of the expansion header for use by a cape. **Figure 24** is the
connection of the USB power input on the PMIC.

###### Figure 24. USB Power Connections 

#### 6.1.4 Power Selection 

The selection of either the 5VDC or the USB as the power source is
handled internally to the **TPS65217C** and automatically switches to
5VDC power if both are connected. SW can change the power configuration
via the I2C interface from the processor. In addition, the SW can read
the **TPS65217C** and determine if the board is running on the 5VDC
input or the USB input. This can be beneficial to know the capability of
the board to supply current for things like operating frequency and
expansion cards.

It is possible to power the board from the USB input and then connect
the DC power supply. The board will switch over automatically to the DC
input.

#### 6.1.5 Power Button 

A power button is connected to the input of the **TPS65217C**. This is a
momentary switch, the same type of switch used for reset and boot
selection on the board.

If you push the button the **TPS65217C** will send an interrupt to the
processor. It is up to the processor to then pull the
**PMIC\_POWER\_EN** pin low at the correct time to power down the board.
At this point, the PMIC is still active, assuming that the power input
was not removed. Pressing the power button will cause the board to power
up again if the processor puts the board in the power off mode.

In power off mode, the RTC rail is still active, keeping the RTC powered
and running off the main power input. If you remove that power, then the
RTC will not be powered. You also have the option of using the battery
holes on the board to connect a battery if desired as discussed in the
next section.

If you push and hold the button for greater than 8 seconds, the PMIC
will power down. But you must release the button when the power LED
turns off. Holding the button past that point will cause the board to
power cycle.

#### 6.1.6 Battery Access Pads 

Four pads are provided on the board to allow access to the battery pins
on the **TPS65217C**. The pads can be loaded with a 4x4 header or you
may just wire a battery into the pads. In addition they could provide
access via a cape if desired. The four signals are listed below in
**Table 3**.

######  Table 3. BeagleBone Black Battery Pins 

  **PIN **       **DESIGNATION **   **FUNCTION **
  -------------- ------------------ ------------------------------------------------------------------------------------
  **BAT **       TP5                > Battery connection point.
  > **SENSE **   TP6                > Battery voltage sense input, connect to BAT directly at the battery terminal.
  **TS **        TP7                > Temperature sense input. Connect to NTC thermistor to sense battery temperature.
  **GND **       TP8                > System ground.

There is no fuel gauge function provided by the **TPS65217C**. That
would need to be added if that function was required. If you want to add
a fuel gauge, and option is to use 1-wire SPI or I2C device. You will
need to add this using the expansion headers and place it on an
expansion board.

  ---------------------------------------------------
  ***NOTE: Refer to the TPS65217C documentation ***
  
  ***before connecting anything to these pins. ***
  ---------------------------------------------------

#### 6.1.7 Power Consumption 

The power consumption of the board varies based on power scenarios and
the board boot processes. Measurements were taken with the board in the
following configuration:

-   DC powered and USB powered

-   HDMI monitor connected

-   USB HUB

-   4GB Thumbdrive

-   Ethernet connected @ 100M

-   Serial debug cable connected

**Table 4** is an analysis of the power consumption of the board in
these various scenarios.

######  Table 4. BeagleBone Black Power Consumption(mA@5V) 

  **MODE **                          **USB **   **DC **   **DC+USB **
  ---------------------------------- ---------- --------- -------------
  **Reset **                         TBD        TBD       TBD
  **Idling @ UBoot **                210        210       210
  **Kernel Booting (Peak) **         460        460       460
  **Kernel Idling **                 350        350       350
  **Kernel Idling Display Blank **   280        280       280
  **Loading a Webpage **             430        430       430

The current will fluctuate as various activates occur, such as the LEDs
on and microSD/eMMC accesses.

#### 6.1.8 Processor Interfaces 

The processor interacts with the **TPS65217C** via several different
signals. Each of these signals is described below.

######  *6.1.8.1 I2C0 *

I2C0 is the control interface between the processor and the
**TPS65217C**. It allows the processor to control the registers inside
the **TPS65217C** for such things as voltage scaling and switching of
the input rails.

######  *6.1.8.2 PMC\_POWR\_EN *

On power up the **VDD\_RTC** rail activates first. After the RTC
circuitry in the processor has activated it instructs the **TPS65217C**
to initiate a full power up cycle by activating the **PMIC\_POWR\_EN**
signal by taking it HI. When powering down, the processor can take this
pin low to start the power down process.

######  *6.1.8.3 LDO\_GOOD *

This signal connects to the **RTC\_PORZn** signal, RTC power on reset.
The small “**n**” indicates that the signal is an active low signal.
Word processors seem to be unable to put a bar over a word so the **n**
is commonly used in electronics. As the RTC circuitry comes up first,
this signal indicates that the LDOs, the 1.8V VRTC rail, is up and
stable. This starts the power up process.

######  *6.1.8.4 PMIC\_PGOOD *

Once all the rails are up, the **PMIC\_PGOOD** signal goes high. This
releases the **PORZn** signal on the processor which was holding the
processor reset.

######  *6.1.8.5 WAKEUP *

The WAKEUP signal from the **TPS65217C** is connected to the
**EXT\_WAKEUP** signal on the processor. This is used to wake up the
processor when it is in a sleep mode. When an event is detected by the
**TPS65217C,** such as the power button being pressed**,** it generates
this signal.

######  *6.1.8.6 PMIC\_INT *

The **PMIC\_INT** signal is an interrupt signal to the processor.
Pressing the power button will send an interrupt to the processor
allowing it to implement a power down mode in an orderly fashion, go
into sleep mode, or cause it to wake up from a sleep mode. All of these
require SW support.

#### 6.1.9 Power Rails 

**Figure 25** shows the connections of each of the rails from the
**TPS65217C**.

![](docs/media/image39.jpg){width="5.858333333333333in"
height="5.26875in"}

####### Figure 25. Power Rails 

########  *6.1.9.1 VRTC Rail *

The **VRTC** rail is a 1.8V rail that is the first rail to come up in
the power sequencing. It provides power to the RTC domain on the
processor and the I/O rail of the **TPS65217C**. It can deliver up to
250mA maximum.

########  *6.1.9.2 VDD\_3V3A Rail *

The **VDD\_3V3A** rail is supplied by the **TPS65217C** and provides the
3.3V for the processor rails and can provide up to 400mA.

########  *6.1.9.3 VDD\_3V3B Rail *

The current supplied by the **VDD\_3V3A** rail is not sufficient to
power all of the 3.3V rails on the board. So a second LDO is supplied,
U4, a **TL5209A**, which sources the **VDD\_3V3B** rail. It is powered
up just after the **VDD\_3V3A** rail.

########  *6.1.9.4 VDD\_1V8 Rail *

The **VDD\_1V8** rail can deliver up to 400mA and provides the power
required for the 1.8V rails on the processor and the HDMI framer. This
rail is not accessible for use anywhere else on the board.

########  *6.1.9.5 VDD\_CORE Rail *

The **VDD\_CORE** rail can deliver up to 1.2A at 1.1V. This rail is not
accessible for use anywhere else on the board and connects only to the
processor. This rail is fixed at 1.1V and should not be adjusted by SW
using the PMIC. If you do, then the processor will no longer work.

########  *6.1.9.6 VDD\_MPU Rail *

The **VDD\_MPU** rail can deliver up to 1.2A. This rail is not
accessible for use anywhere else on the board and connects only to the
processor. This rail defaults to 1.1V and can be scaled up to allow for
higher frequency operation. Changing of the voltage is set via the I2C
interface from the processor.

########  *6.1.9.7 VDDS\_DDR Rail *

The **VDDS\_DDR** rail defaults to **1.5V** to support the DDR3L rails
and can deliver up to 1.2A. It is possible to adjust this voltage rail
down to **1.35V** for lower power operation of the DDR3L device. Only
DDR3L devices can support this voltage setting of 1.35V.

########  *6.1.9.8 Power Sequencing *

The power up process is consists of several stages and events. **Figure
26** describes the events that make up the power up process for the
processer from the PMIC. This diagram is used elsewhere to convey
additional information. I saw no need to bust it up into smaller
diagrams. It is from the processor datasheet supplied by Texas
Instruments.

![](docs/media/image40.png){width="5.703333333333333in" height="4.14in"}

####### Figure 26. Power Rail Power Up Sequencing 

**Figure 27** the voltage rail sequencing for the **TPS65217C** as it
powers up and the voltages on each rail. The power sequencing starts at
15 and then goes to one. That is the way the **TPS65217C** is
configured. You can refer to the TPS65217C datasheet for more
information.

![](docs/media/image41.png){width="2.3466666666666667in"
height="1.9666666666666666in"}

####### Figure 27. TPS65217C Power Sequencing Timing 

#### 6.1.10 Power LED 

The power LED is a blue LED that will turn on once the **TPS65217C** has
finished the power up procedure. If you ever see the LED flash once,
that means that the **TPS65217C** started the process and encountered an
issue that caused it to shut down. The connection of the LED is shown in
**Figure 25**.

#### 6.1.11 TPS65217C Power Up Process 

**Figure 28** shows the interface between the **TPS65217C** and the
processor. It is a cut from the PDF form of the schematic and reflects
what is on the schematic.

![](docs/media/image42.jpg){width="5.996527777777778in"
height="1.9319444444444445in"}

####### Figure 28. Power Processor Interfaces 

When voltage is applied, DC or USB, the **TPS65217C** connects the power
to the SYS output pin which drives the switchers and LDOs in the
**TPS65217C**.

At power up all switchers and LDOs are off except for the **VRTC LDO**
(1.8V), which provides power to the VRTC rail and controls the
**RTC\_PORZn** input pin to the processor, which starts the power up
process of the processor. Once the RTC rail powers up, the
**RTC\_PORZn** pin, driven by the **LDO\_PGOOD** signal from the
**TPS65217C**, of the processor is released.

Once the **RTC\_PORZn** reset is released, the processor starts the
initialization process. After the RTC stabilizes, the processor launches
the rest of the power up process by activating the **PMIC\_POWER\_EN**
signal that is connected to the **TPS65217C** which starts the
**TPS65217C** power up process.

The **LDO\_PGOOD** signal is provided by the **TPS65217C** to the
processor. As this signal is 1.8V from the **TPS65217C** by virtue of
the **TPS65217C** VIO rail being set to 1.8V, and the **RTC\_PORZ**
signal on the processor is 3.3V, a voltage level shifter, **U4**, is
used. Once the LDOs and switchers are up on the **TPS65217C**, this
signal goes active releasing the processor. The LDOs on the
**TPS65217C** are used to power the VRTC rail on the processor.

#### 6.1.12 Processor Control Interface 

**Figure 28** above shows two interfaces between the processor and the
**TPS65217C** used for control after the power up sequence has
completed.

The first is the **I2C0** bus. This allows the processor to turn on and
off rails and to set the voltage levels of each regulator to supports
such things as voltage scaling.

The second is the interrupt signal. This allows the T**PS65217C** to
alert the processor when there is an event, such as when the power
button is pressed. The interrupt is an open drain output which makes it
easy to interface to 3.3V of the processor.

#### 6.1.13 Low Power Mode Support 

This section covers three general power down modes that are available.
These modes are only described from a Hardware perspective as it relates
to the HW design.

#########  6.1.13.1 RTC Only 

In this mode all rails are turned off except the **VDD\_RTC**. The
processor will need to turn off all the rails to enter this mode. The
**VDD\_RTC** staying on will keep the RTC active and provide for the
wakeup interfaces to be active to respond to a wake up event.

#########  6.1.13.2 RTC Plus DDR 

In this mode all rails are turned off except the **VDD\_RTC** and the
**VDDS\_DDR**, which powers the DDR3L memory. The processor will need to
turn off all the rails to enter this mode. The **VDD\_RTC** staying on
will keep the RTC active and provide for the wakeup interfaces to be
active to respond to a wake up event.

The **VDDS\_DDR** rail to the DDR3L is provided by the 1.5V rail of the
**TPS65217C** and with **VDDS\_DDR** active, the DDR3L can be placed in
a self refresh mode by the processor prior to power down which allows
the memory data to be saved.

Currently, this feature is not included in the standard software
release. The plan is to include it in future releases.

#########  6.1.13.3 Voltage Scaling 

For a mode where the lowest power is possible without going to sleep,
this mode allows the voltage on the ARM processor to be lowered along
with slowing the processor frequency down. The I2C0 bus is used to
control the voltage scaling function in the **TPS65217C**.

### 6.2 Sitara AM3358BZCZ100 Processor 

The board is designed to use the Sitara AM3358BZCZ100 processor in the
15 x 15 package. Earlier revisions of the board used the XM3359AZCZ100
processor.

#### 6.2.1 Description 

**Figure 29** is a high level block diagram of the processor. For more
information on the processor, go to
[*http://www.ti.com/product/am3358*.](http://www.ti.com/product/am3358)

![](docs/media/image43.png){width="5.243333333333333in"
height="5.326666666666667in"}

###### Figure 29. Sitara AM3358BZCZ Block Diagram 

.

#### 6.2.2 High Level Features 

**Table 5** below shows a few of the high level features of the Sitara
processor.

######  Table 5. Processor Features 

  ---------------------------------------------------------------------------------------------------------------------
  > Operating Systems           > Linux, Android, Windows                      MMC/SD                  3
                                                                                                       
                                Embedded CE,QNX,                                                       
                                                                                                       
                                ThreadX                                                                
  ----------------------------- ---------------------------------------------- ----------------------- ----------------
  Standby Power                 7 mW                                           CAN                     2

  ARM CPU                       1 ARM Cortex-A8                                > UART (SCI)            6

  > ARM MHz (Max.)              275,500,600,800,1000                           ADC                     8-ch 12-bit

  ARM MIPS (Max.)               1000,1200,2000                                 PWM (Ch)                3

  Graphics Acceleration         1 3D                                           eCAP                    3

  Other Hardware Acceleration   2 PRU-ICSS,Crypto                              eQEP                    3
                                                                                                       
                                Accelerator                                                            

  > On-Chip L1 Cache            > 64 KB (ARM Cortex-A8)                        RTC                     1

  > On-Chip L2 Cache            256 KB (ARM Cortex-                            I2C                     3
                                                                                                       
                                A8)                                                                    

  Other On-Chip Memory          128 KB                                         McASP                   2

  Display Options               LCD                                            SPI                     2

  General Purpose Memory        1 16-bit (GPMC, NAND flash, NOR Flash, SRAM)   DMA (Ch)                > 64-Ch EDMA

  DRAM                          1 16-bit (LPDDR-400,                           > IO Supply (V)         1.8V(ADC),3.3V
                                                                                                       
                                DDR2-532, DDR3-400)                                                    

  USB Ports                     2                                              Operating               -40 to 90
                                                                                                       
                                                                               Temperature Range (C)   
  ---------------------------------------------------------------------------------------------------------------------

#### 6.2.3 Documentation 

Full documentation for the processor can be found on the TI website at
[*http://www.ti.com/product/am3358*](http://www.ti.com/product/am3358)
for the current processor used on the board. Make sure that you always
use the latest datasheets and Technical Reference Manuals (TRM).

#### 6.2.4 Crystal Circuitry 

**Figure 30** is the crystal circuitry for the AM3358 processor.

> ![](docs/media/image44.png){width="5.943333333333333in"
> height="2.3266666666666667in"}

**Figure 30. Processor Crystals **

#### 6.2.5 Reset Circuitry 

**Figure 31** is the board reset circuitry. The initial power on reset
is generated by the **TPS65217C** power management IC. It also handles
the reset for the Real Time Clock.

The board reset is the SYS\_RESETn signal. This is connected to the
NRESET\_INOUT pin of the processor. This pin can act as an input or an
output. When the reset button is pressed, it sends a warm reset to the
processor and to the system.

On the revision A5D board, a change was made. On power up, the
NRESET\_INOUT signal can act as an output. In this instance it can cause
the SYS\_RESETn line to go high prematurely. In order to prevent this,
the PORZn signal from the TPS65217C is connected to the SYS\_RESETn line
using an open drain buffer. These ensure that the line does not
momentarily go high on power up.

![](docs/media/image45.png){width="5.926667760279965in"
height="3.4766666666666666in"}

###### Figure 31. Board Reset Circuitry 

This change is also in all revisions after A5D.

DDR3L Memory

The BeagleBone Black uses a single MT41K256M16HA-125 512MB DDR3L device
from Micron that interfaces to the processor over 16 data lines, 16
address lines, and 14 control lines. On rev C we added the Kingston
**KE4CN2H5A-A58** device as a source for the DDR3L device**. **

The following sections provide more details on the design.

#### 6.2.6 Memory Device 

The design supports the standard DDR3 and DDR3L x16 devices and is built
using the DDR3L. A single x16 device is used on the board and there is
no support for two x8 devices. The DDR3 devices work at 1.5V and the
DDR3L devices can work down to

1.35V to achieve lower power. The DDR3L comes in a 96-BALL FBGA package
with 0.8 mil pitch. Other standard DDR3 devices can also be supported,
but the DDR3L is the lower power device and was chosen for its ability
to work at 1.5V or 1.35V. The standard frequency that the DDR3L is run
at on the board is 400MHZ.

#### 6.2.7 DDR3L Memory Design 

**Figure 32** is the schematic for the DDR3L memory device. Each of the
groups of signals is described in the following lines.

***Address Lines:*** Provide the row address for ACTIVATE commands, and
the column address and auto pre-charge bit (A10) for READ/WRITE
commands, to select one location out of the memory array in the
respective bank. A10 sampled during a

PRECHARGE command determines whether the PRECHARGE applies to one bank
(A10 LOW, bank selected by BA\[2:0\]) or all banks (A10 HIGH). The
address inputs also provide the op-code during a LOAD MODE command.
Address inputs are referenced to VREFCA. A12/BC\#: When enabled in the
mode register (MR), A12 is sampled during READ and WRITE commands to
determine whether burst chop (on-the-fly) will be performed (HIGH = BL8
or no burst chop, LOW = BC4 burst chop).

***Bank Address Lines:*** BA\[2:0\] define the bank to which an
ACTIVATE, READ, WRITE, or PRECHARGE command is being applied. BA\[2:0\]
define which mode register (MR0, MR1, MR2, or MR3) is loaded during the
LOAD MODE command. BA\[2:0\] are referenced to VREFCA.

***CK and CK\# Lines:*** are differential clock inputs. All address and
control input signals are sampled on the crossing of the positive edge
of CK and the negative edge of CK\#. Output data strobe (DQS, DQS\#) is
referenced to the crossings of CK and CK\#.

***Clock Enable Line:*** CKE enables (registered HIGH) and disables
(registered LOW) internal circuitry and clocks on the DRAM. The specific
circuitry that is enabled/disabled is dependent upon the DDR3 SDRAM
configuration and operating mode. Taking CKE LOW provides PRECHARGE
power-down and SELF REFRESH operations (all banks idle) or active
power-down (row active in any bank). CKE is synchronous for powerdown
entry and exit and for self refresh entry. CKE is asynchronous for self
refresh exit. Input buffers (excluding CK, CK\#, CKE, RESET\#, and ODT)
are disabled during powerdown. Input buffers (excluding CKE and RESET\#)
are disabled during SELF REFRESH. CKE is referenced to VREFCA.

> ![](docs/media/image46.png){width="5.903334426946632in"
> height="5.47in"}

###### Figure 32. DDR3L Memory Design 

***Chip Select Line:*** CS\# enables (registered LOW) and disables
(registered HIGH) the command decoder. All commands are masked when CS\#
is registered HIGH. CS\# provides for external rank selection on systems
with multiple ranks. CS\# is considered part of the command code. CS\#
is referenced to VREFCA.

***Input Data Mask Line:*** DM is an input mask signal for write data.
Input data is masked when DM is sampled HIGH along with the input data
during a write access. Although the DM ball is input-only, the DM
loading is designed to match that of the DQ and DQS balls. DM is
referenced to VREFDQ.

***On-die Termination Line:*** ODT enables (registered HIGH) and
disables (registered LOW) termination resistance internal to the DDR3L
SDRAM. When enabled in normal operation, ODT is only applied to each of
the following balls: DQ\[7:0\], DQS, DQS\#, and DM for the x8;
DQ\[3:0\], DQS, DQS\#, and DM for the x4. The ODT input is ignored if
disabled via the LOAD MODE command. ODT is referenced to VREFCA.

#### 6.2.8 Power Rails 

The **DDR3L** memory device and the DDR3 rails on the processor are
supplied by the **TPS65217C**. Default voltage is 1.5V but can be scaled
down to 1.35V if desired.

#### 6.2.9 VREF 

The **VREF** signal is generated from a voltage divider on the
**VDDS\_DDR** rail that powers the processor DDR rail and the DDR3L
device itself. **Figure 33** below shows the configuration of this
signal and the connection to the DDR3L memory device and the processor.

> ![](docs/media/image47.jpg){width="3.9166666666666665in"
> height="2.8020833333333335in"}

**Figure 33. DDR3L VREF Design **

### 6.3 4GB eMMC Memory 

The eMMC is a communication and mass data storage device that includes a
Multi-

MediaCard (MMC) interface, a NAND Flash component, and a controller on
an advanced 11-signal bus, which is compliant with the MMC system
specification. The nonvolatile eMMC draws no power to maintain stored
data, delivers high performance across a wide range of operating
temperatures, and resists shock and vibration disruption.

One of the issues faced with SD cards is that across the different
brands and even within the same brand, performance can vary. Cards use
different controllers and different memories, all of which can have bad
locations that the controller handles. But the controllers may be
optimized for reads or writes. You never know what you will be getting.
This can lead to varying rates of performance. The eMMC card is a known
controller and when coupled with the 8bit mode, 8 bits of data instead
of 4, you get double the performance which should result in quicker boot
times.

The following sections describe the design and device that is used on
the board to implement this interface.

#### 6.3.1 eMMC Device 

The device used is one of two different devices:

>  Micron **MTFC4GLDEA 0M WT**  Kingston **KE4CN2H5A-A58**

The package is a 153 ball WFBGA device on both devices.

#### 6.3.2 eMMC Circuit Design 

**Figure 34** is the design of the eMMC circuitry. The eMMC device is
connected to the MMC1 port on the processor. MMC0 is still used for the
microSD card as is currently done on the original BeagleBone. The size
of the eMMC supplied is now 4GB.

The device runs at 3.3V both internally and the external I/O rails. The
VCCI is an internal voltage rail to the device. The manufacturer
recommends that a 1uF capacitor be attached to this rail, but a 2.2uF
was chosen to provide a little margin.

Pullup resistors are used to increase the rise time on the signals to
compensate for any capacitance on the board.

![](docs/media/image48.png){width="5.653334426946632in" height="2.34in"}

**Figure 34. eMMC Memory Design **

The pins used by the eMMC1 in the boot mode are listed below in **Table
6**.

######  Table 6. eMMC Boot Pins 

![](docs/media/image49.png){width="5.510001093613298in" height="1.17in"}

For eMMC devices the ROM will only support raw mode. The ROM Code reads
out raw sectors from image or the booting file within the file system
and boots from it. In raw mode the booting image can be located at one
of the four consecutive locations in the main area: offset 0x0 / 0x20000
(128 KB) / 0x40000 (256 KB) / 0x60000 (384 KB). For this reason, a
booting image shall not exceed 128KB in size. However it is possible to
flash a device with an image greater than 128KB starting at one of the
aforementioned locations. Therefore the ROM Code does not check the
image size. The only drawback is that the image will cross the
subsequent image boundary. The raw mode is detected by reading sectors
\#0, \#256, \#512, \#768. The content of these sectors is then verified
for presence of a TOC structure. In the case of a **GP Device**, a
Configuration Header (CH) **must** be located in the first sector
followed by a **GP header**. The CH might be void (only containing a
CHSETTINGS item for which the Valid field is zero).

The ROM only supports the 4-bit mode. After the initial boot, the switch
can be made to 8-bit mode for increasing the overall performance of the
eMMC interface.

### 6.4 Board ID EEPROM 

The BeagleBone is equipped with a single 32Kbit(4KB) 24LC32AT-I/OT
EEPROM to allow the SW to identify the board. **Table 7** below defined
the contents of the EERPOM.

######  Table 7. EEPROM Contents 

  ---------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Name **                   > **Size (bytes) **   **Contents **
  --------------------------- --------------------- -------------------------------------------------------------------------------------------------------------
  **Header **                 **4 **                **0xAA, 0x55, 0x33, EE **

  **Board Name **             **8 **                **Name for board in ASCII: A335BNLT **

  **Version **                **4 **                **Hardware version code for board in ASCII: **
                                                    
                                                    **00A3 for Rev A3, 00A4 for Rev A4, 00A5 for Rev A5, 00A6 for Rev A6,00B0 for Rev B, and 00C0 for Rev C. **

  **Serial Number **          **12 **               **Serial number of the board. This is a 12 character string which is: **
                                                    
                                                    **WWYY4P16nnnn **
                                                    
                                                    **where: WW = 2 digit week of the year of production **
                                                    
                                                    **YY = 2 digit year of production **
                                                    
                                                    > **BBBK = BeagleBone Black nnnn = incrementing board number **

  **Configuration Option **   **32 **               **Codes to show the configuration setup on this board. **
                                                    
                                                    **All FF **

  **RSVD **                   **6 **                **FF FF FF FF FF FF **

  **RSVD **                   **6 **                **FF FF FF FF FF FF **

  **RSVD **                   **6 **                **FF FF FF FF FF FF **

  **Available **              **4018 **             **Available space for other non-volatile codes/data **
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------

**Figure 35** shows the new design on the EEPROM interface**.**

![](docs/media/image50.png){width="4.930001093613298in"
height="2.0233333333333334in"}

###### Figure 35. EEPROM Design Rev A5 

The EEPROM is accessed by the processor using the I2C 0 bus. The **WP**
pin is enabled by default. By grounding the test point, the write
protection is removed.

The first 48 locations should not be written to if you choose to use the
extras storage space in the EEPROM for other purposes. If you do, it
could prevent the board from booting properly as the SW uses this
information to determine how to set up the board.

### 6.5 Micro Secure Digital 

The microSD connector on the board will support a microSD card that can
be used for booting or file storage on the BeagleBone Black.

#### 6.5.1 microSD Design 

**Figure 36** below is the design of the microSD interface on the board.

![](docs/media/image51.png){width="5.73in" height="2.26in"}

####### Figure 36. microSD Design 

The signals **MMC0-3** are the data lines for the transfer of data
between the processor and the microSD connector.

The **MMC0\_CLK** signal clocks the data in and out of the microSD card.

The **MMCO\_CMD** signal indicates that a command versus data is being
sent.

There is no separate card detect pin in the microSD specification. It
uses **MMCO\_DAT3** for that function. However, most microSD connectors
still supply a CD function on the connectors. In the BeagleBone Black
design, this pin is connected to the **MMC0\_SDCD** pin for use by the
processor. You can also change the pin to **GPIO0\_6**, which is able to
wake up the processor from a sleep mode when an microSD card is inserted
into the connector.

Pullup resistors are provided on the signals to increase the rise times
of the signals to overcome PCB capacitance.

Power is provided from the **VDD\_3V3B** rail and a 10uF capacitor is
provided for filtering.

### 6.6 User LEDs 

There are four user LEDs on the BeagleBone Black. These are connected to
GPIO pins on the processor. **Figure 37** shows the interfaces for the
user LEDs.

> ![](docs/media/image52.png){width="5.943333333333333in"
> height="3.03in"}

####### Figure 37. User LEDs 

Resistors R71-R74 were changed to 4.75K on the revision A5B board.

**Table 8** shows the signals used to control the four LEDs from the
processor.

#######  Table 8. User LED Control Signals/Pins 

  **LED **   **GPIO SIGNAL **   **PROC PIN **
  ---------- ------------------ ---------------
  USR0       > GPIO1\_21        V15
  USR1       > GPIO1\_22        U15
  USR2       > GPIO1\_23        T15
  USR3       > GPIO1\_24        V16

A logic level of “1” will cause the LEDs to turn on.

### 6.7 Boot Configuration 

The design supports two groups of boot options on the board. The user
can switch between these modes via the Boot button. The primary boot
source is the onboard eMMC device. By holding the Boot button, the user
can force the board to boot from the microSD slot. This enables the eMMC
to be overwritten when needed or to just boot an alternate image. The
following sections describe how the boot configuration works.

In most applications, including those that use the provided demo
distributions available from
[*beagleboard.org*,](http://beagleboard.org/) the processor-external
boot code is composed of two stages. After the primary boot code in the
processor ROM passes control, a secondary stage (secondary program
loader -- "SPL" or "MLO") takes over. The SPL stage initializes only the
required devices to continue the boot process, and then control is
transferred to the third stage "U-boot". Based on the settings of the
boot pins, the ROM knows where to go and get the SPL and UBoot code. In
the case of the BeagleBone Black, that is either eMMC or microSD based
on the position of the boot switch.

#### 6.7.1 Boot Configuration Design 

**Figure 38** shows the circuitry that is involved in the boot
configuration process. On power up, these pins are read by the processor
to determine the boot order. S2 is used to change the level of one bit
from HI to LO which changes the boot order.

> ![](docs/media/image53.png){width="4.673333333333333in"
> height="3.83in"}

####### Figure 38. Processor Boot Configuration Design 

It is possible to override these setting via the expansion headers. But
be careful not to add too much load such that it could interfere with
the operation of the HDMI interface or LCD panels. If you choose to
override these settings, it is strongly recommended that you gate these
signals with the **SYS\_RESETn** signal. This ensures that after coming
out of reset these signals are removed from the expansion pins.

### 6.8 Default Boot Options 

Based on the selected option found in **Figure 39** below, each of the
boot sequences for each of the two settings is shown.

![](docs/media/image54.jpg){width="6.260543525809274in"
height="1.3582666229221347in"}

####### Figure 39. Processor Boot Configuration 

The first row in **Figure 39** is the default setting. On boot, the
processor will look for the eMMC on the MMC1 port first, followed by the
microSD slot on MMC0, USB0 and UART0. In the event there is no microSD
card and the eMMC is empty, UART0 or USB0 could be used as the board
source.

If you have a microSD card from which you need to boot from, hold the
boot button down. On boot, the processor will look for the SPIO0 port
first, then microSD on the MMC0 port, followed by USB0 and UART0. In the
event there is no microSD card and the eMMC is empty, USB0 or UART0
could be used as the board source.

### 6.9 10/100 Ethernet 

The BeagleBone Black is equipped with a 10/100 Ethernet interface. It
uses the same PHY as is used on the original BeagleBone. The design is
described in the following sections.

#### 6.9.1 Ethernet Processor Interface 

**Figure 40** shows the connections between the processor and the PHY.
The interface is in the MII mode of operation.

> ![](docs/media/image55.png){width="4.676667760279965in"
> height="3.25in"}

####### Figure 40. Ethernet Processor Interface 

This is the same interface as is used on the BeagleBone. No changes were
made in this design for the board.

#### 6.9.2 Ethernet Connector Interface 

The off board side of the PHY connections are shown in **Figure 41**
below.

![](docs/media/image56.png){width="5.943334426946632in"
height="3.6166666666666667in"}

####### Figure 41. Ethernet Connector Interface 

This is the same interface as is used on the BeagleBone. No changes were
made in this design for the board.

#### 6.9.3 Ethernet PHY Power, Reset, and Clocks 

**Figure 42** shows the power, reset, and lock connections to the
**LAN8710A** PHY. Each of these areas is discussed in more detail in the
following sections.

> ![](docs/media/image57.png){width="5.940001093613298in"
> height="3.8266666666666667in"}

####### Figure 42. Ethernet PHY, Power, Reset, and Clocks 

########  *6.9.3.1 VDD\_3V3B Rail *

The VDD\_3V3B rail is the main power rail for the **LAN8710A**. It
originates at the VD\_3V3B regulator and is the primary rail that
supports all of the peripherals on the board. This rail also supplies
the VDDIO rails which set the voltage levels for all of the I/O signals
between the processor and the **LAN8710A**.

########  *6.9.3.2 VDD\_PHYA Rail *

A filtered version of VDD\_3V3B rail is connected to the VDD rails of
the LAN8710 and the termination resistors on the Ethernet signals. It is
labeled as **VDD\_PHYA**. The filtering inductor helps block transients
that may be seen on the VDD\_3V3B rail.

########  *6.9.3.3 PHY\_VDDCR Rail *

The **PHY\_VDDCR** rail originates inside the LAN8710A. Filter and
bypass capacitors are used to filter the rail. Only circuitry inside the
LAN8710A uses this rail.

#######  *6.9.3.4 SYS\_RESET *

The reset of the LAN8710A is controlled via the **SYS\_RESETn** signal,
the main board reset line.

########  *6.9.3.5 Clock Signals *

A crystal is used to create the clock for the LAN8710A. The processor
uses the **RMII\_RXCLK** signal to provide the clocking for the data
between the processor and the LAN8710A.

#### 6.9.4 LAN8710A Mode Pins 

There are mode pins on the LAN8710A that sets the operational mode for
the PHY when coming out of reset. These signals are also used to
communicate between the processor and the LAN8710A. As a result, these
signals can be driven by the processor which can cause the PHY not to be
initialized correctly. To ensure that this does not happen, three low
value pull up resistors are used. **Figure 43** below shows the three
mode pin resistors.

> **Figure 43. Ethernet PHY Mode Pins **

This will set the mode to be 111, which enables all modes and enables
auto-negotiation.

### 6.10 HDMI Interface 

The BeagleBone Black has an onboard HDMI framer that converts the LCD
signals and audio signals to drive a HDMI monitor. The design uses an
NXP **TDA19988** HDMI Framer.

The following sections provide more detail into the design of this
interface.

#### 6.10.1 Supported Resolutions 

The maximum resolution supported by the BeagleBone Black is 1280x1024 @
60Hz. **Table 9** below shows the supported resolutions. Not all
resolutions may work on all monitors, but these have been tested and
shown to work on at least one monitor. EDID is supported on the
BeagleBone Black. Based on the EDID reading from the connected monitor,
the highest compatible resolution is selected.

#######  Table 9. HDMI Supported Monitor Resolutions 

  RESOLUTION            AUDIO
  --------------------- ------- --
  > 800 x 600 @60Hz             
  > 800 x 600 @56Hz             
  > 640 x 480 @75Hz             
  > 640 x 480 @60Hz     YES     
  > 720 x 400 @70Hz             
  > 1280 x 1024 @75Hz           
  > 1024 x 768 @75Hz            
  > 1024 x 768 @70Hz            
  > 1024 x 768 @60Hz            
  > 800 x 600 @75Hz             
  > 800 x 600 @72Hz             
  > 720 x 480 @60Hz     YES     
  > 1280 x 720 @60Hz    YES     
  > 1920x1080@24Hz      YES     

NOTE: The updated software image used on the Rev A5B board added support
for 1920x1080@24HZ.

Audio is limited to CEA supported resolutions. LCD panels only activate
the audio in CEA modes. This is a function of the specification and is
not something that can be fixed on the board via a hardware change or a
software change.

#### 6.10.2 HDMI Framer 

The **TDA19988** is a High-Definition Multimedia Interface (HDMI) 1.4a
transmitter. It is backward compatible with DVI 1.0 and can be connected
to any DVI 1.0 or HDMI sink. The HDCP mode is not used in the design.
The non-HDCP version of the device is used in the BeagleBone Black
design.

This device provides additional embedded features like CEC (Consumer
Electronic Control). CEC is a single bidirectional bus that transmits
CEC over the home appliance network connected through this bus. This
eliminates the need of any additional device to handle this feature.
While this feature is supported in this device, as of this point, the SW
to support this feature has not been implemented and is not a feature
that is considered critical. It can be switched to very low power
Standby or Sleep modes to save power when HDMI is not used. **TDA19988**
embeds I~2~C-bus master interface for DDC-bus communication to read
EDID. This device can be controlled or configured via I~2~C-bus
interface.

#### 6.10.3 HDMI Video Processor Interface 

The **Figure 44** shows the connections between the processor and the
HDMI framer device. There are 16 bits of display data, 5-6-5 that is
used to drive the framer. The reason for 16 bits is that allows for
compatibility with display and LCD capes already available on the
original BeagleBone. The unused bits on the **TDA19988** are tied low.
In addition to the data signals are the VSYNC, HSYNC, DE, and PCLK
signals that round out the video interface from the processor.

> ![](docs/media/image58.png){width="4.683333333333334in"
> height="5.013334426946631in"}

####### Figure 44. HDMI Framer Processor Interface 

#### 6.10.4 HDMI Control Processor Interface 

In order to use the **TDA19988**, the processor needs to setup the
device. This is done via the I2C interface between the processor and the
**TDA19988**. There are two signals on the **TDA19988** that could be
used to set the address of the **TDA19988**. In this design they are
both tied low. The I2C interface supports both 400kHz and 100KhZ
operation. **Table 10** shows the I2C address.

#######  Table 10. TDA19988 I2C Address 

![](docs/media/image59.png){width="5.9600010936132986in"
height="0.7533344269466317in"}

#### 6.10.5 Interrupt Signal 

There is a HDMI\_INT signal that connects from the TDA19988 to the
processor. This signal can be used to alert the processor in a state
change on the HDMI interface.

#### 6.10.6 Audio Interface 

There is an I2S audio interface between the processor and the
**TDA19988**. Stereo audio can be transported over the HDMI interface to
an audio equipped display. In order to create the required clock
frequencies, and external 24.576MHz oscillator, **Y4**, is used. From
this clock, the processor generates the required clock frequencies for
the **TDA19988**.

There are three signals used to pass data from the processor to the
**TDA19988**. SCLK is the serial clock. SPI1\_CS0 is the data pin to the
**TDA199888**. SPI1\_D0 is the word sync pin. These signals are
configured as I2S interfaces.

Audio is limited to CEA supported resolutions. LCD panels only activate
the audio in CEA modes. This is a function of the specification and is
not something that can be fixed on the board via a hardware change or a
software change.

In order to create the correct clock frequencies, we had to add an
external **24.576MHZ** oscillator. Unfortunately this had to be input
into the processor using the pin previously used for **GPIO3\_21**. In
order to keep GPIO3\_21 functionality, we provided a way to disable the
oscillator if the need was there to use the pin on the expansion header.
**Figure 45** shows the oscillator circuitry.

![](docs/media/image60.png){width="5.995129046369204in"
height="1.7631616360454943in"}

####### Figure 45. 24.576MHZ Oscillator 

#### 6.10.7 Power Connections 

**Figure 46** shows the power connections to the **TDA19988** device.
All voltage rails for the device are at 1.8V. A filter is provided to
minimize any noise from the 1.8V rail getting back into the device.

> ![](docs/media/image64.png){width="5.730001093613298in"
> height="3.2866666666666666in"}

####### Figure 46. HDMI Power Connections 

All of the interfaces between the processor and the **TDA19988** are
3.3V tolerant allowing for direct connection.

#### 6.10.8 HDMI Connector Interface 

**Figure 47** shows the design of the interface between the HDMI Framer
and the connector.

![](docs/media/image65.png){width="5.4366666666666665in"
height="4.486666666666666in"}

####### Figure 47. Connector Interface Circuitry 

The connector for the HDMI interface is a microHDMI. It should be noted
that this connector has a different pinout than the standard or mini
HDMI connectors. D6 and D7 are ESD protection devices.

### 6.11 USB Host 

The board is equipped with a single USB host interface accessible from a
single USB Type A female connector. **Figure 48** is the design of the
USB Host circuitry.

> ![](docs/media/image66.png){width="5.943334426946632in"
> height="2.1433333333333335in"}

#### 6.11.1 Power Switch 

**U8** is a switch that allows the power to the connector to be turned
on or off by the processor. It also has an over current detection that
can alert the processor if the current gets too high via the
**USB1\_OC** signal. The power is controlled by the **USB1\_DRVBUS**
signal from the processor.

#### 6.11.2 ESD Protection 

**U9** is the ESD protection for the signals that go to the connector.

#### 6.11.3 Filter Options 

**FB7** and **FB8** were added to assist in passing the FCC emissions
test. The **USB1\_VBUS** signal is used by the processor to detect that
the 5V is present on the connector. **FB7** is populated and **FB8** is
replaced with a .1 ohm resistor.

### 6.12 PRU-ICSS 

The PRU-ICSS module is located inside the AM3358 processor. Access to
these pins is provided by the expansion headers and is multiplexed with
other functions on the board. Access is not provided to all of the
available pins.

All documentation is located at
[*http://github.com/beagleboard/am335x\_pru\_package*.](http://github.com/beagleboard/am335x_pru_package)
This feature is not supported by Texas Instruments.

#### 6.12.1 PRU-ICSS Features 

The features of the PRU-ICSS include:

Two independent programmable real-time (PRU) cores:

######## – 32-Bit Load/Store RISC architecture – 8K Byte instruction RAM (2K instructions) per core – 8K Bytes data RAM per core – 12K Bytes shared RAM 

-   Operating frequency of 200 MHz

-   PRU operation is little endian similar to ARM processor

-   All memories within PRU-ICSS support parity

-   Includes Interrupt Controller for system event handling

-   Fast I/O interface

– 16 input pins and 16 output pins per PRU core. (Not all of these are
accessible on the BeagleBone Black).

#### 6.12.2 PRU-ICSS Block Diagram 

**Figure 49** is a high level block diagram of the PRU-ICSS.

![](docs/media/image67.png){width="4.45in"
height="2.8666666666666667in"}

####### Figure 49. PRU-ICSS Block Diagram 

#### 6.12.3 PRU-ICSS Pin Access 

Both PRU 0 and PRU1 are accessible from the expansion headers. Some may
not be useable without first disabling functions on the board like LCD
for example. Listed below is what ports can be accessed on each PRU.

PRU0

-   8 outputs or 9 inputs

PRU1

-   13 outputs or 14 inputs

-   UART0\_TXD, UART0\_RXD, UART0\_CTS, UART0\_RTS

**Table 11** below shows which PRU-ICSS signals can be accessed on the
BeagleBone Black and on which connector and pins they are accessible
from. Some signals are accessible on the same pins.

#######  Table 11. PRU0 and PRU1 Access 

       > **PIN **   > **PROC **   > **NAME **                                                                                                                         
  ---- ------------ ------------- -------------- ------------------------------------------------------ ------------------------------------------------------------- -------------------------------------
  P8   11           R12           > GPIO1\_13                                                           > **pr1\_pru0\_pru\_r30\_15 (Output) **                       
       12           T12           > GPIO1\_12                                                           > **pr1\_pru0\_pru\_r30\_14 (Output) **                       
       15           U13           > GPIO1\_15                                                           **pr1\_pru0\_pru\_r31\_15 (Input) **                          
       16           V13           > GPIO1\_14                                                           **pr1\_pru0\_pru\_r31\_14 (Input) **                          
       20           V9            > GPIO1\_31    > pr1\_pru1\_pru\_r30\_13 (Output)                     pr1\_pru1\_pru\_r31\_13 (INPUT)                               
       21           U9            > GPIO1\_30    > pr1\_pru1\_pru\_r30\_12 (Output)                     pr1\_pru1\_pru\_r31\_12 (INPUT)                               
       27           U5            > GPIO2\_22    > pr1\_pru1\_pru\_r30\_8 (Output)                      pr1\_pru1\_pru\_r31\_8 (INPUT)                                
       28           V5            > GPIO2\_24    > pr1\_pru1\_pru\_r30\_10 (Output)                     pr1\_pru1\_pru\_r31\_10 (INPUT)                               
       29           R5            > GPIO2\_23    > pr1\_pru1\_pru\_r30\_9 (Output)                      pr1\_pru1\_pru\_r31\_9 (INPUT)                                
       39           > T3          > GPIO2\_12    > pr1\_pru1\_pru\_r30\_6 (Output)                      pr1\_pru1\_pru\_r31\_6 (INPUT)                                
       40           > T4          > GPIO2\_13    > pr1\_pru1\_pru\_r30\_7 (Output)                      pr1\_pru1\_pru\_r31\_7 (INPUT)                                
       41           > T1          > GPIO2\_10    > pr1\_pru1\_pru\_r30\_4 (Output)                      pr1\_pru1\_pru\_r31\_4 (INPUT)                                
       42           > T2          > GPIO2\_11    > pr1\_pru1\_pru\_r30\_5 (Output)                      pr1\_pru1\_pru\_r31\_5 (INPUT)                                
       43           R3            GPIO2\_8       > pr1\_pru1\_pru\_r30\_2 (Output)                      pr1\_pru1\_pru\_r31\_2 (INPUT)                                
       44           R4            GPIO2\_9       > pr1\_pru1\_pru\_r30\_3 (Output)                      pr1\_pru1\_pru\_r31\_3 (INPUT)                                
       45           R1            GPIO2\_6       > pr1\_pru1\_pru\_r30\_0 (Output)                      pr1\_pru1\_pru\_r31\_0 (INPUT)                                
       46           R2            GPIO2\_7       > pr1\_pru1\_pru\_r30\_1 (Output)                      pr1\_pru1\_pru\_r31\_1 (INPUT)                                
                                                                                                                                                                      
  P9   17           A16           I2C1\_SCL      pr1\_uart0\_txd                                                                                                      
       18           B16           I2C1\_SDA      > pr1\_uart0\_rxd                                                                                                    
       19           D17           I2C2\_SCL      > pr1\_uart0\_rts\_n                                                                                                 
       20           D18           I2C2\_SDA      > pr1\_uart0\_cts\_n                                                                                                 
       21           B17           > UART2\_TXD   > pr1\_uart0\_rts\_n                                                                                                 
       22           A17           > UART2\_RXD   > pr1\_uart0\_cts\_n                                                                                                 
       24           D15           > UART1\_TXD   pr1\_uart0\_txd                                        **pr1\_pru0\_pru\_r31\_16 (Input) **                          
                    A14           GPIO3\_21\*    **pr1\_pru0\_pru\_r30\_5 (Output) **                   **pr1\_pru0\_pru\_r31\_5((Input) **                           
       26           D16           > UART1\_RXD   pr1\_uart0\_rxd **pr1\_pru0\_pru\_r30\_7 (Output) **   pr1\_pru1\_pru\_r31\_16 **pr1\_pru0\_pru\_r31\_7 (Input) **   
       27           C13           GPIO3\_19                                                                                                                           
       28           C12           SPI1\_CS0      eCAP2\_in\_PWM2\_out                                   > **pr1\_pru0\_pru\_r30\_3 (Output) **                        **pr1\_pru0\_pru\_r31\_3 (Input) **
       29           B13           SPI1\_D0       > **pr1\_pru0\_pru\_r30\_1 (Output) **                 **pr1\_pru0\_pru\_r31\_1 (Input) **                           
       30           D12           SPI1\_D1       > **pr1\_pru0\_pru\_r30\_2 (Output) **                 **pr1\_pru0\_pru\_r31\_2 (Input) **                           
       31           A13           SPI1\_SCLK     > **pr1\_pru0\_pru\_r30\_0 (Output) **                 **pr1\_pru0\_pru\_r31\_0 (Input) **                           

**7.0 Connectors **
===================

This section describes each of the connectors on the board.

### 7.1 Expansion Connectors 

The expansion interface on the board is comprised of two 46 pin
connectors. All signals on the expansion headers are ***3.3V*** unless
otherwise indicated.

***NOTE: Do not connect 5V logic level signals to these pins or the
board will be* *damaged.* **

> **NOTE: DO NOT APPLY VOLTAGE TO ANY I/O PIN WHEN POWER IS NOT SUPPLIED
> TO THE BOARD. IT WILL DAMAGE THE PROCESSOR AND VOID THE WARRANTY. **
>
> **NO PINS ARE TO BE DRIVEN UNTIL AFTER THE SYS\_RESET LINE GOES HIGH.
> **

**Figure 50** shows the location of the expansion connectors.

![](docs/media/image68.jpg){width="2.9819444444444443in"
height="4.111805555555556in"}

###### Figure 50. Expansion Connector Location 

The location and spacing of the expansion headers are the same as on the
original BeagleBone.

#### 7.1.1 Connector P8 

**Table 12** shows the pinout of the **P8** expansion header. Other
signals can be connected to this connector based on setting the pin mux
on the processor, but this is the default settings on power up. The SW
is responsible for setting the default function of each pin. There are
some signals that have not been listed here. Refer to the processor
documentation for more information on these pins and detailed
descriptions of all of the pins listed. In some cases there may not be
enough signals to complete a group of signals that may be required to
implement a total interface.

The **PROC** column is the pin number on the processor.

The **PIN** column is the pin number on the expansion header.

The **MODE** columns are the mode setting for each pin. Setting each
mode to align with the mode column will give that function on that pin.

> **NOTE: DO NOT APPLY VOLTAGE TO ANY I/O PIN WHEN POWER IS NOT SUPPLIED
> TO THE BOARD. IT WILL DAMAGE THE PROCESSOR AND VOID THE WARRANTY. **
>
> **NO PINS ARE TO BE DRIVEN UNTIL AFTER THE SYS\_RESET LINE GOES HIGH.
> **

  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **REF: BBONEBLK\_SRM BeagleBone Black System Rev C.1 **
  
  > **Reference Manual **
  
  **Table 12. Expansion Header P8 Pinout **
  
    > **PIN **   > **PROC **   **NAME **       **MODE0 **            **MODE1 **         **MODE2 **              **MODE3 **              **MODE4 **
    ------------ ------------- --------------- --------------------- ------------------ ----------------------- ----------------------- ----------------------- --------------------------- ------------------------- -------------
    1,2                                                              > **GND **                                                         
    3            R9            GPIO1\_6        gpmc\_ad6             mmc1\_dat6                                                         
    4            T9            GPIO1\_7        gpmc\_ad7             mmc1\_dat7                                                         
    5            R8            GPIO1\_2        gpmc\_ad2             mmc1\_dat2                                                         
    6            T8            GPIO1\_3        gpmc\_ad3             mmc1\_dat3                                                         
    7            R7            TIMER4          > gpmc\_advn\_ale                        timer4                                          
    8            T7            TIMER7          > gpmc\_oen\_ren                         timer7                                          
    9            T6            TIMER5          > gpmc\_be0n\_cle                        timer5                                          
    10           U6            TIMER6          gpmc\_wen                                timer6                                          
    11           R12           GPIO1\_13       gpmc\_ad13            lcd\_data18        mmc1\_dat5              mmc2\_dat1              eQEP2B\_in
    12           T12           GPIO1\_12       gpmc\_ad12            Lcd\_data19        mmc1\_dat4              Mmc2\_dat0              Eqep2a\_in
    13           T10           > EHRPWM2B      gpmc\_ad9             lcd\_data22        mmc1\_dat1              mmc2\_dat5              ehrpwm2B
    14           T11           GPIO0\_26       gpmc\_ad10            lcd\_data21        mmc1\_dat2              mmc2\_dat6              ehrpwm2\_tripzone\_in
    15           U13           GPIO1\_15       gpmc\_ad15            lcd\_data16        mmc1\_dat7              mmc2\_dat3              eQEP2\_strobe
    16           V13           GPIO1\_14       gpmc\_ad14            lcd\_data17        mmc1\_dat6              mmc2\_dat2              eQEP2\_index
    17           U12           GPIO0\_27       gpmc\_ad11            lcd\_data20        mmc1\_dat3              mmc2\_dat7              ehrpwm0\_synco
    18           V12           GPIO2\_1        > gpmc\_clk\_mux0     lcd\_memory\_clk   gpmc\_wait1             mmc2\_clk               
    19           U10           > EHRPWM2A      gpmc\_ad8             lcd\_data23        mmc1\_dat0              mmc2\_dat4              ehrpwm2A
    20           V9            GPIO1\_31       gpmc\_csn2            gpmc\_be1n         mmc1\_cmd                                       
    21           U9            GPIO1\_30       gpmc\_csn1            gpmc\_clk          mmc1\_clk                                       
    22           V8            GPIO1\_5        gpmc\_ad5             mmc1\_dat5                                                         
    23           U8            GPIO1\_4        gpmc\_ad4             mmc1\_dat4                                                         
    24           V7            GPIO1\_1        gpmc\_ad1             mmc1\_dat1                                                         
    25           U7            GPIO1\_0        gpmc\_ad0             mmc1\_dat0                                                         
    26           V6            GPIO1\_29       gpmc\_csn0                                                                               
    27           U5            GPIO2\_22       lcd\_vsync            gpmc\_a8                                                           
    28           V5            GPIO2\_24       lcd\_pclk             gpmc\_a10                                                          
    29           R5            GPIO2\_23       lcd\_hsync            gpmc\_a9                                                           
    30           R6            GPIO2\_25       > lcd\_ac\_bias\_en   gpmc\_a11                                                          
    31           V4            > UART5\_CTSN   lcd\_data14           gpmc\_a18          eQEP1\_index            mcasp0\_axr1            uart5\_rxd
    32           T5            > UART5\_RTSN   lcd\_data15           gpmc\_a19          eQEP1\_strobe           mcasp0\_ahclkx          mcasp0\_axr3
    33           V3            > UART4\_RTSN   lcd\_data13           gpmc\_a17          eQEP1B\_in              mcasp0\_fsr             mcasp0\_axr3
    34           U4            > UART3\_RTSN   lcd\_data11           gpmc\_a15          ehrpwm1B                mcasp0\_ahclkr          mcasp0\_axr2
    35           V2            > UART4\_CTSN   lcd\_data12           gpmc\_a16          eQEP1A\_in              mcasp0\_aclkr           mcasp0\_axr2
    36           U3            > UART3\_CTSN   lcd\_data10           gpmc\_a14          ehrpwm1A                mcasp0\_axr0            
    37           U1            > UART5\_TXD    lcd\_data8            gpmc\_a12          ehrpwm1\_tripzone\_in   mcasp0\_aclkx           uart5\_txd
    38           U2            > UART5\_RXD    lcd\_data9            gpmc\_a13          ehrpwm0\_synco          mcasp0\_fsx             uart5\_rxd
    39           T3            GPIO2\_12       lcd\_data6            gpmc\_a6                                   eQEP2\_index            
    40           T4            GPIO2\_13       lcd\_data7            gpmc\_a7                                   eQEP2\_strobe           pr1\_edio\_data\_out7
    41           T1            GPIO2\_10       lcd\_data4            gpmc\_a4                                   eQEP2A\_in              
    42           T2            GPIO2\_11       lcd\_data5            gpmc\_a5                                   eQEP2B\_in              
    43           R3            GPIO2\_8        lcd\_data2            gpmc\_a2                                   ehrpwm2\_tripzone\_in   
    44           R4            GPIO2\_9        lcd\_data3            gpmc\_a3                                   ehrpwm0\_synco          
    45           R1            GPIO2\_6        lcd\_data0            gpmc\_a0                                   ehrpwm2A                
    46           R2            GPIO2\_7        lcd\_data1            gpmc\_a1                                   ehrpwm2B                
  
  > ![](docs/media/image2.jpg){width="5.873611111111111in" height="0.5in"}
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### 7.1.2 Connector P9 

**Table 13** lists the signals on connector **P9**. Other signals can be
connected to this connector based on setting the pin mux on the
processor, but this is the default settings on power up.

There are some signals that have not been listed here. Refer to the
processor documentation for more information on these pins and detailed
descriptions of all of the pins listed. In some cases there may not be
enough signals to complete a group of signals that may be required to
implement a total interface.

The **PROC** column is the pin number on the processor.

The **PIN** column is the pin number on the expansion header.

The **MODE** columns are the mode setting for each pin. Setting each
mode to align with the mode column will give that function on that pin.

NOTES:

In the table are the following notations:

**PWR\_BUT** is a 5V level as pulled up internally by the TPS65217C. It
is activated by pulling the signal to GND.

\# Both of these signals connect to pin 41 of P11. Resistors are
installed that allow for the GPIO3\_20 connection to be removed by
removing R221. The intent is to allow the SW to use either of these
signals, one or the other, on pin 41. SW should set the unused pin in
input mode when using the other pin. This allowed us to get an extra
signal out to the expansion header.

@ Both of these signals connect to pin 42 of P11. Resistors are
installed that allow for the GPIO3\_18 connection to be removed by
removing R202. The intent is to allow the SW to use either of these
signals, on pin 42. SW should set the unused pin in input mode when
using the other pin. This allowed us to get an extra signal out to the
expansion header.

> **NOTE: DO NOT APPLY VOLTAGE TO ANY I/O PIN WHEN POWER IS NOT SUPPLIED
> TO THE BOARD. IT WILL DAMAGE THE PROCESSOR AND VOID THE WARRANTY. **
>
> **NO PINS ARE TO BE DRIVEN UNTIL AFTER THE SYS\_RESET LINE GOES HIGH.
> **

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Table 13. Expansion Header P9 Pinout **
  
    **PIN **   > **PROC **   **NAME **     **MODE0 **               **MODE1 **            **MODE2 **            **MODE3 **                         **MODE4 **                    **MODE5 **                **MODE6 **
    ---------- ------------- ------------- ------------------------ --------------------- --------------------- ---------------------------------- ----------------------------- ------------------------- -------------------------- ------------------------
    1,2                                                                                                         > GND                                                                                      
    3,4                                                                                                         > DC\_3.3V                                                                                 
    5,6                                                                                                         > VDD\_5V                                                                                  
    7,8                                                                                                         > SYS\_5V                                                                                  
    9                                                                                                           > **PWR\_BUT**                                                                             
    10         A10                                                                                              > SYS\_RESETnRESET\_OUT                                                                    
    11         T17           UART4\_RXD    gpmc\_wait0              mii2\_crs             gpmc\_csn4            rmii2\_crs\_dv                     mmc1\_sdcd                                              uart4\_rxd\_mux2
    12         U18           GPIO1\_28     gpmc\_be1n               mii2\_col             gpmc\_csn6            mmc2\_dat3                         gpmc\_dir                                               mcasp0\_aclkr\_mux3
    13         U17           UART4\_TXD    gpmc\_wpn                mii2\_rxerr           gpmc\_csn5            rmii2\_rxerr                       mmc2\_sdcd                                              uart4\_txd\_mux2
    14         U14           EHRPWM1A      gpmc\_a2                 mii2\_txd3            rgmii2\_td3           mmc2\_dat1                         gpmc\_a18                                               ehrpwm1A\_mux1
    15         R13           GPIO1\_16     gpmc\_a0                 gmii2\_txen           rmii2\_tctl           mii2\_txen                         gpmc\_a16                                               ehrpwm1\_tripzone\_input
    16         T14           EHRPWM1B      gpmc\_a3                 mii2\_txd2            rgmii2\_td2           mmc2\_dat2                         gpmc\_a19                                               ehrpwm1B\_mux1
    17         A16           I2C1\_SCL     spi0\_cs0                mmc2\_sdwp            I2C1\_SCL             ehrpwm0\_synci                     pr1\_uart0\_txd                                         
    18         B16           I2C1\_SDA     > spi0\_d1 uart1\_rtsn   mmc1\_sdwp timer5     I2C1\_SDA dcan0\_rx   > ehrpwm0\_tripzone I2C2\_SCL      > pr1\_uart0\_rxd spi1\_cs1   > pr1\_uart0\_rts\_n      
    19         D17           I2C2\_SCL                                                                                                                                                                     
    20         D18           I2C2\_SDA     uart1\_ctsn              timer6                dcan0\_tx             I2C2\_SDA                          spi1\_cs0                     pr1\_uart0\_cts\_n        
    21         B17           UART2\_TXD    spi0\_d0                 uart2\_txd            I2C2\_SCL             ehrpwm0B                           pr1\_uart0\_rts\_n                                      EMU3\_mux1
    22         A17           UART2\_RXD    spi0\_sclk               uart2\_rxd            I2C2\_SDA             ehrpwm0A                           pr1\_uart0\_cts\_n                                      EMU2\_mux1
    23         V14           GPIO1\_17     gpmc\_a1                 gmii2\_rxdv           rgmii2\_rxdv          mmc2\_dat0                         gpmc\_a17                                               ehrpwm0\_synco
    24         D15           UART1\_TXD    uart1\_txd               mmc2\_sdwp            dcan1\_rx             I2C1\_SCL                                                        pr1\_uart0\_txd           pr1\_pru0\_pru\_r31\_16
    25         A14           GPIO3\_21\*   mcasp0\_ahclkx           eQEP0\_strobe         mcasp0\_axr3          mcasp1\_axr1                       EMU4\_mux2                    pr1\_pru0\_pru\_r30\_7    pr1\_pru0\_pru\_r31\_7
    26         D16           UART1\_RXD    uart1\_rxd               mmc1\_sdwp            dcan1\_tx             I2C1\_SDA                                                        pr1\_uart0\_rxd           pr1\_pru1\_pru\_r31\_16
    27         C13           GPIO3\_19     mcasp0\_fsr              eQEP0B\_in            mcasp0\_axr3          mcasp1\_fsx                        EMU2\_mux2                    pr1\_pru0\_pru\_r30\_5    pr1\_pru0\_pru\_r31\_5
    28         C12           SPI1\_CS0     mcasp0\_ahclkr           ehrpwm0\_synci        mcasp0\_axr2          spi1\_cs0                          eCAP2\_in\_PWM2\_out          pr1\_pru0\_pru\_r30\_3    pr1\_pru0\_pru\_r31\_3
    29         B13           SPI1\_D0      mcasp0\_fsx              ehrpwm0B                                    spi1\_d0                           mmc1\_sdcd\_mux1              pr1\_pru0\_pru\_r30\_1    pr1\_pru0\_pru\_r31\_1
    30         D12           SPI1\_D1      mcasp0\_axr0             > ehrpwm0\_tripzone                         spi1\_d1                           mmc2\_sdcd\_mux1              pr1\_pru0\_pru\_r30\_2    pr1\_pru0\_pru\_r31\_2
    31         A13           SPI1\_SCLK    mcasp0\_aclkx            ehrpwm0A                                    spi1\_sclk                         mmc0\_sdcd\_mux1              pr1\_pru0\_pru\_r30\_0    pr1\_pru0\_pru\_r31\_0
    32                                                                                                          > VADC                                                                                     
    33         C8                                                                                               > AIN4                                                                                     
    34                                                                                                          > AGND                                                                                     
    35         A8                                                                                               > AIN6                                                                                     
    36         B8                                                                                               > AIN5                                                                                     
    37         B7                                                                                               > AIN2                                                                                     
    38         A7                                                                                               > AIN3                                                                                     
    39         B6                                                                                               > AIN0                                                                                     
    40         C7                                                                                               > AIN1                                                                                     
    41\#       D14           CLKOUT2       xdma\_event\_intr1                             tclkin                clkout2                            timer7\_mux1                  pr1\_pru0\_pru\_r31\_16   EMU3\_mux0
               D13           GPIO3\_20     mcasp0\_axr1             eQEP0\_index                                Mcasp1\_axr0                       emu3                          pr1\_pru0\_pru\_r30\_6    pr1\_pru0\_pru\_r31\_6
    42@        C18           GPIO0\_7      eCAP0\_in\_PWM0\_out     uart3\_txd            spi1\_cs1             pr1\_ecap0\_ecap\_capin\_apwm\_o   spi1\_sclk                    mmc0\_sdwp                xdma\_event\_intr2
               B12           GPIO3\_18     Mcasp0\_aclkr            eQEP0A\_in            Mcaspo\_axr2          Mcasp1\_aclkx                                                    pr1\_pru0\_pru\_r30\_4    pr1\_pru0\_pru\_r31\_4
    43-46                                                                                                       > GND                                                                                      
  
  > ****\*GPIO3\_21 is also the 24.576MHZ clock input to the processor to enable HDMI audio. To use this pin the oscillator must be disabled.****
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### 7.2 Power Jack 

The DC power jack is located next to the RJ45 Ethernet connector as
shown in **Figure 51**. This uses the same power connector as is used on
the original BeagleBone. The connector has a 2.1mm diameter center post
(5VDC) and a 5.5mm diameter outer dimension on the barrel (GND).

![](docs/media/image69.jpg){width="6.041388888888889in"
height="4.281972878390201in"}

###### Figure 51. 5VDC Power Jack 

The board requires a regulated 5VDC +/-.25V supply at 1A. A higher
current rating may be needed if capes are plugged into the expansion
headers. Using a higher current power supply will not damage the board.

### 7.3 USB Client 

The USB Client connector is accessible on the bottom side of the board
under the row of four LEDs as shown in **Figure 52**. It uses a 5 pin
miniUSB cable, the same as is used on the original BeagleBone. The cable
is provided with the board. The cable can also be used to power the
board.

![](docs/media/image71.jpg){width="6.602055993000875in"
height="4.730194663167104in"}

This port is a USB Client only interface and is intended for connection
to a PC.

### 7.4 USB Host 

There is a single USB Host connector on the board and is shown in
**Figure 53** below.

![](docs/media/image71.jpg){width="6.184388670166229in"
height="4.033500656167979in"}

###### Figure 53. USB Host Connector 

The port is USB 2.0 HS compatible and can supply up to 500mA of current.
If more current or ports is needed, then a HUB can be used.

### 7.5 Serial Header 

Each board has a debug serial interface that can be accessed by using a
special serial cable that is plugged into the serial header as shown in
**Figure 54** below.

> ![](docs/media/image71.jpg){width="5.4998611111111115in"
> height="3.6651673228346455in"}

###### Figure 54. Serial Debug Header 

Two signals are provided, TX and RX on this connector. The levels on
these signals are 3.3V. In order to access these signals, a FTDI USB to
Serial cable is recommended as shown in **Figure 55** below.

> ![](docs/media/image73.jpg){width="4.465360892388452in"
> height="1.6920614610673665in"}

The cable can be purchased from several different places and must be the
3.3V version TTL-232R-3V3. Information on the cable itself can be found
direct from FTDI at:

[*http://www.ftdichip.com/Support/Documents/DataSheets/Cables/DS\_TTL232R\_CABLES.pdf*
](http://www.ftdichip.com/Support/Documents/DataSheets/Cables/DS_TTL-232R_CABLES.pdf)

Pin 1 of the cable is the black wire. That must align with the pin 1 on
the board which is designated by the white dot next to the connector on
the board.

Refer to the support WIKI
[*http://circuitco.com/support/index.php?title=BeagleBoneBlack*](http://circuitco.com/support/index.php?title=BeagleBoneBlack)
for more sources of this cable and other options that will work.

Table is the pinout of the connector as reflected in the schematic. It
is the same as the

FTDI cable which can be found at

[*http://www.ftdichip.com/Support/Documents/DataSheets/Cables/DS\_TTL-*](http://www.ftdichip.com/Support/Documents/DataSheets/Cables/DS_TTL-232R_CABLES.pdf)

[*232R\_CABLES.pdf*](http://www.ftdichip.com/Support/Documents/DataSheets/Cables/DS_TTL-232R_CABLES.pdf)
with the exception that only three pins are used on the board. The pin
numbers are defined in **Table 14**. The signals are from the
perspective of the board.

######  Table 14. J1 Serial Header Pins 

  PIN NUMBER   SIGNAL
  ------------ ------------
  > **1 **     > Ground
  > **4 **     > Receive
  > **5 **     > Transmit

**Figure 56** shows the pin location on the board.

> ![](docs/media/image75.jpg){width="3.8956944444444446in"
> height="3.9025273403324583in"}

**Figure 56. Serial Header **

### 7.6 HDMI 

Access to the HDMI interface is through the HDMI connector that is
located on the bottom side of the board as shown in **Figure 57** below.

> ![](docs/media/image71.jpg){width="6.03625in"
> height="4.033500656167979in"}

###### Figure 57. HDMI Connector 

The connector is microHDMI connector. This was done due to the space
limitations we had in finding a place to fit the connector. It requires
a microHDMI to HDMI cable as shown in **Figure 58** below. The cable can
be purchased from several different sources.

> ![](docs/media/image77.jpg){width="2.0430555555555556in"
> height="2.0430566491688538in"}

**Figure 58. HDMI Cable **

### 7.7 microSD 

A microSD connector is located on the back or bottom side of the board
as shown in **Figure 59** below. The microSD card is not supplied with
the board.

![](docs/media/image71.jpg){width="6.039388670166229in"
height="4.566833989501312in"}

###### Figure 59. microSD Connector 

When plugging in the SD card, the writing on the card should be up.
Align the card with the connector and push to insert. Then release.
There should be a click and the card will start to eject slightly, but
it then should latch into the connector. To eject the card, push the SD
card in and then remove your finger. The SD card will be ejected from
the connector.

Do not pull the SD card out or you could damage the connector.

### 7.8 Ethernet 

The board comes with a single 10/100 Ethernet interface located next to
the power jack as shown in **Figure 60**.

> ![](docs/media/image71.jpg){width="6.03625in"
> height="4.033500656167979in"}

**Figure 60. Ethernet Connector **

The PHY supports AutoMDX which means either a straight or a swap cable
can be used

### 7.9 JTAG Connector 

A place for an optional 20 pin CTI JTAG header is provided on the board
to facilitate the SW development and debugging of the board by using
various JTAG emulators. This header is not supplied standard on the
board. To use this, a connector will need to be soldered onto the board.

If you need the JTAG connector you can solder it on yourself. No other
components are needed. The connector is made by Samtec and the part
number is FTR-110-03-G-D-06. You can purchase it from
[*www.digikey.com*.](http://www.digikey.com/)

**8.0 Cape Board Support **
===========================

The BeagleBone Black has the ability to accept up to four expansion
boards or capes that can be stacked onto the expansion headers. The word
cape comes from the shape of the board as it is fitted around the
Ethernet connector on the main board. This notch acts as a key to ensure
proper orientation of the cape.

This section describes the rules for creating capes to ensure proper
operation with the BeagleBone Black and proper interoperability with
other capes that are intended to coexist with each other. Co-existence
is not a requirement and is in itself, something that is impossible to
control or administer. But, people will be able to create capes that
operate with other capes that are already available based on public
information as it pertains to what pins and features each cape uses.
This information will be able to be read from the EEPROM on each cape.

This section is intended as a guideline for those wanting to create
their own capes. Its intent is not to put limits on the creation of
capes and what they can do, but to set a few basic rules that will allow
the SW to administer their operation with the BeagleBone Black. For this
reason there is a lot of flexibility in the specification that we hope
most people will find liberating and in the spirit of Open Source
Hardware. I am sure there are others that would like to see tighter
control, more details, more rules and much more order to the way capes
are handled.

Over time, this specification will change and be updated, so please
refer to the latest version of this manual prior to designing your own
capes to get the latest information.

**DO NOT APPLY VOLTAGE TO ANY I/O PIN WHEN **

**POWER IS NOT SUPPLIED TO THE BOARD. IT WILL DAMAGE THE PROCESSOR AND
VOID THE WARRANTY. **

**NO PINS ARE TO BE DRIVEN UNTIL AFTER THE SYS\_RESET LINE GOES HIGH. **

### 8.1 BeagleBoneBlack Cape Compatibility 

The main expansion headers are the same between the BeagleBone and
BeagleBone Black. While the pins are the same, some of these pins are
now used on the BeagleBone Black. The following sections discuss these
pins.

The Power Expansion header was removed from the BeagleBone Black and is
not available.

****PAY VERY CLOSE ATTENTION TO THIS SECTION AND READ CAREFULLY!! ****

#### 8.1.1 LCD Pins 

The LCD pins are used on the BeagleBone Black to drive the HDMI framer.
These signals are listed in **Table 15** below.

######  Table 15. P8 LCD Conflict Pins 

  **PIN **   > **PROC **   **NAME **       **MODE0 **
  ---------- ------------- --------------- ---------------------
  > 27       U5            GPIO2\_22       lcd\_vsync
  > 28       V5            GPIO2\_24       lcd\_pclk
  > 29       R5            GPIO2\_23       lcd\_hsync
  > 30       R6            GPIO2\_25       > lcd\_ac\_bias\_en
  > 31       V4            > UART5\_CTSN   lcd\_data14
  > 32       T5            > UART5\_RTSN   lcd\_data15
  > 33       V3            > UART4\_RTSN   lcd\_data13
  > 34       U4            > UART3\_RTSN   lcd\_data11
  > 35       V2            > UART4\_CTSN   lcd\_data12
  > 36       U3            > UART3\_CTSN   lcd\_data10
  > 37       U1            > UART5\_TXD    lcd\_data8
  > 38       U2            > UART5\_RXD    lcd\_data9
  > 39       T3            GPIO2\_12       lcd\_data6
  > 40       T4            GPIO2\_13       lcd\_data7
  > 41       T1            GPIO2\_10       lcd\_data4
  > 42       T2            GPIO2\_11       lcd\_data5
  > 43       R3            GPIO2\_8        lcd\_data2
  > 44       R4            GPIO2\_9        lcd\_data3
  > 45       R1            GPIO2\_6        lcd\_data0
  > 46       R2            GPIO2\_7        lcd\_data1

If you are using these pins for other functions, there are a few things
to keep in mind:

-   On the HDMI Framer, these signals are all inputs so the framer will
    not be driving these pins.

-   The HDMI framer will add a load onto these pins.

-   There are small filter caps on these signals which could also change
    the operation of these pins if used for other functions.

-   When used for other functions, the HDMI framer cannot be used.

-   There is no way to power off the framer as this would result in the
    framer being powered through these input pins which would not a be a
    good idea.

-   These pins are also the **SYSBOOT** pins. DO NOT drive them before
    the **SYS\_RESETN** signal goes high. If you do, the board may not
    boot because you would be changing the boot order of the processor.

In order to use these pins, the SW will need to reconfigure them to
whatever function you need the pins to do. To keep power low, the HDMI
framer should be put in a low power mode via the SW using the **I2C0**
interface.

#### 8.1.2 eMMC Pins 

The BeagleBone Black uses 10 pins to connect to the processor that also
connect to the

P8 expansion connector. These signals are listed below in **Table 16**.
The proper mode is

MODE2.

######  Table 16. P8 eMMC Conflict Pins 

  > **PIN **   **PROC **   **SIGNAL **   > **MODE **
  ------------ ----------- ------------- -------------
  > 22         V8          MMC1\_DAT5    1
  > 23         > U8        MMC1\_DAT4    1
  > 24         V7          MMC1\_DAT1    1
  5            > R8        MMC1\_DAT2    1
  4            T9          MMC1\_DAT7    1
  3            > R9        MMC1\_DAT6    1
  6            T8          MMC1\_DAT3    1
  > 25         > U7        MMC1\_DAT0    1
  > 20         V9          > MMC1\_CMD   2
  > 21         > U9        > MMC1\_CLK   2

If using these pins, several things need to be kept in mind when doing
so:

-   On the eMMC device, these signals are inputs and outputs.

-   The eMMC device will add a load onto these pins.

-   When used for other functions, the eMMC cannot be used. This means
    you must boot from the microSD slot.

-   If using these pins, you need to put the eMMC into reset. This
    requires that the eMMC be accessible from the processor in order to
    set the eMMC to accept the eMMC pins.

-   DO NOT drive the eMMC pins until the eMMC has been put into reset.
    This means that if you choose to use these pins, they must not drive
    any signal until enabled via Software. This requires a buffer or
    some other form of hold off function enabled by a GPIO pin on the
    expansion header.

On power up, the eMMC is NOT reset. If you hold the Boot button down,
this will force a boot from the microSD. This is not convenient when a
cape is plugged into the board. There are two solutions to this issue:

1.  Wipe the eMMC clean. This will cause the board to default to microSD
    boot. If you want to use the eMMC later, it can be reprogrammed.

2.  You can also tie LCD\_DATA2 low on the cape during boot. This will
    be the same as if you were holding the boot button. However, in
    order to prevent unforeseen issues, you need to gate this signal
    with RESET, when the data is sampled. After reset goes high, the
    signal should be removed from the pin.

***BEFORE*** the SW reinitializes the pins, it ***MUST*** put the eMMC
in reset. This is done by taking eMMC\_RSTn (GPIO1\_20) LOW
****after**** the eMMC has been put into a mode to enable the reset
line. This pin does not connect to the expansion header and is
accessible only on the board.

**DO NOT** automatically drive any conflicting pins until the SW enables
it. This puts the SW in control to ensure that the eMMC is in reset
before the signals are used from the cape. You can use a GPIO pin for
this. No, we will not designate a pin for this function. It will be
determined on a cape by cape basis by the designer of the respective
cape.

### 8.2 EEPROM 

Each cape must have its own EEPROM containing information that will
allow the SW to identify the board and to configure the expansion
headers pins as needed. The one exception is proto boards intended for
prototyping. They may or may not have an EEPROM on them. An EEPROM is
required for all capes sold in order for them operate correctly when
plugged into the BeagleBone Black.

The address of the EEPROM will be set via either jumpers or a dipswitch
on each expansion board. **Figure 61** below is the design of the EEPROM
circuit.

The EEPROM used is the same one as is used on the BeagleBone and the
BeagleBone Black, a CAT24C256. The CAT24C256 is a 256 kb Serial CMOS
EEPROM, internally organized as 32,768 words of 8 bits each. It features
a 64−byte page write buffer and supports the Standard (100 kHz), Fast
(400 kHz) and Fast−Plus (1 MHz) I2C protocol.

> ![](docs/media/image78.png){width="5.303334426946631in"
> height="2.3833333333333333in"}

###### Figure 61. Expansion Board EEPROM Without Write Protect 

The addressing of this device requires two bytes for the address which
is not used on smaller size EEPROMs, which only require only one byte.
Other compatible devices may be used as well. Make sure the device you
select supports 16 bit addressing. The part package used is at the
discretion of the cape designer.

#### 8.2.1 EEPROM Address 

In order for each cape to have a unique address, a board ID scheme is
used that sets the address to be different depending on the setting of
the dipswitch or jumpers on the capes. A two position dipswitch or
jumpers is used to set the address pins of the EEPROM.

It is the responsibility of the user to set the proper address for each
board and the position in the stack that the board occupies has nothing
to do with which board gets first choice on the usage of the expansion
bus signals. The process for making that determination and resolving
conflicts is left up to the SW and, as of this moment in time, this
method is a something of a mystery due to the new Device Tree
methodology introduced in the 3.8 kernel.

Address line A2 is always tied high. This sets the allowable address
range for the expansion cards to **0x54** to **0x57**. All other I2C
addresses can be used by the user in the design of their capes. But,
these addresses must not be used other than for the board EEPROM
information. This also allows for the inclusion of EEPROM devices on the
cape if needed without interfering with this EEPROM. It requires that A2
be grounded on the EEPROM not used for cape identification.

#### 8.2.2 I2C Bus 

The EEPROMs on each expansion board are connected to I2C2 on connector
P9 pins 19 and 20. For this reason I2C2 must always be left connected
and should not be changed by SW to remove it from the expansion header
pin mux settings. If this is done, the system will be unable to detect
the capes.

The I2C signals require pullup resistors. Each board must have a 5.6K
resistor on these signals. With four capes installed this will result in
an effective resistance of 1.4K if all capes were installed and all the
resistors used were exactly 5.6K. As more capes are added the resistance
is reduced to overcome capacitance added to the signals. When no capes
are installed the internal pullup resistors must be activated inside the
processor to prevent I2C timeouts on the I2C bus.

The I2C2 bus may also be used by capes for other functions such as I/O
expansion or other I2C compatible devices that do not share the same
address as the cape EEPROM.

#### 8.2.3 EEPROM Write Protect 

The design in **Figure 62** has the write protect disabled. If the write
protect is not enabled, this does expose the EEPROM to being corrupted
if the I2C2 bus is used on the cape and the wrong address written to. It
is recommended that a write protection function be implemented and a
Test Point be added that when grounded, will allow the EEPROM to be
written to. To enable write operation, Pin 7 of the EEPROM must be tied
to ground.

When not grounded, the pin is HI via pullup resistor R210 and therefore
write protected. Whether or not Write Protect is provided is at the
discretion of the cape designer.

> **Variable & MAC Memory**

VDD\_3V3B

> ![](docs/media/image79.png){width="5.91in"
> height="1.9766666666666666in"}

###### Figure 62. Expansion Board EEPROM Write Protect 

#### 8.2.4 EEPROM Data Format 

**Table 17** shows the format of the contents of the expansion board
EEPROM. Data is stored in Big Endian with the least significant value on
the right. All addresses read as a single byte data from the EEPROM, but
two byte addressing is used. ASCII values are intended to be easily read
by the user when the EEPROM contents are dumped.

######  Table 17. Expansion Board EEPROM 

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Name **                > **Offset **   **Size (bytes) **   **Contents **
  ------------------------ --------------- ------------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Header **              **0 **          **4 **              **0xAA, 0x55, 0x33, 0xEE **

  **EEPROM Revision **     **4 **          **2 **              **Revision number of the overall format of this EEPROM in ASCII =A1 **

  **Board Name **          **6 **          **32 **             **Name of board in ASCII so user can read it when the EEPROM is dumped. Up to developer of the board as to what they call the board.. **

  **Version **             **38 **         **4 **              > **Hardware version code for board in ASCII. Version format is up to the developer. **
                                                               
                                                               **i.e. 02.1…00A1....10A0 **

  **Manufacturer **        **42 **         **16 **             **ASCII name of the manufacturer. Company or individual’s name. **

  **Part Number **         **58 **         **16 **             **ASCII Characters for the part number. Up to maker of the board. **

  **Number of Pins **      **74 **         **2 **              **Number of pins used by the daughter board including the power pins used. Decimal value of total pins 92 max, stored in HEX. **

  **Serial Number **       **76 **         **12 **             **Serial number of the board. This is a 12 character string which is: **
                                                               
                                                               **WWYY&&&&nnnn **
                                                               
                                                               **where: WW = 2 digit week of the year of production **
                                                               
                                                               **YY = 2 digit year of production **
                                                               
                                                               > **&&&&=Assembly code to let the manufacturer document the assembly number or product. A way to quickly tell from reading the serial number what the board is. Up to the developer to determine. **
                                                               
                                                               **nnnn = incrementing board number for that week of production **

  **Pin Usage **           **88 **         **148 **            ***Two bytes* for each configurable pins of the 74 pins on the expansion **
                                                               
                                                               **connectors *MSB* *LSB* **
                                                               
                                                               **Bit order: 15 14 ……………1..0 **
                                                               
                                                               **Bit 15…………..Pin is used or not……..…...0=Unused by cape 1=Used by cape **
                                                               
                                                               **Bit 14-13………Pin Direction…………...….1 0=Output 01=Input 11=BDIR **
                                                               
                                                               **Bits 12-7………Reserved……………………should be all zeros **
                                                               
                                                               **Bit 6……….…..Slew Rate …………………..0=Fast 1=Slow **
                                                               
                                                               **Bit 5…….……..Rx Enable…………………..0=Disabled 1=Enabled **
                                                               
                                                               **Bit 4……….…..Pull Up/Dn Select…………..0=Pulldown 1=PullUp **
                                                               
                                                               **Bit 3…………...Pull Up/DN enabled………..0=Enabled 1=Disabled **
                                                               
                                                               **Bits 2-0 ……….Mux Mode Selection………..Mode 0-7 **

  **VDD\_3V3B Current **   **236 **        **2 **              **Maximum current in milliamps. This is HEX value of the current in decimal **
                                                               
                                                               **1500mA=0x05 0xDC 325mA=0x01 0x45 **

  **VDD\_5V Current **     **238 **        **2 **              **Maximum current in milliamps. This is HEX value of the current in decimal **
                                                               
                                                               **1500mA=0x05 0xDC 325mA=0x01 0x45 **

  **SYS\_5V Current **     **240 **        **2 **              **Maximum current in milliamps. This is HEX value of the current in decimal **
                                                               
                                                               **1500mA=0x05 0xDC 325mA=0x01 0x45 **

  **DC Supplied **         **242 **        **2 **              **Indicates whether or not the board is supplying voltage on the VDD\_5V rail and the current rating 000=No 1-0xFFFF is the current supplied storing the decimal **
                                                               
                                                               **equivalent in HEX format **

  **Available **           **244 **        **32543 **          **Available space for other non-volatile codes/data to be used as needed by the manufacturer or SW driver. Could also store presets for use by SW. **
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### 8.2.5 Pin Usage 

**Table 18** is the locations in the EEPROM to set the I/O pin usage for
the cape. It contains the value to be written to the Pad Control
Registers. Details on this can be found in section **9.2.2** of the
**AM3358 Technical Reference Manual**, The table is left blank as a
convenience and can be printed out and used as a template for creating a
custom setting for each cape. The 16 bit integers and all 16 bit fields
are to be stored in Big Endian format.

***Bit 15 PIN USAGE*** is an indicator and should be a 1 if the pin is
used or 0 if it is unused.

***Bits 14-7 RESERVED*** is not to be used and left as 0.

***Bit 6 SLEW CONTROL*** 0=Fast 1=Slow ***Bit 5 RX Enabled*** 0=Disabled
1=Enabled ***Bit 4 PU/PD*** 0=Pulldown 1=Pullup.

***Bit 3 PULLUP/DN*** 0=Pullup/pulldown enabled

> 1= Pullup/pulldown disabled

***Bit 2-0 MUX MODE SELECT*** Mode 0-7. (refer to TRM)

Refer to the TRM for proper settings of the pin MUX mode based on the
signal selection to be used.

The **AIN0-6** pins do not have a pin mux setting, but they need to be
set to indicate if each of the pins is used on the cape. Only bit 15 is
used for the AIN signals.

###### Table 18. EEPROM Pin Usage 

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                                     **15 **        > **14 **     > **13 **   > **12 **       > **11 **   > **10 **   > **9 **   > **8 **   > **7 **   > **6 **   > **5 **
  -------------- -------------- -------------------- -------------- ------------- ----------- --------------- ----------- ----------- ---------- ---------- ---------- ---------- --------------- ---------- ---------- ---------- -------- --------
  **Off set **   > **Conn **    **Name **            **Pin **       > **Type **               **Reserved **                           > **S**    > **R**    > **P**    > **P**    **Mux Mode **
                                                                                                                                      >          >          >          >          
                                                     > **Usage **                                                                     > **L**    > **X **   > **U**    > **U**    
                                                                                                                                      >                     >          >          
                                                                                                                                      > **E**               > **-**    > **/**    
                                                                                                                                                            >                     
                                                                                                                                      **W **                > **P**    **D E**    
                                                                                                                                                            >                     
                                                                                                                                                            > **D **   > **N **   

  **88 **        > **P9-22 **   > **UART2\_RXD **                                                                                                                                 

  **90 **        > **P9-21 **   > **UART2\_TXD **                                                                                                                                 

  **92 **        > **P9-18 **   **I2C1\_SDA **                                                                                                                                    

  **94 **        > **P9-17 **   **I2C1\_SCL **                                                                                                                                    

  **96 **        > **P9-42 **   **GPIO0\_7 **                                                                                                                                     

  **98 **        > **P8-35 **   > **UART4\_CTSN **                                                                                                                                

  **100 **       > **P8-33 **   > **UART4\_RTSN **                                                                                                                                

  **102 **       > **P8-31 **   > **UART5\_CTSN **                                                                                                                                

  **104 **       > **P8-32 **   > **UART5\_RTSN **                                                                                                                                

  **106 **       > **P9-19 **   **I2C2\_SCL **                                                                                                                                    

  **108 **       > **P9-20 **   **I2C2\_SDA **                                                                                                                                    

  **110 **       > **P9-26 **   > **UART1\_RXD **                                                                                                                                 

  **112 **       > **P9-24 **   > **UART1\_TXD **                                                                                                                                 

  **114 **       > **P9-41 **   **CLKOUT2 **                                                                                                                                      

  **116 **       > **P8-19 **   > **EHRPWM2A **                                                                                                                                   

  **118 **       > **P8-13 **   > **EHRPWM2B **                                                                                                                                   

  **120 **       > **P8-14 **   **GPIO0\_26 **                                                                                                                                    

  **122 **       > **P8-17 **   **GPIO0\_27 **                                                                                                                                    

  **124 **       > **P9-11 **   > **UART4\_RXD **                                                                                                                                 

  **126 **       > **P9-13 **   > **UART4\_TXD **                                                                                                                                 

  **128 **       > **P8-25 **   **GPIO1\_0 **                                                                                                                                     

  **130 **       > **P8-24 **   **GPIO1\_1 **                                                                                                                                     

  **132 **       **P8-5 **      **GPIO1\_2 **                                                                                                                                     

  **134 **       **P8-6 **      **GPIO1\_3 **                                                                                                                                     

  **136 **       > **P8-23 **   **GPIO1\_4 **                                                                                                                                     

  **138 **       > **P8-22 **   **GPIO1\_5 **                                                                                                                                     

  **140 **       **P8-3 **      **GPIO1\_6 **                                                                                                                                     

  **142 **       **P8-4 **      **GPIO1\_7 **                                                                                                                                     

  **144 **       > **P8-12 **   **GPIO1\_12 **                                                                                                                                    

  **146 **       > **P8-11 **   **GPIO1\_13 **                                                                                                                                    

  **148 **       > **P8-16 **   **GPIO1\_14 **                                                                                                                                    

  **150 **       > **P8-15 **   **GPIO1\_15 **                                                                                                                                    

  **152 **       > **P9-15 **   **GPIO1\_16 **                                                                                                                                    
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                                     **15 **        > **14 **     > **13 **   > **12 **       > **11 **   > **10 **   > **9 **   > **8 **   > **7 **   > **6 **   > **5 **
  -------------- -------------- -------------------- -------------- ------------- ----------- --------------- ----------- ----------- ---------- ---------- ---------- ---------- --------------- ---------- ---------- ---------- -------- --------
  **Off set **   > **Conn **    **Name **            **Pin **       > **Type **               **Reserved **                           > **S**    > **R**    > **P**    > **P**    **Mux Mode **
                                                                                                                                      >          >          >          >          
                                                     > **Usage **                                                                     > **L**    > **X **   > **U**    > **U**    
                                                                                                                                      >                     >          >          
                                                                                                                                      > **E**               > **-**    > **/**    
                                                                                                                                                            >                     
                                                                                                                                      **W **                > **P**    **D E**    
                                                                                                                                                            >                     
                                                                                                                                                            > **D **   > **N **   

  **154 **       > **P9-23 **   **GPIO1\_17 **                                                                                                                                    

  **156 **       > **P9-14 **   > **EHRPWM1A **                                                                                                                                   

  **158 **       > **P9-16 **   > **EHRPWM1B **                                                                                                                                   

  **160 **       > **P9-12 **   **GPIO1\_28 **                                                                                                                                    

  **162 **       > **P8-26 **   **GPIO1\_29 **                                                                                                                                    

  **164 **       > **P8-21 **   **GPIO1\_30 **                                                                                                                                    

  **166 **       > **P8-20 **   **GPIO1\_31 **                                                                                                                                    

  **168 **       > **P8-18 **   **GPIO2\_1 **                                                                                                                                     

  **170 **       **P8-7 **      **TIMER4 **                                                                                                                                       

  **172 **       **P8-9 **      **TIMER5 **                                                                                                                                       

  **174 **       > **P8-10 **   **TIMER6 **                                                                                                                                       

  **176 **       **P8-8 **      **TIMER7 **                                                                                                                                       

  **178 **       > **P8-45 **   **GPIO2\_6 **                                                                                                                                     

  **180 **       > **P8-46 **   **GPIO2\_7 **                                                                                                                                     

  **182 **       > **P8-43 **   **GPIO2\_8 **                                                                                                                                     

  **184 **       > **P8-44 **   **GPIO2\_9 **                                                                                                                                     

  **186 **       > **P8-41 **   **GPIO2\_10 **                                                                                                                                    

  **188 **       > **P8-42 **   **GPIO2\_11 **                                                                                                                                    

  **190 **       > **P8-39 **   **GPIO2\_12 **                                                                                                                                    

  **192 **       > **P8-40 **   **GPIO2\_13 **                                                                                                                                    

  **194 **       > **P8-37 **   > **UART5\_TXD **                                                                                                                                 

  **196 **       > **P8-38 **   > **UART5\_RXD **                                                                                                                                 

  **198 **       > **P8-36 **   > **UART3\_CTSN **                                                                                                                                

  **200 **       > **P8-34 **   > **UART3\_RTSN **                                                                                                                                

  **202 **       > **P8-27 **   **GPIO2\_22 **                                                                                                                                    

  **204 **       > **P8-29 **   **GPIO2\_23 **                                                                                                                                    

  **206 **       > **P8-28 **   **GPIO2\_24 **                                                                                                                                    

  > **208 **     > **P8-30 **   **GPIO2\_25 **                                                                                                                                    

  > **210 **     > **P9-29 **   **SPI1\_D0 **                                                                                                                                     

  **212 **       > **P9-30 **   **SPI1\_D1 **                                                                                                                                     

  **214 **       > **P9-28 **   **SPI1\_CS0 **                                                                                                                                    

  **216 **       > **P9-27 **   **GPIO3\_19 **                                                                                                                                    

  **218 **       > **P9-31 **   **SPI1\_SCLK **                                                                                                                                   

  **220 **       > **P9-25 **   **GPIO3\_21 **                                                                                                                                    

                                                     **15 **        > **14 **     > **13 **   > **12 **       > **11 **   > **10 **   > **9 **   > **8 **   > **7 **   > **6 **   > **5 **

  **Off set **   > **Conn **    **Name **            **Pin **       > **Type **               **Reserved **                           > **S**    > **R**    > **P**    > **P**    **Mux Mode **
                                                                                                                                      >          >          >          >          
                                                     > **Usage **                                                                     > **L**    > **X **   > **U**    > **U**    
                                                                                                                                      >                     >          >          
                                                                                                                                      > **E**               > **-**    > **/**    
                                                                                                                                                            >                     
                                                                                                                                      **W **                > **P**    **D E**    
                                                                                                                                                            >                     
                                                                                                                                                            > **D **   > **N **   

                                                                    > **0 **      > **0 **    **0 **          > **0 **    > **0 **    > **0 **   > **0 **   > **0 **   > **0 **   > **0 **

  > **222 **     > **P9-39 **   **AIN0 **                                                                                                                                         

  > **224 **     > **P9-40 **   **AIN1 **                                                                                                                                         

  > **226 **     > **P9-37 **   **AIN2 **                                                                                                                                         

  > **228 **     > **P9-38 **   **AIN3 **                                                                                                                                         

  > **230 **     > **P9-33 **   **AIN4 **                                                                                                                                         

  > **232 **     > **P9-36 **   **AIN5 **                                                                                                                                         

  > **234 **     > **P9-35 **   **AIN6 **                                                                                                                                         
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### 8.3 Pin Usage Consideration 

This section covers things to watch for when hooking up to certain pins
on the expansion headers.

#### 8.3.1 Boot Pins 

There are 16 pins that control the boot mode of the processor that are
exposed on the expansion headers. **Figure 63** below shows those
signals as they appear on the BeagleBone Black.:

> ![](docs/media/image80.png){width="5.530001093613298in"
> height="4.88in"}

If you plan to use any of these signals, then on power up, these pins
should not be driven. If you do, it can affect the boot mode of the
processor and could keep the processor from booting or working
correctly.

If you are designing a cape that is intended to be used as a boot
source, such as a NAND board, then you should drive the pins to
reconfigure the boot mode, but only at reset. After the reset phase, the
signals should not be driven to allow them to be used for the other
functions found on those pins. You will need to override the resistor
values in order to change the settings. The DC pull-up requirement
should be based on the AM3358 Vih min voltage of 2 volts and AM3358
maximum input leakage current of 18uA. Also take into account any other
current leakage paths on these signals which could be caused by your
specific cape design.

The DC pull-down requirement should be based on the AM3358 Vil max
voltage of 0.8 volts and AM3358 maximum input leakage current of 18uA
plus any other current leakage paths on these signals.

### 8.4 Expansion Connectors 

A combination of male and female headers is used for access to the
expansion headers on the main board. There are three possible mounting
configurations for the expansion headers:

-   *Single*-no board stacking but can be used on the top of the stack.

-   *Stacking*-up to four boards can be stacked on top of each other.

-   *Stacking with signal stealing*-up to three boards can be stacked on
    top of each other, but certain boards will not pass on the signals
    they are using to prevent signal loading or use by other cards in
    the stack.

The following sections describe how the connectors are to be implemented
and used for each of the different configurations.

#### 8.4.1 Non-Stacking Headers-Single Cape 

For non-stacking capes single configurations or where the cape can be
the last board on the stack, the two 46 pin expansion headers use the
same connectors. **Figure 64** is a picture of the connector. These are
dual row 23 position 2.54mm x 2.54mm connectors.

> ![](docs/media/image81.jpg){width="0.6861111111111111in"
> height="0.9381944444444444in"}

###### Figure 64. Single Expansion Connector 

The connector is typically mounted on the bottom side of the board as
shown in **Figure 65**. These are very common connectors and should be
easily located. You can also use two single row 23 pin headers for each
of the dual row headers.

![](docs/media/image82.jpg){width="5.9986122047244095in"
height="0.5715277777777777in"}

###### Figure 65. Single Cape Expansion Connector 

It is allowed to only populate the pins you need. As this is a
non-stacking configuration, there is no need for all headers to be
populated. This can also reduce the overall cost of the cape. This
decision is up to the cape designer.

For convenience listed in **Table 19** are some possible choices for
part numbers on this connector. They have varying pin lengths and some
may be more suitable than others for your use. It should be noted, that
the longer the pin and the further it is inserted into the BeagleBone
Black connector, the harder it will be to remove due to the tension on
92 pins. This can be minimized by using shorter pins or removing those
pins that are not used by your particular design. The first item in
**Table 18** is on the edge and may not be the best solution. Overhang
is the amount of the pin that goes past the contact point of the
connector on the BeagleBone Black

.

######  Table 19. Single Cape Connectors 

  > **SUPPLIER **                                      > **PARTNUMBER **        > **TAIL LENGTH(in) **   > **OVERHANG(in) **
  ---------------------------------------------------- ------------------------ ------------------------ ---------------------
  > [*Major League* ](http://www.mlelectronics.com/)   TSHC-123-D-03-145-G-LF   > .145                   > .004
  > [*Major League* ](http://www.mlelectronics.com/)   TSHC-123-D-03-240-G-LF   > .240                   > .099
  > [*Major League* ](http://www.mlelectronics.com/)   TSHC-123-D-03-255-G-LF   > .255                   > .114

The G in the part number is a plating option. Other options may be used
as well as long as the contact area is gold. Other possible sources are
Sullins and Samtec for these connectors. You will need to ensure the
depth into the connector is sufficient

#### 8.4.2 Main Expansion Headers-Stacking 

For stacking configuration, the two 46 pin expansion headers use the
same connectors. **Figure 66** is a picture of the connector. These are
dual row 23 position 2.54mm x 2.54mm connectors.

![](docs/media/image83.jpg){width="0.7284722222222222in"
height="0.9381944444444444in"}

###### Figure 66. Expansion Connector 

The connector is mounted on the top side of the board with longer tails
to allow insertion into the BeagleBone Black. **Figure 67** is the
connector configuration for the connector.

![](docs/media/image84.jpg){width="5.9986122047244095in"
height="0.6847222222222222in"}

###### Figure 67. Stacked Cape Expansion Connector 

For convenience listed in **Table 18** are some possible choices for
part numbers on this connector. They have varying pin lengths and some
may be more suitable than others for your use. It should be noted, that
the longer the pin and the further it is inserted into the BeagleBone
Black connector, the harder it will be to remove due to the tension on
92 pins. This can be minimized by using shorter pins. There are most
likely other suppliers out there that will work for this connector as
well. If anyone finds other suppliers of compatible connectors that
work, let us know and they will be added to this document. The first
item in **Table 19** is on the edge and may not be the best solution.
Overhang is the amount of the pin that goes past the contact point of
the connector on the BeagleBone Black.

The third part listed in **Table 20** will have insertion force issues.

######  Table 20. Stacked Cape Connectors 

  > **SUPPLIER **                                      > **PARTNUMBER **    > **TAIL LENGTH(in) **   > **OVERHANG(in) **
  ---------------------------------------------------- -------------------- ------------------------ ---------------------
  > [*Major League* ](http://www.mlelectronics.com/)   SSHQ-123-D-06-G-LF   .190                     > 0.049
  > [*Major League* ](http://www.mlelectronics.com/)   SSHQ-123-D-08-G-LF   .390                     > 0.249
  > [*Major League* ](http://www.mlelectronics.com/)   SSHQ-123-D-10-G-LF   .560                     > 0.419

There are also different plating options on each of the connectors
above. Gold plating on the contacts is the minimum requirement. If you
choose to use a different part number for plating or availability
purposes, make sure you do not select the “LT” option.

Other possible sources are Sullins and Samtec but make sure you select
one that has the correct mating depth.

#### 8.4.3 Stacked Capes w/Signal Stealing 

**Figure 68** is the connector configuration for stackable capes that
does not provide all of the signals upwards for use by other boards.
This is useful if there is an expectation that other boards could
interfere with the operation of your board by exposing those signals for
expansion. This configuration consists of a combination of the stacking
and nonstacking style connectors.

![](docs/media/image85.jpg){width="5.996527777777778in"
height="0.74375in"}

###### Figure 68. Stacked w/Signal Stealing Expansion Connector 

#### 8.4.4 Retention Force 

The length of the pins on the expansion header has a direct relationship
to the amount of force that is used to remove a cape from the BeagleBone
Black. The longer the pins extend into the connector the harder it is to
remove. There is no rule that says that if longer pins are used, that
the connector pins have to extend all the way into the mating connector
on the BeagleBone Black, but this is controlled by the user and
therefore is hard to control. We have also found that if you use gold
pins, while more expensive, it makes for a smoother finish which reduces
the friction.

This section will attempt to describe the tradeoffs and things to
consider when selecting a connector and its pin length.

#### 8.4.5 BeagleBone Black Female Connectors 

**Figure 69** shows the key measurements used in calculating how much
the pin extends past the contact point on the connector, what we call
overhang.

![](docs/media/image86.jpg){width="5.75in" height="3.279861111111111in"}

###### Figure 69. Connector Pin Insertion Depth 

To calculate the amount of the pin that extends past the Point of
Contact, use the following formula:

Overhang=Total Pin Length- PCB thickness (.062) - contact point (.079)

The longer the pin extends past the contact point, the more force it
will take to insert and remove the board. Removal is a greater issue
than the insertion.

### 8.5 Signal Usage 

Based on the pin muxing capabilities of the processor, each expansion
pin can be configured for different functions. When in the stacking
mode, it will be up to the user to ensure that any conflicts are
resolved between multiple stacked cards. When stacked, the first card
detected will be used to set the pin muxing of each pin. This will
prevent other modes from being supported on stacked cards and may result
in them being inoperative.

In **Section 7.1** of this document, the functions of the pins are
defined as well as the pin muxing options. Refer to this section for
more information on what each pin is. To simplify things, if you use the
default name as the function for each pin and use those functions, it
will simplify board design and reduce conflicts with other boards.

Interoperability is up to the board suppliers and the user. This
specification does not specify a fixed function on any pin and any pin
can be used to the full extent of the functionality of that pin as
enabled by the processor.

**DO NOT APPLY VOLTAGE TO ANY I/O PIN WHEN POWER IS NOT SUPPLIED TO THE
BOARD. IT WILL DAMAGE THE PROCESSOR AND VOID THE WARRANTY. **

**NO PINS ARE TO BE DRIVEN UNTIL AFTER THE SYS\_RESET LINE GOES HIGH. **

### 8.6 Cape Power 

This section describes the power rails for the capes and their usage.

#### 8.6.1 Main Board Power 

The **Table 1** describes the voltages from the main board that are
available on the expansion connectors and their ratings. All voltages
are supplied by connector **P9**. The current ratings listed are per
pin.

######  Table 21. Expansion Voltages 

  > **Current **   > **Name **          **P9 **   > **Name **   > **Current **
  ---------------- ------------- ------ --------- ------------- ---------------- ----------
                   > GND         > 1              > 2           > GND            
  > 250mA          > VDD\_3V3B   > 3              > 4           > VDD\_3V3B      > 250mA
  > 1000mA         > VDD\_5V     > 5              > 6           > VDD\_5V        > 1000mA
  > 250mA          > SYS\_5V     > 7              > 8           > SYS\_5V        > 250mA
                                 > :              > :                            
                   > GND         > 43             > 44          > GND            
                   > GND         > 45             > 46          > GND            

The **VDD\_3V3B** rail is supplied by the LDO on the BeagleBone Black
and is the primary power rail for expansion boards. If the power
requirement for the capes exceeds the current rating, then locally
generated voltage rail can be used. It is recommended that this rail be
used to power any buffers or level translators that may be used.

**VDD\_5V** is the main power supply from the DC input jack. This
voltage is not present when the board is powered via USB. The amount of
current supplied by this rail is dependent upon the amount of current
available. Based on the board design, this rail is limited to 1A per pin
from the main board.

The **SYS\_5V** rail is the main rail for the regulators on the main
board. When powered from a DC supply or USB, this rail will be 5V. The
available current from this rail depends on the current available from
the USB and DC external supplies.

#### 8.6.2 Expansion Board External Power 

A cape can have a jack or terminals to bring in whatever voltages may be
needed by that board. Care should be taken not to let this voltage be
fed back into any of the expansion header pins.

It is possible to provide 5V to the main board from an expansion board.
By supplying a 5V signal into the **VDD\_5V** rail, the main board can
be supplied. This voltage must not exceed 5V. You should not supply any
voltage into any other pin of the expansion connectors. Based on the
board design, this rail is limited to 1A per pin to the BeagleBone
Black.

**There are several precautions that need to me taken when working with
the expansion headers to prevent damage to the board. **

1)  **Do not apply any voltages to any I/O pins when the board is not
    powered on. **

2)  **Do not drive any external signals into the I/O pins until after
    the VDD\_3V3B rail is up. **

3)  **Do not apply any voltages that are generated from external
    sources. **

4)  **If voltages are generated from the VDD\_5V signal, those supplies
    must not become active until after the VDD\_3V3B rail is up. **

5)  **If you are applying signals from other boards into the expansion
    headers, make sure you power the board up after you power up the
    BeagleBone Black or make the connections after power is applied on
    both boards. **

**Powering the processor via its I/O pins can cause damage to the
processor. **

### 8.7 Mechanical 

This section provides the guidelines for the creation of expansion
boards from a mechanical standpoint. Defined is a standard board size
that is the same profile as the BeagleBone Black. It is expected that
the majority of expansion boards created will be of standard size. It is
possible to create boards of other sizes and in some cases this is
required, as in the case of an LCD larger than the BeagleBone Black
board.

#### 8.7.1 Standard Cape Size 

**Figure 70** is the outline of the standard cape. The dimensions are in
inches.

![](docs/media/image87.jpg){width="5.995138888888889in"
height="3.8534722222222224in"}

###### Figure 70. Cape Board Dimensions 

A slot is provided for the Ethernet connector to stick up higher than
the cape when mounted. This also acts as a key function to ensure that
the cape is oriented correctly. Space is also provided to allow access
to the user LEDs and reset button on the main board.

Some people have inquired as to the difference in the radius of the
corners of the BeagleBone Black and why they are different. This is a
result of having the BeagleBone fit into the Altoids style tin.

It is not required that the cape be exactly like the BeagleBone Black
board in this respect.

#### 8.7.2 Extended Cape Size 

Capes larger than the standard board size are also allowed. A good
example would be an LCD panel. There is no practical limit to the sizes
of these types of boards. The notch for the key is also not required,
but it is up to the supplier of these boards to ensure that the
BeagleBone Black is not plugged in incorrectly in such a manner that
damage would be cause to the BeagleBone Black or any other capes that
may be installed. Any such damage will be the responsibility of the
supplier of such a cape to repair.

As with all capes, the EEPROM is required and compliance with the power
requirements must be adhered to.

#### 8.7.3 Enclosures 

There are numerous enclosures being created in all different sizes and
styles. The mechanical design of these enclosures is not being defined
by this specification.

The ability of these designs to handle all shapes and sizes of capes,
especially when you consider up to four can be mounted with all sorts of
interface connectors, it is difficult to define a standard enclosure
that will handle all capes already made and those yet to be defined.

If cape designers want to work together and align with one enclosure and
work around it that is certainly acceptable. But we will not pick
winners and we will not do anything that impedes the openness of the
platform and the ability of enclosure designers and cape designers to
innovate and create new concepts.

**9.0 BeagleBone Black Mechanical **
====================================

### 9.1 Dimensions and Weight 

Size: 3.5” x 2.15” (86.36mm x 53.34mm)

Max height: .187” (4.76mm)

PCB Layers: 6

PCB thickness: .062” RoHS Compliant: Yes

Weight: 1.4 oz

### 9.2 Silkscreen and Component Locations 

![](docs/media/image88.jpg){width="5.529861111111111in"
height="8.153472222222222in"}

###### Figure 71. Board Dimensions 

![](docs/media/image89.jpg){width="5.145138888888889in"
height="8.522917760279965in"}

###### Figure 72. Component Side Silkscreen 

![](docs/media/image90.jpg){width="5.223611111111111in"
height="8.04513888888889in"}

**Figure 73. Circuit Side Silkscreen **

**10.0 Pictures **
==================

![](docs/media/image91.jpg){width="4.961805555555555in"
height="8.006944444444445in"}

**Figure 74. Top Side **

![](docs/media/image92.jpg){width="5.066666666666666in"
height="7.9631944444444445in"}

**Figure 75. Bottom Side **

**11.0 Support Information **
=============================

> All support for this design is through the BeagleBoard.org community
> at:
>
> *beagleboard@googlegroups.com* or
>
> [*http://beagleboard.org/discuss*](http://beagleboard.org/discuss) .

### 11.1 Hardware Design 

Design documentation can be found on the eMMC of the board under the
documents/hardware directory when connected using the USB cable.
Provided there is:

-   Schematic in PDF

-   Schematic in OrCAD (Cadence Design Entry CIS 16.3)

-   PCB Gerber

-   PCB Layout File (Allegro)

-   Bill of Material

-   System Reference Manual (This document).

This directory is not always kept up to date in every SW release due to
the frequency of changes of the SW. The best solution is to download the
files from the Circuitco WIKI at
[*http://circuitco.com/support/index.php?title=BeagleBoneBlack*](http://circuitco.com/support/index.php?title=BeagleBoneBlack)

We do not track SW revision of what is in the eMMC. SW is tracked
separately from the HW due to the frequency of changes which would
require massive relabeling of boards due to the frequent SW changes. You
should always use the latest SW revision.

To see what SW revision is loaded into the eMMC follow the instructions
at
[*http://circuitco.com/support/index.php?title=Updating\_The\_Software\#Checking\_The\_An
gstrom\_Image\_Version*
](http://circuitco.com/support/index.php?title=Updating_The_Software#Checking_The_Angstrom_Image_Version)

### 11.2 Software Updates 

It is a good idea to always use the latest software. Instructions for
how to update your software to the latest version can be found at:

[*http://circuitco.com/support/index.php?title=BeagleBoneBlack\#Updating\_the\_eMMC\_S
oftware*
](http://circuitco.com/support/index.php?title=BeagleBoneBlack#Updating_the_eMMC_Software)

### 11.3 RMA Support 

If you feel your board is defective or has issues, request an RMA by
filling out the form at
[*http://beagleboard.org/support/rma*](http://beagleboard.org/support/rma)
. You will need the serial number and revision of the board. The serial
numbers and revisions keep moving. Different boards can have different
locations depending on when they were made. The following figures show
the three locations of the serial and revision number.

![](docs/media/image93.jpg){width="5.4in" height="3.2131944444444445in"}

###### Figure 76. Initial Serial Number and Revision Locations 

![](docs/media/image94.jpg){width="5.401388888888889in"
height="2.404861111111111in"}

###### Figure 77. Second Phase Serial Number and Revision Location 

![](docs/media/image95.jpg){width="5.9986122047244095in"
height="2.321527777777778in"}

> **Figure 78. Third Phase Serial Number and Revision Location **

### 11.4 Trouble Shooting HDMI Issues 

Many people are having issues with getting HDMI to work on their
TV/Display. Unfortunately, we do not have the resources to buy all the
TVs and Monitors on the market today nor go to eBay and buy all of the
TVs and monitors made over the last five years to thoroughly test each
and every one. We are depending on community members to help us get
these tested and information provided on how to get them to work.

One would think that if it worked on a lot of different TVs and monitors
it would work on most if not all of them, assuming they meet the
specification. However, there are other issues that could also result in
these various TVs and monitors not working. The intent is that this page
will be useful in navigating some of these issues. As others also find
solutions, as long as we know about them, they will be added here as
well. For access to the most up to date troubleshooting capabilities, go
to the support wiki at
[*http://www.elinux.org/Beagleboard:BeagleBoneBlack\_HDMI*](http://www.elinux.org/Beagleboard:BeagleBoneBlack_HDMI)

The early release of the Software had some issues in the HDMI driver. Be
sure and use the latest SW to take advantage of the improvements.

[*http://www.elinux.org/Beagleboard:BeagleBoneBlack\#Software\_Resources*
](http://www.elinux.org/Beagleboard:BeagleBoneBlack#Software_Resources)

11.4.1 EDID 
------------

EDID is the way the board requests information from the display and
determines all the resolutions that it can support. The driver on the
board will then look at these timings and find the highest resolution
that is compatible with the board and uses that resolution for the
display. For more information on EDID, you can take a look at
[*http://en.wikipedia.org/wiki/Extended\_display\_identification\_data*
](http://en.wikipedia.org/wiki/Extended_display_identification_data)

If the board is not able to read the EDID, for whatever reason, it does
not have this information. A few possible reasons for this are:

-   Bad cable

-   Cable not plugged in all the way on both ends

-   Display not powered on. (It should still work powered off, but some
    displays do not).

11.4.2 DISPLAY SOURCE SELECTION 
--------------------------------

One easy thing to overlook is that you need to select the display source
that matches the port you are using on the TV. Some displays may auto
select, so you may need to disconnect the other inputs until you are
sure the display works with the board.

11.4.3 OUT OF SEQUENCE 
-----------------------

Sometimes the display and the board can get confused. One way to prevent
this is after everything is cabled up and running, you can power cycle
the display, with the board still running. You can also try resetting
the board and let it reboot to resync with the TV.

11.4.4 OVERSCAN 
----------------

Some displays use what is called overscan. This can be seen in TVs and
not so much on Monitors. It causes the image to be missing on the edges,
such that you cannot see them displayed. Some higher end displays allow
you to disable overscan.

Most TVs have a mode that allows you to adjust the image. These are
options like Normal, Wide, Zoom, or Fit. Normal seems to be the best
option as it does not chop of the edges. The other ones will crop of the
edges.

11.4.5 Taking a Nap 
--------------------

In some cases the board can come up in a power down/screen save mode. No
display will be present. This is due to the board believing that it is
asleep. To come out of this, you will need to hit the keyboard or move
the mouse.

Once working, the board will time out and go back to sleep again. This
can cause the display to go into a power down mode as well. You may need
to turn the display back on again. Sometimes, it may take a minute or so
for the display to catch up and show the image.

11.4.6 AUDIO 
-------------

Audio will only work on TV resolutions. This is due to the the way the
specification was written. Some displays have built in speakers and
others require external. Make sure you have a TV resolution and speakers
are connected if they are not built in. The SW should default to a TV
resolution giving audio support. The HDMI driver should default to the
highest audio supported resolution.

11.4.7 Getting Help 
--------------------

If you need some up to date troubleshooting techniques, we have a Wiki
set up at
[*http://circuitco.com/support/index.php?title=BeagleBoneBlack\_HDMI*
](http://circuitco.com/support/index.php?title=BeagleBoneBlack_HDMI)
