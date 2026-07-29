The impetus of this archive was simply to capture the custom address decoder 6301 PROM IC #8C (4 x 256) from the early 1980's Morrow DiskJockey 2D-B Rev-2 S-100 floppy disk controller card and add it to the previous E000 and F800 collection provided on Herb Johnson's Morrow DJ2D info page. This PROM is unique as it is from the Exidy Sorcerer which has the DJ2D memory mapped to D000.

	https://www.retrotechnology.com/herbs_stuff/morrow_dj2d.html

I had purchased this Morrow 8in disk system in 1981 to be used along with my S-100 expansion box for the Exidy Sorcerer.

My contact info (RCL9): RetroComputingArchive@gmail.com   

File List Overview
=-=-=-=-=-=-=-

Exidy Sorcerer, DJ2D PROM dumps @ D000 by RCL9 

	RCL9's  PROM # 3D.bin
		The dump of 6331 PROM 3D which is identical to all DJ2D cards
		
	RCL9's  PROM # 8C @D000 (Exidy Sorcerer).bin
		The dump of 6301 PROM 8C which provides the D000 address decoding for the Exidy Sorcerer. 

	6301 PROM to 2716 EPROM Pin Mapping.pdf
		My technical notes about how to map from a 6301 PROM to a 2716 pinout to be used with an EPROM reader

	6331 PROM to 2716 EPROM Pin Mapping.pdf
		My technical notes about how to map from a 6331 PROM to a 2716 pinout to be used with an EPROM reader

	6301, PROM 8C, Address Decoding Verification Table.pdf
		To understand how the 256-vector encoding is performed, and to verify that everything is okay, I created the logic table in this file to alieviate any concerns that I may have had. Everything checks out fine for the D000, E000 and F800 PROM dumps.

	PROM types.txt
		Some of my general notes about the 6301 and 6331 PROM ICs.

	Schematic -- 6301 -- 8C.webp
	Schematic -- 6331 -- 3D.webp
		Captures of the two PROM chips from the Morrow DJ2D schematics.
