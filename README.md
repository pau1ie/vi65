# vi65
I am attempting to port vi65 to the BBC Micro.

Thanks to Soci/Singular for creating a vi clone for the 6502,
and licensing it under the GPL so I could port it.

To compile:
* Install the following:
  * perl
  * python 2.7
* Download and install the 64tass assembler: http://sourceforge.net/projects/tass64/
* Update the Makefile with its location TASS= at the top
* Download upd-inf.sh from https://github.com/crtc-demos/sugarsmash/blob/master/update-inf.sh and place it in the build directory
* Download https://github.com/sweharris/MMB_Utils
* Update bbc.sh (PATH in the top line) with this location (~/Programs/mmb)
* type make
* Download b-em from https://github.com/stardot/b-em


I got vi65 from here: https://sourceforge.net/projects/vi65/

This is a very early version of the port. It loads and commands can be typed etc, but there are serious limitations:
* It only works in mode 7, which must be selected before running the program.
* Arrow keys don't work (Just need to change the mode)
* Loading doesn't work
* Saving doesn't work
* Quitting doesn't work
* Screen updates (Apart from the cursor) are done directly to RAM rather than through the OS.
* Like many games it rudely overwrites BASIC memory, so will need CTRL-BREAK to exit (This is why quitting doesn't work)
* The build process could be friendlier

