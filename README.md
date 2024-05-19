# Dela Eprommer I
 Recreated schematics, gerbers and original and translated software for the first version of the Dela Programmer for the Commodore 64.

![3d](https://github.com/BDelectrics/Dela-Eprommer-V1/assets/170223093/6cb0ce12-665c-4710-bc90-bf06d1432c04)

## Hardware
The hardware has been recreated as fas as possible. The traces are routed like the original where possible, but the original handdrawn style has not been recreated. The size for the PCB and connector is 1:1. The silkscreen are in most cases recreated.

As of the current date the recreated board has not been tested. I should not that the Z1 Zener diode should be 16V.

> [!WARNING]
> There are many more capable and compatible eprom-burners for the C64. Please research other alternatives before even considering this one. This repo is more for troubleshooting/conservation purposes.

## Software
I have provided both the original software and a crudely translated version to english.

## Instructions

For basic usage you can start the first program with LOAD"DE*",8,1 or you other prefered ways. The standard commands should be self explanatory. Note that when you are required to enter a starting adress you should use $1000 for the RAM and $0000 for the Eprom. In the monitor you can make small changes to the software when in ram. I have found the following commands in the Dela eprommer II-manual, but i can not guarantee that all will work:

| Command | Example |
| ---| --- |
| .$ | Convert HEX in DEC
| .= | Convert DEC in HEX
| .L Load | L"NAME",08 Loads program according to original address |
| .S Save | S "NAME",08,A-Adr.,E-Adr.+1 Saves program |
| .F Filling | F 1000 2000 FF - Fills memory from 1000 to 2000 with the value #FF. |
| .M Memory display | M 2000 or M 2000 2 100 - displays the range in hexadecimal and decimal respectively |
| .D Disassemble | D 1000 or D 1000 1100 - Disassembles the range from $1000 |
| .T Transfer | T 1000 2000 4000 Moves the range from 1000 to 2000 after 4000 |
| .G Go | G 1000 - Starts a program from address 1000 |
| .H Hunt | H 2000 3000 45 46 47 - Searches the range from 2000 to 3000 using the byte sequence 45 46 47 |
| .N New locate | N 4000 5000 3000 1000 2000 - After moving a memory area to another, this function recalculates the absolute jump addresses so that the program is then ready to run. |


If you are a native german speaker and can help with the translations, then please send a pull request or open an issue.

## Thanks

Thanks to use @Commander at Forum64.de for uploading the original software.

You should also check out the project by Commodore-Bench https://github.com/Commodore-Bench/DELA-EPROMMER-II
And manuals uploaded to archive at https://archive.org/details/dela-eprommer-ii-software-eng-den
