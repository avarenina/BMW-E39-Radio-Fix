# BMW-E39-Radio-Fix
Those are the instruction on how to fix BMW radio that doesnt save settings, fm stations etc. The procedure is for BMW E39 and it probably can be applied to others.
This happens because the 24C16 memory chip (EEPROM) inside the radio is faulty. They fail because EEPROMs have a limited amount of 1 million read-write cycles which amounts to about 10 years of usage and because of this you are better to replace the chip than buy a used radio. I used a 24LC16, which is slightly different than a 24C16, but it is a direct replacement for 24C16. I have purchased one at a local electronic store for about 10 HRK [1.5$].

If you think that you dont have enough knowledge about electronics to desolder and solder chips then give these instructions to your favourite electronic repair shop.

Instructions:
1. Remove the radio from the car. This is a fairly simple so I will not describe it in detail.
2. Open the top and bottom lid and remove the tape/cd mechanizm from it.
3. The 24C16 chip should be located below the tape/cd mechanism. Its a standard DIP-8 IC and its the only one on the whole board so its kind of hard to miss it. See image below for reference.
4. Remove the 24C16 IC. You need to have good desoldering skills for this. CAUTION: Do not damage the IC or board.
5. Use EEPROM programmer to read the contents of the chip that you just removed from the board and save it to your PC. If you somehow managed to damage the IC and you are unable to read its contents I have provided contents of my 24C16 IC here. I am not sure that the contents of my chip will work on your radio because they contain configuration data including serial number but its worth a shot. The file is "BMW_Radio_24_C_16.bin".
6. Use EEPROM programmer to write those contents on a new 24C16/24LC16 chip.
7. Solder the new chip to the board. Make sure that the orientation of the chip is correct.
8. Reassemble the radio and test it in your car.

Note: To read and write EEPROMs I have used EEPROM programmer CH341A. I bought one on ebay for about 3$. If you need tutorial and drivers just google "CH341A" and you will find a lot of info on it.

Chip contents:
https://github.com/avarenina/BMW-E39-Radio-Fix/blob/master/BMW_Radio_24_C_16.bin

Chip location on board:
![alt text](https://github.com/avarenina/BMW-E39-Radio-Fix/blob/master/24C16_location.jpg)
