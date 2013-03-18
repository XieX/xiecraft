---
layout: post
title: "Updating to Minecraft 1.5..."
description: ""
category: 
tags: []
thumbnail: "/assets/img/xiewtfface.jpeg"
---
{% include JB/setup %}

<style>
img {
  display: block; margin-left: auto; margin-right: auto;
}
</style>

### Updating to Minecraft 1.5...

... is a work in progress, and probably gonna take another week.

While I admit that the biggest reason this update is taking so long is because I play a lot of video games (*cough* StarCraft II), this update is quite a bit more complex than previous ones, because of the changes that have been made to how Minecraft handles textures.

<!--more-->

They're good changes. Great changes. Changes for the better. But my mod has to go through quite a few changes of its own in order to take full advantage of them. The big difference is that instead of textures being referred to by an integer index on a spritesheet, they are referenced directly by filename.

For most mods the update is actually pretty easy, it's just a matter of slicing up your spritesheets and returning the filename for your texture instead of the index/spritesheet name combination.

Unfortunately my mod is a bit more complicated than that. I parse a JSON object to determine which spritesheets and texture indices to use for any given block or item, instancing objects dynamically at runtime to relay that information to the engine in-game. Still, in theory all I would need to do is update the JSON specification to take filenames instead of indices, right?

Yes, absolutely right, that's what I should do, and I would have been done by now... :P HOWEVER, while I was updating I saw an opportunity to take full advantage of the new texture handling system, and to begone with tedious texture allocation via JSON (anyone who has authored or attempted to author content using my mod knows what I'm talking about).

For example, this is the <b>old way</b> of specifying corn crop textures:

<a href="http://instacod.es/65902"><img src="http://instacod.es/file/65902" /></a>

But instead of doing that, why not just leave that whole mess out and have the parser automatically detect the files "cornCrop_0-3.png", "cornCrop_4-6.png" etc in your textures folder and do it all for you? So that's what I've been working on.

One of the biggest reasons for this change is to make updating pre-1.5 content easier - all you'll need to do is slice up the sprite sheets and name the files correctly. The .xie files won't need to be edited at all.

If a job's worth doing, it's worth overthinking it and building something far more complicated than you need!