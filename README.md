# RGH_Coolrunner_64
This is an approximate replica of the coolrunner rev C based on the clones I 
have, but with a few extra features.

The extra features include solder points for level shifting post as well as a
crowbar point and a nand chip enable point for a potential future Oban voltage
glitch, if that ever happens and is ported to the xc2c64.

Note that the post pads do not exactly match the configuration Octal450's 
level_shifter uses, which isn't a problem for my usecase.  If one wants to
use level_shifter, either edit the UCF file or wire to match it.
