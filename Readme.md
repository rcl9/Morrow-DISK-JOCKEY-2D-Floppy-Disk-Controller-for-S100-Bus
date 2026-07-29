# Morrow DISK JOCKEY 2D Floppy Disk Controller for S-100 Bus - A Historical Compendium & Snaphot of Technical Information

This repository was penned to capture my experience, memories and technical information about the early 1980's Morrow DISK JOCKEY 2D 8" floppy disk controller card for the S-100 bus as I was/am using with my Exidy Sorcerer computer. This information would have saved me two months of work if I had it in hand while bringing this system fully online again in recent times. 

<div style="text-align:center">
<img src="https://github.com/rcl9/Morrow-DJ2D-CPM-22-Recompile-From-Source/raw/main/Images/Morrow%20DJ2D%20S-100%20controller%20card.jpg" alt="" style="width:45%; height:auto;">     <img src="https://github.com/rcl9/Morrow-DJ2D-CPM-22-Recompile-From-Source/raw/main/Images/Morrow%20DJ2D%20Shugart%20800%208in%20floppy%20drive.jpg" alt="" style="width:45%; height:auto;">
</div>

The photos above show my Morrow DJ2D controller card (Model B Rev 2) and its associated "DISCUS 2D" Shugart 801R 8" Floppy Drive. Purchased July 1981 for US$899 from Mini Micro Mart, Syracuse NY. The firmware ROM is located at D000H and its RAM at D400H. The system is still functional and in active use today. That Shugart drive has turned out to be very reliable over the years and decades! Both have been recently recapped.

In this repository we will cover these topics:

- Retro-fitting the 1981 Morrow DJ2D card by replacing its tantalum capacitors, replacing the 12v regulator and adding a new large heatsink to the main 5v regulator.
- Recapping all of the capacitors in my related hardware.
- An explanation of how the Morrow DJ2D card in the Exidy Sorcerer was made to run in a stable manner.
- How to connect the Morrow DJ2D Card to a HxC Floppy Emulator via two different "50pin to 36pin" adapter boards.
- The capture and preservation of the two PROM chips on the Morrow DJ2D card.
- How and why the "Stepping Rate" was changed in the 2708 EPROM.
- A capture of the original 24k CP/M distribution disk that came with the Morrow DISCUS 2D system. 
- How system tracks are laid out for the Morrow DJ2D system.
- My '*diskdef*' definitions For '*CP/M Tools*' and '*Modified CP/M Tools*'.

## Restoring the System to "Fully Operational Status"

I went through a multi-month process to carefully restore my 1979 Exidy Sorcerer I, Exidy S-100 box, my various S-100 cards (in particular the DJ2D card and my 
1983-era [Light Speed 100](<https://github.com/rcl9/Integration-of-the-1983-DRC-Light-Speed-100-RAMdisk-S100-Board-With-Exidy-Sorcerer-CPM-2.2>) (LS-100) 256k S-100 RAMdisk board) as well as my six 8" floppy drives (Calcomp Model 143M DSDD (2), Siemens FDD100 SSDD (3) and Shugart SA801R ).

This is a short list of what I did in this restoration process:

- Morrow DJ2D S-100 floppy controller card: the tantalum capacitors were all replaced: 2.2uf (25v, 3, radial ), 2.2uf (25v, 6, axial), 33uf (2, axial). Axial tantalums are expensive. A new 12v regulator was installed due to it dying. 

- Exidy Sorcerer I: a replacement [switched mode PSU](<https://github.com/rcl9/Exidy-Sorcerer-New-Power-Supply>) and all tantalums were replaced with equivalents.

- Exidy "Ram-Pac" cartridge: in the past I had turned the Exidy 8k Rom-Pac into a 4K Ram-Pac to increase the memory in the computer from 48K to 52k. I replaced the tantalums and also replaced the aging 2K static RAM chips. 

- Exidy S-100 Box: 4700uf (35v, 2), 30000uf (25v, 1) and 6.8uf (25v, 2). I chose to keep its original linear power supply rather than change over to switched mode regulators, given its lower overall power requirements. 

- The six 8" floppy drive controller cards: replacement of the tantalums and some electrolytics. The individual parts list is too long to inline in this document. 

<div style="text-align:center">
<img src="/Images/Recapping Siemens FDD100 drive controller card.webp" alt="" style="width:75%; height:auto;">
</div>

<div style="text-align:center">
<img src="/Images/Recapping Siemens FDD100.webp" alt="" style="width:75%; height:auto;">
</div>

<div style="text-align:center">
<img src="/Images/Recapping Siemens FDD100 drives.webp" alt="" style="width:75%; height:auto;">
</div>

<div style="text-align:center">
<img src="/Images/Completed recapping of Siemens FDD100 drives.webp" alt="" style="width:75%; height:auto;">
</div>

- Shugart SA801R drive power supply: 5600uf (50v), 4700uf (25v), 470uf (25v), 5.6uf (50v) and 6.8uf (5v). This floppy drive has been 100% reliable from 1981 to date but I didn't want to take any more chances with the tantalums and electrolytics in its linear power supply. 

<div style="text-align:center">
<img src="/Images/Shugart SA801R drive power supply.webp" alt="" style="width:75%; height:auto;">
</div>

- Dual Calcomp Model 143M drives: replacement of the old shared linear power supply with a new Mean Well RD-125B switched mode supply which does +5v at 4.6A and +24v at 4.6A.

## An Augmented Heatsink for the DJ2D Card

Since purchase in 1981 the 5v regulator on the Morrow DJ2D card has run incredibly hot. I could literally cook an egg on it or burn my fingers. I was determined to resolve this issue once and for all so I came up with a concoction of add-on heat sinks, cobbled together from the parts I had removed from my Exidy Sorcerer and one metal binder clip. 

It will probably look confusing from the photos as how I came to create this multi-heatsink setup:

- The labelled "Butterfly heatsink" is a typical dual-wing 5v regulator heatsink with two mounting holes that I have bent flat one side (where I point out that the "heatsink is bent"). I have drawn a red line to show how the new shape of the heatsink from its side. 

- The larger "Old Sorcerer heatsink" is attached to the "Butterfly heatsink" via 2 screws + thermal paste.

- The "Butterfly heatsink" is then attached to the original DJ2D 5v regulator heatsink with a small metal binder clip and some thermal paste. You can also see that I connected the binder clip handle to the "Butterfly heatsink" with a small piece of copper wire to prevent it from shorting out with the motherboard. Also, I had to remove, shorten and then re-attach the two handle arms of the binder clips to work in this setup (which was a real pain!). 

<div style="text-align:center">
<img src="/Images/Heatsink %231.webp" alt="" style="width:75%; height:auto;">
</div>

<div style="text-align:center">
<img src="/Images/Heatsink %232.webp" alt="" style="width:75%; height:auto;">
</div>

<div style="text-align:center">
<img src="/Images/Heatsink %233.webp" alt="" style="width:75%; height:auto;">
</div>

I thought that this was quite a creative solution to a problem which has long plagued this board. Now it runs cool. The only problem with this setup is that it forces the card to sit at the front of the motherboard due to its excessive height. 

## Checking the Drive "Lead Screw" & Stepper Motor on Your 8in, 5-1/4" and 3.5" Floppy Drives

**WARNING** If your drives have "sat on the shelf" for a bit of time then I'd highly recommend that you try to manually turn the "Lead Screw" (which positions the heads in the drive via the attached stepper motor) before using the drive to be sure it has not locked up. I've encountered several cases where the screw has locked up in my drives due to age. What happens is that the lead screw shaft gets gummed up within the stepper motor. I've had this happen with my 40+ year old 8in, 5-1/4" and 3.5" drives, as well as the mechanism for a 2000s era CDROM drive. 

I've tended to find that my dual Calcomp Model 143M drives turn freely while my three Siemens FDD100 drives remain difficult to turn. 

What I chose to do is clean the shaft of the lead screws with a tooth brush and then apply *white lithium grease* to them, carefully worked-in so not to get on the R/W head. I also tried to drip some thin machine oil into the mechanism of the front/back stepper motor but in the ideal world I'd open them up and clean the internals properly (as the core issue at hand to resolve). 

## Making the Morrow DJ2D Card "Stable"

What stumped me for an extended period of time was why the card was unstable, but fully functional, at the Sorcerer's stock 2Mhz speed and especially at my extended [3.1Mhz speed-up](<https://github.com/rcl9/Exidy-Sorcerer-Hardware-Speedup-Modification>). The card and system would also become unstable if I put the DJ2D card on a S-100 extender card, or added in my LS-100 RAMdisk card, and/or added in my S-100 expander I/O card. 

<div style="text-align:center">
<img src="/Images/Debugging stability issue.webp" alt="" style="width:75%; height:auto;">
</div>

<div style="text-align:center">
<img src="/Images/Debugging stability issue %232.webp" alt="" style="width:75%; height:auto;">
</div>

It eventually came down to the following:

- I was thinking, for a long while, that this may be due to a bus termination issue given the oddities which happened when I added in my extra S-100 cards or changed their placement on the bus. The Exidy S-100 backplane has no termination, active or passive given how short it is (6 slots). However, this ended up being a red herring. I was all set to buy and build an active termination card but in reality that wasn't truly needed. Maybe it is needed but not at the 2Mhz Sorcerer CPU clock speed. 

- I noticed that some of the chips on the DJ2D card used a RC delay line on the S-100 signals coming into the card. Given the 45 year age of the overall system I was thinking that timing may have become skewed and/or these RC components going slightly out of spec. After swapping out every IC on the board (and testing them) one by one, I narrowed it down to 7A which is a 74LS10 NAND gate. It was also the chip furthest from the backplane.  What luck!

- While I was at it, I noticed that several chips had badly blackened legs. So, I decided to pry them out and sand the legs down. For the other half of the chips (other than the PROM, EPROM and some specialty chips), I just re-seated them in-place (by prying them up a bit then pressing them back down firmly). However, I did retest the card every few chips just in case I introduced more problems than I was actually fixing. 

- Against my long term common logic, I came to understand that I needed to enable one wait state for EPROM access by flipping on switch #7 of the DJ2D card. That helped a lot with the system stability. 

- After making those two changes, adding in a new 12v regulator, a heat sink and recapping the board, it has remained 100% functional and reliable to date. I've had this machine and card running for endless hours with no problems nor any hardware related crashes.

## Connecting the Morrow DJ2D Card to a HxC Floppy Emulator

I had purchased the [HxC Floppy Emulator](<https://hxc2001.com>) (revision C, SDCard version) in 2015 for use with my [Cypher Z80/68000](<https://github.com/rcl9/Cypher-Z80-68000-Single-Board-Computer-1984-by-Motel-Computers---History-and-Documentation>) system which handles 5-1/4" and 8" drives. That worked well. It provides functionality to emulate two 5-1/4" and/or 8" floppy drives. I can attest to the fact that it works very well but you need to be careful which version of firmware is used. 

After I got the Morrow DJ2D system running in a stable manner I turned my attention to getting it to work with the HxC Floppy Emulator.

1) The first issue at hand was to get a 1:1 system image of a bootable DJ2D disk which could be used as a boot HFE disk image with the HxC emulator. That took several months of work mainly due to the (a) stability issues mentioned above and (2) having to rebuild all of my knowledge and experience of running this system from 40+ years ago. Both of these issues have been solidly resolved. This work resulted in the process I outlined in [this tutorial](<https://github.com/rcl9/How-to-Create-CPM-Boot-Disks-From-Scratch-in-IMG--IMD-and-HFE-File-Formats>) to build new system boot image files from scratch, as well the other tutorial which explains how to build a Morrow system boot disk from [source files](<Morrow DISK JOCKEY 2D CP/M 2.2 "SYSGEN" Recompile From Source Files (For Exidy Sorcerer)>). 

2) The second issue was to be careful in my methods and understanding of connecting the old 1981-era 50-pin Shugart cable to the newer 36-pin Shugart connector on the HxC emulator. I have decades of experience doing this with my other computers and hence my slight hesitation. What I ended up doing was:
   
- Design and build my own 50pin-to-36pin Shugart adapter board. My version allowed for both the HxC emulator to be attached to the Morrow DJ2D card *as well as* another set of 8" floppy drives. I'd eventually test this as a working solution. I am providing my pin mapping in this [Excel spreadsheet](</50pin-to-36pin Shugart adapter board/RCL9's Shugart 34 pin to 50 pin mapping.xlsx>). 
   
- A short while later I purchased the "[fd50to34](<https://gitlab.com/NF6X_Retrocomputing/fd50to34>)" adapter PCB designed by Mark J. Blair nf6x@nf6x.net. It's design is a bit different than mine but still provides similar functionality. 
   
- Both of these adapter boards work very well. This only "gotcha" is that you need to be wary of the "2-sided" jumper. The Morrow DJ2D card cannot determine if a virtual disk in the HxC emulator is single sided or double sided and hence this jumper needs to be manually set. What I've come to do with my generated HxC HFE disk image files is to always make them double-sided. 

<div style="text-align:center">
<img src="/Images/Building the 50pinto36pin adapter board.webp" alt="" style="width:75%; height:auto;">
</div>

<div style="text-align:center">
<img src="/Images/RCL9's 50pinto36pin adapter board.webp" alt="" style="width:75%; height:auto;">
</div>

<div style="text-align:center">
<img src="/Images/Connecting HxC emulator to Sorcerer.webp" alt="" style="width:75%; height:auto;">
</div>

<div style="text-align:center">
<img src="/Images/Connecting HxC emulator to Sorcerer #2.webp" alt="" style="width:40%; height:auto;">
</div>

## Capturing the Two PROM Chip Contents

For years I've wanted to capture the contents of the two old 1970s era PROM chips on the Morrow DJ2D card, as a loss of them would cripple the board forever. The Boot PROM had been previously captured by others but not the unique Address PROM (D000 PROM # 8C) as used by the Exidy Sorcerer variation of the Morrow DJ2D card. I figured it was up to me to make that capture for historical posterity. However, I was a bit reluctant to do so just in case I (somehow) came to destroy the chip in the process. 

The following image shows how I connected my XGecu T48 EPROM programmer to each PROM chip for reading into the computer:

<div style="text-align:center">
<img src="/Images/Reading DJ2D PROMs.webp" alt="" style="width:75%; height:auto;">
</div>

I've put together an archive of files for reference by future retro-computing enthusiasts:

| File Name in ZIP File                                  | File Description      |
|:---------------------------------------------- |:---------------------------------------------- |
| PROM # 8C @D000 (Exidy Sorcerer).bin                   | The dump of 6301 PROM 8C which provides the D000 address decoding for the Exidy Sorcerer.                                                                                                                                                                              |
| PROM # 3D.bin                                          | The dump of 6331 PROM 3D which is identical to all DJ2D cards/                                                                                                                                                                                                         |
| 6301 PROM to 2716 EPROM Pin Mapping.pdf                | My technical notes about how to map from a 6301 PROM to a 2716 pinout to be used with an EPROM reader.                                                                                                                                                                 |
| 6331 PROM to 2716 EPROM Pin Mapping.pdf                | My technical notes about how to map from a 6331 PROM to a 2716 pinout to be used with an EPROM reader.                                                                                                                                                                 |
| 6301, PROM 8C, Address Decoding Verification Table.pdf | To understand how the 256-vector encoding is performed with PROM # 8C, and to verify that everything is okay, I created the logic table in this file to alieviate any concerns that I may have had. Everything checks out fine for the D000, E000 and F800 PROM dumps. |
| PROM types.txt                                         | Some of my general notes about the 6301 and 6331 PROM ICs.                                                                                                                                                                                                             |

<div style="text-align:center">
<img src="/DJ2D PROMs/Schematic -- 6301 -- 8C.webp" alt="" style="width:45%; height:auto;">     <img src="/DJ2D PROMs/Schematic -- 6331 -- 3D.webp" alt="" style="width:45%; height:auto;">
</div>

## My "Stepping Rate" Change (Minor)

For my and others reference, back in the day I burned a new 2708 EPROM to change the stepping rate from 3.6ms to 10ms. This was done by changing the "1F, 1F, 1F" to "3E 01 00" at offset 0x248. This may have been done for my then-new dual Calcomp DSDD 8" drives. The original 3.6ms stepping rate had been chosen by Morrow for the Shugart SA801R drive.

The three '1F' values are 8080 'RAR' opcodes to do shifts, resulting in a 3.6ms stepping rate.  The new "3E 01 00" values translates to loading the A register with 01. 

## Original 24k CP/M Distribution Disk

Documenting the Morrow DJ2D card would not be complete without a copy of the original 24k CP/M 2.2  boot disk as set up for the Exidy Sorcerer. I am providing a copy of that in the associated [ZIP file](</Original Morrow 24k CPM 2.2 boot disk for Exidy Sorcerer/Original Morrow 24k CPM 2.2 boot disk for Exidy Sorcerer.zip>). 

The ZIP file also contains *cpm24k_SS_CBios3.1.sys* which is a capture of the first two system boot tracks of the 24k distribution disk.  If you are ever having trouble with your Morrow DJ2D system then I'd suggest starting with this simplified 24k system as I had done with my several months of system testing. Please note that it uses non-optimized character I/O and hence it tends to be slow when outputting text such as disk directory listings. 

## How System Tracks Are Laid Out For the Morrow DJ2D System

For quick reference, my other [Morrow DJ2D technical article](<https://github.com/rcl9/How-to-Create-CPM-Boot-Disks-From-Scratch-in-IMG--IMD-and-HFE-File-Formats>) explains the disk format and layout of single-sided and double-sided Morrow DJ2D disks. Basically track 0 is in single density (FM, 16 sectors of 128 bytes) and the remainder of the tracks are in double density (MFM, 8 sectors of 1024 bytes). 

For double sided disks, the Morrow DJ2D card only reads the system boot image from the first side and not interleaved with the second side. This confused me for a while before I did some disk-level sleuthing. 

This is "simple" knowledge that I wish I fully understood months ago. 

## My 'diskdef' Definitions For 'CP/M Tools' and 'Modified CP/M Tools'

The [Morrow DJ2D technical article](<https://github.com/rcl9/How-to-Create-CPM-Boot-Disks-From-Scratch-in-IMG--IMD-and-HFE-File-Formats>) provides copies of my special CPMTools 'diskdefs' for the Morrow DJ2D card as well as custom single/double-sided "B2I" (binary-to-IMD) configuration files for the 32-bit version of ImageDisk. 

## See Also

[Morrow DJ2D S-100 floppy controller](<https://www.retrotechnology.com/herbs_stuff/morrow_dj2d.html>) - This is a definitive go-site for information relating to the Morrow DJ2D card. I have contributed my PROM chip images to the site.

[Morrow DISK JOCKEY 2D CP/M 2.2 "SYSGEN" Recompile From Source Files (For Exidy Sorcerer)](<Morrow DISK JOCKEY 2D CP/M 2.2 "SYSGEN" Recompile From Source Files (For Exidy Sorcerer)>)

[How to Create Mixed-Mode Geometry CP/M Boot Disks From Scratch in IMG, IMD and HFE File Formats](<https://github.com/rcl9/How-to-Create-CPM-Boot-Disks-From-Scratch-in-IMG--IMD-and-HFE-File-Formats>)

[Hex File Overlayer Utility for CP/M 2.2 SYSGEN Image Files](https://github.com/rcl9/Hex-File-Overlayer-of-CPM-Sysgen-Image)
