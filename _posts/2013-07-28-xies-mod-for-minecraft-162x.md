---
layout: post
title: "Xie's Mod for Minecraft 1.6.2"
description: ""
category: Releases
tags: []
thumbnail: "/assets/img/posts/releases/new_default_content.jpg"
---
{% include JB/setup %}

I managed to hack out an updated version of my mod for Minecraft 1.6.2!

### [Download](/assets/files/downloads/releases/2013_Jul_28/Xie%27s%20Mod%20for%20Minecraft%201.6.2.zip)

It took me a little longer than expected, though it was a relatively easy update - super easy compared to 1.5! But I had some deployment issues, and it took me a little while to figure out what to do with textures, but I got it sorted out. We still have to unzip the download into the ./mods/ directory, it'd be nice to just copy in a zip or jar file, but there's a bit more work I'll have to do to get there. 

Includes default farming content.

<!--more-->

## Installation

Assuming you already have Minecraft Forge installed, just unzip the above download into your .minecraft/mods/ directory, so that the contained "Xie" folder is inside the /mods/ directory.

## Known Bugs

Here is a list of known bugs, if you find a bug that isn't on this list feel free to let me know.

* wheat override still suffers from infinite recursion
* metavariant plant spawning is still buggy (i.e. only shrubs and apple trees spawn naturally)

## Fixed Bugs From Previous Release
* _some glitches with the top level of corn crops not popping when harvested_ 
* _fertilizing custom crops is still the old fashioned way (grows it to max)_