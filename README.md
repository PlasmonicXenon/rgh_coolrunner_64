# RGH_Coolrunner_64
This is an approximate replica of the coolrunner rev C based on the clones I 
have, but with a few extra features.

The extra features include solder points for level shifting post, an extra pll
io pad, as well as a crowbar point and a nand chip enable point for a potential
future Oban voltage glitch, if that ever happens and is ported to the xc2c64.

Note that the post points do not exactly match the configuration Octal450's 
level_shifter uses, which isn't a problem for my usecase.  If one wants to
use level_shifter, either edit the UCF file or wire to match it.

As mentioned above, this pcb has two IO pads that can drive the PLL point -- the
usual 3v3 io pad through a 22k resistor as usual, and an IO pad in the CPU VCCIO
bank. This second pad is only intended to be used with slims because the 
coolrunner  II's lowest IO voltage is 1.5V whereas phat CPUs use V_GPUCORE 
(~1.1 V) as their  IO voltage.  The intent here is that driving PLL_BYPASS with
a lower impedance should reduce its sensitivity to interference. 
