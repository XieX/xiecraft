---
layout: post
title: "Some bug fixes"
description: ""
category: Releases
tags: []
---
{% include JB/setup %}

### [Download Xie's Mod](/assets/files/downloads/releases/2013_Feb_24/Xie.zip)
For Minecraft 1.4.7

## Changes

* Some recipe fixes 
* Added support for explosion resistance
* More refactoring

<!--more-->

## Explosion resistance

To change a custom block's explosive resistance, just add a "resistance" property to your block declaration, e.g.:

	  {
		"blocks": {
		  "myToughBlock": {
			"name": "Tough Block",
			...
			"resistance": 10
		  }
		}
	  }
  
This is one-third the scale of the explosive resistance listed on the Minecraft wiki, e.g. block resistance 10 is the same as that of stone brick (30).

## Known bugs

I'm still aware of some bugs with block spawning at world generation, I haven't had a chance to track those down yet though.