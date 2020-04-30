# PA1-P06 phono preamplifier

This is my spin on the well known [Elliott Sound Products] "Project 06" phono preamp, with integrated power supply, a couple modifications, and an acrylic sandwich enclosure.

[LICENSE] NOTE: The original ESP P06 is not licensed for reuse in any way. This variant uses only the filter chain topology and component values, neither of which are directly copyrightable, but **please** respect the original designer's (and my) wishes: my version is licensed CC BY-NC-SA, that is the most restrictive of all Creative Commons licenses and forbids commercial use even if you were to follow all the usual open-source rules! Both ESP and I are explicitly requesting you not make money off this design. It's not terribly hard to figure out how to implement the RIAA curves for yourself if you want a commercial product. Don't mooch, filthy capitalist pigs.

The CAD files were created with a development build of KiCad from April 2020; a release build may not load them properly.

[![3D render][render_small]](../master/phonopreamp.png)

- [Schematic]
- [BOM] in Digi-Key bulk add format

## Revision B

This repository includes a Revision B, which I have not yet actually built. See the [changelog] for more information.

## Gerbers

Gerbers currently don't exist in this repository. Recent KiCad builds have had a bug with Gerber export that bit me when I was having this board made and I don't want to go posting files until I'm more confident. Generate yourself, at your own risk.

## Assembly tips

- The mounting screw near the input jacks is meant to be the anchor point for a ground wire. I added a solder lug and heatshrink to the phono ground lead, then put the lug between screw and washer in that corner.
- Build the board as a sandwich: M3×0.5 screw, through nylon or fiber washer (I used [RPC10339-ND]), through acrylic base plate, into short standoff, through PCB, into long standoff (see BOM). From the top, M3×0.5 screw, through washer, through acrylic top plate, into standoff. On the ground terminal corner, the ground lug goes between the top screw and washer.
    - Washers are necessary to prevent _cracking_ the acrylic (I'm not just being picky about scratches), and should be soft washers. These will give slightly if the screws are over-tightened, both preventing excessive pressure on the acrylic, as well as compressing to lock the screws in place better.
    - Short standoffs are omitted from BOM because I ordered the wrong ones and improvized with a couple nuts — I don't have a part number. They should be about 5mm long.
- The PPS film capacitors are, to be polite, a complete bitch to stuff. They're basically unsolderable as they melt easily, and are moisture sensitive too. The method I used is: assemble entire board except these using water soluble flux; wash very well to keep clean. Carefully spot-solder film capacitors with no-clean flux, low temperature, quickly, being careful not to touch the sides with the iron, squish with tweezers, or keep hot too long. Do not wash.
    - If you don't care about cleaning the flux, just use no-clean for the whole board and resist any temptation to clean it.

### Assembled stack:

```
|>----    |    ##    [===]---    ##    [===============]    ##    |          -----<|
               ##                ##                         ##
               ##                ##                         ##
               ##                ##                         ##
               ##                ##                         ##
               ##                ##                         ##
|>----    |    ##    [===]---    ##    [===============]    ##    |    ||    -----<|

^         ^    ^     ^           ^     ^                    ^     ^    ^     ^
|         |    |     |           |     |                    |     |    |     M3×0.5 screws
|         |    |     |           |     |                    |     |    ground lug (input corner only)
|         |    |     |           |     |                    |     nylon washers
|         |    |     |           |     |                    top acrylic plate
|         |    |     |           PCB   long F-F standoffs
|         |    |     short F-M standoffs
|         |    bottom acrylic plate
|         nylon washers
M3×0.5 screws
```

[Elliott Sound Products]: http://sound-au.com/project06.htm
[Schematic]: ../master/phonopreamp.pdf
[LICENSE]: ../master/COPYING
[changelog]: ../master/CHANGELOG
[render_small]: ../master/phonopreamp_small.png
[BOM]: ../master/phonopreamp/bom.txt
[RPC10339-ND]: https://www.digikey.com/product-detail/en/essentra-components/16M03080080/RPC10339-ND/10299235
