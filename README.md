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

[Elliott Sound Products]: http://sound-au.com/project06.htm
[Schematic]: ../master/phonopreamp.pdf
[LICENSE]: ../master/COPYING
[changelog]: ../master/CHANGELOG
[render_small]: ../master/phonopreamp_small.png
[BOM]: ../master/phonopreamp/bom.txt
