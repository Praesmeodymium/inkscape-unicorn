MakerBot Unicorn G-Code Output for Inkscape
===========================================

This is an Inkscape extension that allows you to save your Inkscape drawings as
G-Code files suitable for plotting with Marlin Compatible systems.
Author: [Ian Hoff] With most of the heavy lifting by (http://github.com/martymcguire)

Credits
=======

* Marty McGuire pulled this all together into an Inkscape extension.
* [Inkscape](http://www.inkscape.org/) is an awesome open source vector graphics app.
* [Scribbles](https://github.com/makerbot/Makerbot/tree/master/Unicorn/Scribbles%20Scripts) is the original DXF-to-Unicorn Python script.
* [The Egg-Bot Driver for Inkscape](http://code.google.com/p/eggbotcode/) provided inspiration and good examples for working with Inkscape's extensions API.

Install
=======

Copy the contents of `src/` to your Inkscape `extensions/` folder.

Typical locations include:

* OS X - `/Applications/Inkscape.app/Contents/Resources/extensions`
* Linux - `/usr/share/inkscape/extensions`
* Windows - `C:\Program Files\Inkscape\share\extensions`

Usage
=====

Build a spherebot of some manner like http://www.thingiverse.com/thing:20398
Base it on a microcontroller that you can load marlin on like the currently low cost arduina mega+ramps+pololu's (currently these really are cheaper than smaller controllers)
Install marlin and set your steps to 3200 per mm this sets a 1:1 pixel to step ratio (before the math of spheres)

* Size and locate your image appropriately:
	* build platform size is 3200pixels x 800pixels.
	* The extension will automatically attempt to center everything.
* Convert all text to paths:
	* Select all text objects.
	* Choose **Path | Object to Path**.
* Save as G-Code:
	* **File | Save a Copy**.
	* Select **MakerBot Unicorn G-Code (\*.gcode)**.
	* Save your file.
	* **Problem needs fixing** gcode contains the bad lines of "(polyline..." find and replace all lines "(poly" with ";(poly" to comment them I am unsure where in the code to fix this.
	
* Preview
	* For OS X, [Pleasant3D](http://www.pleasantsoftware.com/developer/pleasant3d/index.shtml) is great for this.
	* For other operating systems... I don't know!
* Print!
	* Open your `.gcode` file in [ReplicatorG](http://replicat.org/)
	* Set up your Unicorn and pen.
	* Center your build platform.
	* Click the **Build** button!

