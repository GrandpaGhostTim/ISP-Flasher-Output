# ISP-Flasher-Output

C:\Users\Tim\Documents\Arduino>avrdude -p m32u4 -c avrisp -P com4 -b 19200 -e -v

avrdude: Version 6.0.1, compiled on Oct 17 2013 at 21:37:20
         Copyright (c) 2000-2005 Brian Dean, http://www.bdmicro.com/
         Copyright (c) 2007-2009 Joerg Wunsch

         System wide configuration file is "C:\Program Files (x86)\MHV AVR Tools\bin\avrdude.conf"

         Using Port                    : com4
         Using Programmer              : avrisp
         Overriding Baud Rate          : 19200
         AVR Part                      : ATmega32U4
         Chip Erase delay              : 9000 us
         PAGEL                         : PD7
         BS2                           : PA0
         RESET disposition             : dedicated
         RETRY pulse                   : SCK
         serial program mode           : yes
         parallel program mode         : yes
         Timeout                       : 200
         StabDelay                     : 100
         CmdexeDelay                   : 25
         SyncLoops                     : 32
         ByteDelay                     : 0
         PollIndex                     : 3
         PollValue                     : 0x53
         Memory Detail                 :

                                  Block Poll               Page                       Polled
           Memory Type Mode Delay Size  Indx Paged  Size   Size #Pages MinW  MaxW   ReadBack
           ----------- ---- ----- ----- ---- ------ ------ ---- ------ ----- ----- ---------
           eeprom        65    20     4    0 no       1024    4      0  9000  9000 0x00 0x00
           flash         65     6   128    0 yes     32768  128    256  4500  4500 0x00 0x00
           lfuse          0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           hfuse          0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           efuse          0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           lock           0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           calibration    0     0     0    0 no          1    0      0     0     0 0x00 0x00
           signature      0     0     0    0 no          3    0      0     0     0 0x00 0x00

         Programmer Type : STK500
         Description     : Atmel AVR ISP
         Hardware Version: 2
         Firmware Version: 1.18
         Topcard         : Unknown
         Vtarget         : 0.0 V
         Varef           : 0.0 V
         Oscillator      : Off
         SCK period      : 0.1 us

avrdude: AVR device initialized and ready to accept instructions

Reading | ################################################## | 100% 0.05s

avrdude: Device signature = 0x1e9587
avrdude: safemode: lfuse reads as 5E
avrdude: safemode: hfuse reads as 99
avrdude: safemode: efuse reads as F3
avrdude: erasing chip

avrdude: safemode: lfuse reads as 5E
avrdude: safemode: hfuse reads as 99
avrdude: safemode: efuse reads as F3
avrdude: safemode: Fuses OK (H:F3, E:99, L:5E)

avrdude done.  Thank you.


C:\Users\Tim\Documents\Arduino>avrdude -p m32u4 -c avrisp -P com4 -b 19200 -U lfuse:w:0xff:m -U hfuse:w:0xd8:m -U efuse:w:0xc9:m -v

avrdude: Version 6.0.1, compiled on Oct 17 2013 at 21:37:20
         Copyright (c) 2000-2005 Brian Dean, http://www.bdmicro.com/
         Copyright (c) 2007-2009 Joerg Wunsch

         System wide configuration file is "C:\Program Files (x86)\MHV AVR Tools\bin\avrdude.conf"

         Using Port                    : com4
         Using Programmer              : avrisp
         Overriding Baud Rate          : 19200
         AVR Part                      : ATmega32U4
         Chip Erase delay              : 9000 us
         PAGEL                         : PD7
         BS2                           : PA0
         RESET disposition             : dedicated
         RETRY pulse                   : SCK
         serial program mode           : yes
         parallel program mode         : yes
         Timeout                       : 200
         StabDelay                     : 100
         CmdexeDelay                   : 25
         SyncLoops                     : 32
         ByteDelay                     : 0
         PollIndex                     : 3
         PollValue                     : 0x53
         Memory Detail                 :

                                  Block Poll               Page                       Polled
           Memory Type Mode Delay Size  Indx Paged  Size   Size #Pages MinW  MaxW   ReadBack
           ----------- ---- ----- ----- ---- ------ ------ ---- ------ ----- ----- ---------
           eeprom        65    20     4    0 no       1024    4      0  9000  9000 0x00 0x00
           flash         65     6   128    0 yes     32768  128    256  4500  4500 0x00 0x00
           lfuse          0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           hfuse          0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           efuse          0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           lock           0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           calibration    0     0     0    0 no          1    0      0     0     0 0x00 0x00
           signature      0     0     0    0 no          3    0      0     0     0 0x00 0x00

         Programmer Type : STK500
         Description     : Atmel AVR ISP
         Hardware Version: 2
         Firmware Version: 1.18
         Topcard         : Unknown
         Vtarget         : 0.0 V
         Varef           : 0.0 V
         Oscillator      : Off
         SCK period      : 0.1 us

avrdude: AVR device initialized and ready to accept instructions

Reading | ################################################## | 100% 0.05s

avrdude: Device signature = 0x1e9587
avrdude: safemode: lfuse reads as 5E
avrdude: safemode: hfuse reads as 99
avrdude: safemode: efuse reads as F3
avrdude: reading input file "0xff"
avrdude: writing lfuse (1 bytes):

Writing | ################################################## | 100% 0.03s

avrdude: 1 bytes of lfuse written
avrdude: verifying lfuse memory against 0xff:
avrdude: load data lfuse data from input file 0xff:
avrdude: input file 0xff contains 1 bytes
avrdude: reading on-chip lfuse data:

Reading | ################################################## | 100% 0.02s

avrdude: verifying ...
avrdude: 1 bytes of lfuse verified
avrdude: reading input file "0xd8"
avrdude: writing hfuse (1 bytes):

Writing | ################################################## | 100% 0.04s

avrdude: 1 bytes of hfuse written
avrdude: verifying hfuse memory against 0xd8:
avrdude: load data hfuse data from input file 0xd8:
avrdude: input file 0xd8 contains 1 bytes
avrdude: reading on-chip hfuse data:

Reading | ################################################## | 100% 0.02s

avrdude: verifying ...
avrdude: 1 bytes of hfuse verified
avrdude: reading input file "0xc9"
avrdude: writing efuse (1 bytes):

Writing | ################################################## | 100% 0.03s

avrdude: 1 bytes of efuse written
avrdude: verifying efuse memory against 0xc9:
avrdude: load data efuse data from input file 0xc9:
avrdude: input file 0xc9 contains 1 bytes
avrdude: reading on-chip efuse data:

Reading | ################################################## | 100% 0.02s

avrdude: verifying ...
avrdude: 1 bytes of efuse verified

avrdude: safemode: lfuse reads as FF
avrdude: safemode: hfuse reads as D8
avrdude: safemode: efuse reads as C9
avrdude: safemode: Fuses OK (H:C9, E:D8, L:FF)

avrdude done.  Thank you.


C:\Users\Tim\Documents\Arduino>avrdude -p m32u4 -c avrisp -P com4 -b 19200 -B 4 -U flash:w:"planck_rev4_default_bootloader.hex" -v

avrdude: Version 6.0.1, compiled on Oct 17 2013 at 21:37:20
         Copyright (c) 2000-2005 Brian Dean, http://www.bdmicro.com/
         Copyright (c) 2007-2009 Joerg Wunsch

         System wide configuration file is "C:\Program Files (x86)\MHV AVR Tools\bin\avrdude.conf"

         Using Port                    : com4
         Using Programmer              : avrisp
         Overriding Baud Rate          : 19200
         Setting bit clk period        : 4.0
         AVR Part                      : ATmega32U4
         Chip Erase delay              : 9000 us
         PAGEL                         : PD7
         BS2                           : PA0
         RESET disposition             : dedicated
         RETRY pulse                   : SCK
         serial program mode           : yes
         parallel program mode         : yes
         Timeout                       : 200
         StabDelay                     : 100
         CmdexeDelay                   : 25
         SyncLoops                     : 32
         ByteDelay                     : 0
         PollIndex                     : 3
         PollValue                     : 0x53
         Memory Detail                 :

                                  Block Poll               Page                       Polled
           Memory Type Mode Delay Size  Indx Paged  Size   Size #Pages MinW  MaxW   ReadBack
           ----------- ---- ----- ----- ---- ------ ------ ---- ------ ----- ----- ---------
           eeprom        65    20     4    0 no       1024    4      0  9000  9000 0x00 0x00
           flash         65     6   128    0 yes     32768  128    256  4500  4500 0x00 0x00
           lfuse          0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           hfuse          0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           efuse          0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           lock           0     0     0    0 no          1    0      0  9000  9000 0x00 0x00
           calibration    0     0     0    0 no          1    0      0     0     0 0x00 0x00
           signature      0     0     0    0 no          3    0      0     0     0 0x00 0x00

         Programmer Type : STK500
         Description     : Atmel AVR ISP
         Hardware Version: 2
         Firmware Version: 1.18
         Topcard         : Unknown
         Vtarget         : 0.0 V
         Varef           : 0.0 V
         Oscillator      : Off
         SCK period      : 0.1 us

avrdude: AVR device initialized and ready to accept instructions

Reading | ################################################## | 100% 0.04s

avrdude: Device signature = 0x1e9587
avrdude: safemode: lfuse reads as FF
avrdude: safemode: hfuse reads as D8
avrdude: safemode: efuse reads as C9
avrdude: NOTE: "flash" memory has been specified, an erase cycle will be performed
         To disable this feature, specify the -D option.
avrdude: erasing chip
avrdude: reading input file "planck_rev4_default_bootloader.hex"
avrdude: input file planck_rev4_default_bootloader.hex auto detected as Intel Hex
avrdude: writing flash (32768 bytes):

Writing | ################################################## | 100% 30.06s

avrdude: 32768 bytes of flash written
avrdude: verifying flash memory against planck_rev4_default_bootloader.hex:
avrdude: load data flash data from input file planck_rev4_default_bootloader.hex:
avrdude: input file planck_rev4_default_bootloader.hex auto detected as Intel Hex
avrdude: input file planck_rev4_default_bootloader.hex contains 32768 bytes
avrdude: reading on-chip flash data:

Reading | ################################################## | 100% 17.11s

avrdude: verifying ...
avrdude: 32768 bytes of flash verified

avrdude: safemode: lfuse reads as FF
avrdude: safemode: hfuse reads as D8
avrdude: safemode: efuse reads as C9
avrdude: safemode: Fuses OK (H:C9, E:D8, L:FF)

avrdude done.  Thank you.
