# OpenAmiga600FastRamExpansion
OpenAmiga600FastRamExpansion is an Open Hardware 4 MB Fast RAM Expansion for the Commodore Amiga 600 Computer.

![Board](https://raw.githubusercontent.com/SukkoPera/OpenAmiga600FastRamExpansion/master/doc/render-top.png)

### Summary
TBD

#### Memory
The required RAM Type is 16 Mbit (1M×16) DRAM in the SOJ-42 package with up to 70-80 ns access time. It is 5v-only DRAM (not SD(!)RAM) found often in old 72-pin SIMMs, EDO chips might work or not. All chips having *8160* in their part number should be OK.

|Model         |Maker           |Tested                                                                              |Working                                                                               |Data Sheet                                                                                                                                                                 |Notes                                                                                |
|--------------|----------------|:----------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|-------------------------------------------------------------------------------------|
|GM71C18160    |Hynix        |![No](doc/no.png)  |                                                                                      |[![PDF](doc/doc.png)](https://github.com/lvd2/A600_8mb_2008/blob/master/DRAM_datasheets/GM71C18160.pdf)                               |                                                                                     |
|MSM5118160    |OKI          |![Yes](doc/yes.png)|![Yes](doc/yes.png)  |[![PDF](doc/doc.png)](https://github.com/lvd2/A600_8mb_2008/blob/master/DRAM_datasheets/msm5118160.pdf)      |                                                                                     |

Normally it is not necessary to mount all the decoupling capacitors. I usually skip C4 and C7. All of them are 100nF in the 0805 package anyway. An additional 10uF electrolytic capacitor can be mounted at C13, if needed.

RAM chips can either be soldered directly on the board or installed in sockets. While soldering the chips might not be trivial for the unexperienced, sockets for the SOJ-42 package are hard to find and not really easier to solder either, so the choice is up to you.

### Assembly and Installation
Open your A600, doing your best not to crack any of the small tabs that hold the case together.

Before soldering the CPU socket you will need to rework it a bit: you should sand down one of its edges which will hit resistor R102 that is present in REV 1.5 boards (at least), so try to fit it on the CPU (a large square chip with *MC68000* written on it) and see which corner it is. Make sure to match the correct orientation: one of the corners of the chip is cut and if you look at the socket, one of its corners will match that cut.

Besides that, most PLCC sockets have some sort of "stand-offs" on the bottom (which is going to be our top), which you are recommended to sand down, too. This should all make the socket fit better on the chip. Remember that the fitting of this kind of expansions is quite a hack and might not even work in all cases.

After everything has been soldered, just install the expansion. Push it down firmly until it feels solidly in place but don't force it.

Before reassembling your case, I recommend to run [SysTest](https://github.com/keirf/Amiga-Stuff). Use the Memory option (<kbd>F1</kbd>), it must show 4 MB of Fast RAM. Then start the Memory Test (<kbd>F1</kbd> again) and let it run for 50-100 rounds: if it doesn't find any errors, you are probably good to go. If you get any errors, power off your computer and try to give the expansion a better fit, by pushing it slightly more or twisting it back and forth a bit.

It might happen that the board slowly works its way out of the socket over time. To avoid this you can anchor it to the mainboard using the hole to the left of the CPU, which should align with one of the holes for the HD cradle legs.

Oh and no, there's no way you can place the HD cradle back into the case, sorry.

### License
The OpenAmiga600FastRamExpansion documentation, including the design itself, is copyright &copy; SukkoPera 2019.

OpenAmiga600FastRamExpansion is Open Hardware licensed under the [CERN OHL v. 1.2](http://ohwr.org/cernohl).

You may redistribute and modify this documentation under the terms of the CERN OHL v.1.2. This documentation is distributed *as is* and WITHOUT ANY EXPRESS OR IMPLIED WARRANTIES whatsoever with respect to its functionality, operability or use, including, without limitation, any implied warranties OF MERCHANTABILITY, SATISFACTORY QUALITY, FITNESS FOR A PARTICULAR PURPOSE or infringement. We expressly disclaim any liability whatsoever for any direct, indirect, consequential, incidental or special damages, including, without limitation, lost revenues, lost profits, losses resulting from business interruption or loss of data, regardless of the form of action or legal theory under which the liability may be asserted, even if advised of the possibility or likelihood of such damages.

A copy of the full license is included in file [LICENSE.pdf](LICENSE.pdf), please refer to it for applicable conditions. In order to properly deal with its terms, please see file [LICENSE_HOWTO.pdf](LICENSE_HOWTO.pdf).

The contact points for information about manufactured Products (see section 4.2) are listed in file [PRODUCT.md](PRODUCT.md).

Any modifications made by Licensees (see section 3.4.b) shall be recorded in file [CHANGES.md](CHANGES.md).

The Documentation Location of the original project is https://github.com/SukkoPera/OpenAmiga600FastRamExpansion/.

### Support the Project
Since the project is open you are free to get the PCBs made by your preferred manufacturer, however in case you want to support the development, you can order them from PCBWay through this link:

[![PCB from PCBWay](https://www.pcbway.com/project/img/images/frompcbway.png)](https://www.pcbway.com/project/shareproject/OpenAmiga600FastRamExpansion_V1.html)

You get my gratitude and cheap, professionally-made and good quality PCBs, I get some credit that will help with this and [other projects](https://www.pcbway.com/project/member/shareproject/?bmbid=41100). You won't even have to worry about the various PCB options, it's all pre-configured for you!

Also, if you still have to register to that site, [you can use this link](https://www.pcbway.com/setinvite.aspx?inviteid=41100) to get some bonus initial credit (and yield me some more).

Again, if you want to use another manufacturer, feel free to, don't feel obligated :).

### Get Help
If you need help or have questions, you can join [the official Telegram group](https://t.me/joinchat/HUHdWBC9J9JnYIrvTYfZmg).

### Thanks
- lvd for the initial design
- Kipper2K for making his boards
- majinga for helping with the testing
