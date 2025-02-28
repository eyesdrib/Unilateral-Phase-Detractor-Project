This document explains the installation and operation the Unilateral Phase Detractor, that draws shapes
on an oscilloscope.

Unzip the __UPD.zip file and transfer it to your computer. The UPD was designed on and for a Raspberry Pi,
running RaspberryPiOS, so I don't know how to get it running on a Windows machine or a Mac.

You will needs a few things before you start.

Hardware:
A Korg NanoKontrol2 Midi controller
A USB audio interface connected to your Pi
PC Keyboard
PC mouse

Software:
The Zexy external (which UPD needs, you may use Deken under Help>Find Externals)
The Cyclone external (which UPD Needs, again use Deken to installation)
AConnectGUI (which is the program that hooks the NanoKontrol2 into the patch. type
		sudo apt-get install aconnectgui) 

To start the Unilateral Phase Detractor, type 
		sudo pd -alsamidi
			This will start Pd with the option to load with AconnectGUI.
	Go to the pulldown menu on your Pi, under Sound & Video, start AconnectGUI
	You will get a window that looks like this graphic https://community.linuxmint.com/software/view/aconnectgui
	but your devices will look very different.

NOW, LOAD "00_UPD-250205-updating.pd"

	Click the patch cable icon at the top and connect your NanoKontrol2_CTR arrow to the Pure Data Midi-In spigot,
	and you're ready to go.

The PNG image (KorgNanoKontrol2-UPD-shortcuts.png) in this package is a guide to what keyboard
and NanoKontrol2 keys, knobs and sliders do what. The YouTube video https://www.youtube.com/watch?v=mAHJvLyt0ug is
a handy guide to what the UPD can do.

Connect your audio outputs to your oscilloscope and when you turn on the DSP, you will hear a complex sound 
and your scope will show a rotating dodecahedron.

Pressing the "-" key will bring up the Lissajous generator. You can enter the Lissajous subpatch by clicking the 
	"pd lissajous" rectangle. And you may instead press the keys in the top row after "-" to select a few presets.
	
Pressing keys a thru l, q thru p and numerals from 1 thru 0 will apply different presets for the ComplexCurves
subpatch and moving sliders on the Nano will make changes as well. Opening "pd complexcurves" will show the complex
curves patch and numerous sliders you can move to make changes to the loaded pattern.

Pressing CAPITAL letters will switch you to the Cogs generator.

The bottom row of the keyboard will show various 3-D shapes designed by Derek Holzer, exceot for the "/" which draw 
"Unilateral Phase Detractor" on the scope.

The "`" key will bring up the Polygons subpatch on the scope, and turning knob 1 on the Nano will display
polygons with differing numbers of sides.

The "?" key will take you to "Syntheshape" and the top row of keys will change the parameters or you can
click the subpatch where you can make changes in Pd.

"/" will bring up the "sawfilter" subptch. Knob 1 changes the harmonics that make a sawtooth wave.

You may record the audio at any time by pressing the ">" button the Nano or "<" to stop. Messages on the 
console will show the nae of the recorded file, which will live in the __UPD folder.

If you're *really* having trouble, you can email me at henry.birdseye@gmail.com.









