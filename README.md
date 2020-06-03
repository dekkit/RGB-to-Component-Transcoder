# Dek's RGB-to-Component-Transcoder
A DIY RGB to Component Video Transcoder to make your own video conversion boxes. 

This schematic and associated PCB does not do any upscaling and is designed to support old CRT TVs that only have component video inputs (not RGB scart like in many european countries) and primarily as way to open up more output options for retro consoles using an external method (rather needing to directly modify the internal hardware).   


This schematic will not upscale a 240p signal. Many LCD tvs will not display a 240p picture through Component video in.


New versions (schematic, pcb files, test results etc) can be found here in the code repository
https://github.com/dekkit/RGB-to-Component-Transcoder

Versions: 
VA01  (initial prototype),
VA02  (fixes, after initial tests),   
VAxx  (future versions will be in their own folders)

If you want to want to get a bunch of PCBs manufactured - simply use the latest GERBER zip (ie Gerber_PCB_2020-04-10 17_26_57.zip) file.  Most manufacturers will provide an instant quote and typically is only be a few dollars plus postage (postage is most expensive part).   Or  use the schematic to build your own breadboard version.

Please feel free to copy, adapt and use as appropriate (public domain). If you do improve on this design, please provide an acknowledgement,  drop me a note / create an issue to let me know and share your results.

If you would like to develop your own version (customised for your specific video device, make a smaller SMD version), or simply to poke around to help further your own understanding  (pick up on any errors too!) - I used the free app EasyEDA - I've opened up the project to make it easiser to clone and adapt (see https://easyeda.com/dekkit/rgb-to-component-transcoder)


Dek.
29/5/2020

Acknowledgements to Ace, Zebidee and all variations available on the web which helped me get this far.
Also to https://www.retrorgb.com/ for most useful info on LM1881 and THS amps - it's an excellent resource highly recommended site.


FURTHER BACKGROUND

This schematic was intended to be used for consumer CRT TVs as another way to support RGB (particulary in retro video game consoles and arcade setups where crt tubes are getting harder to find/replace). It is designed to be used as an external device (outside of the system) rather be used as an internal mod.

Includes
- Audio pass through (to support the development of custom retro console cables)
- Additional variable resistors (trim pots) to attenuate incoming RGB signals and create an all-in-one style plug (useful for per retro console customisations ie snes pal).
- Composite Video to Composite Sync (to extract csync from normal composite video, in case a system does not natively output csync - like Super Nintentdo pal, or if you want to create an RGB Scart to Component transcoder)
- Mostly through-hole components to make it easier to assemble (except for the THS amp).


Design Note(s)

- Designed primarily as an external unit, input are assumed to be 75 ohm signals (hence the use of 75R resitors to ground). You may need to remove these if you intend to adapt this pcb and use it intenally.
- For arcade boards you will need to attenuate the RGB signals to a level that a normal consumer CRT will accept (ie 3-5V p-p down to 0.7V p-p) - this can be done altering the resistor values (google arcade to scart for more info and for recommended adjustments and warning -  this may damage your video hardware if not done correctly).


Materials - i've included the Bill of materials as a downloadable CSV.
- Used 1/4 watt resistors 5% (either ceramic or metallic - though many TV mods use ceramic, so use cermic if possible)
- Low voltage components are acceptable (ie I've been using 6.3v for the electrolytic cap without any issues)
- Monolythic ceramic capacitors were used (104, and 105 - again use metallic ones if ceramic is unavailable).

It has been designed to fit in a small DIY project box of dimensions 10cm x 6cm x 2.5cm (with screw holes aligned).  You can find these easily online or you can arrange a 3D print.


Initial successful testing (on version VA01 19/4/2020):
Snes (PAL), Dreamcast (NTSC), Arcade 60-in-1 Jamma PCB, Sega Saturn (PAL), Sega MegaDrive2 (PAL).

Note - on Playstation 1 (PAL) - I found this required a seperate 5v supply (as the 5v pin dropped to 3.18v underload) 

Warning
No Warranty provided /use at own risk. Will not be held liable for any damage (its free after all!).
Use quality video cables   (cheap imported video cables have all sorts of video interferences - keep cables short too!).  Also please review the issues section before building for any identified issues / work-arounds.

Please share, clone, improve and share again (pay it forward) - that way we can all benefit. 

This schematic and pcb(s) have been based on the many designs found on the web using the BA7230 chip and from plenty of own my trials and testing the outputs until i found a method and design i was comfortable with it.  Project was initiated after discovering that one of my crts was unable to be RGB modded but could be modded to support component video.

Hope you find it as useful as I have.
