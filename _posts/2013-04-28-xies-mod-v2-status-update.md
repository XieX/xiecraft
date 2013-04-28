---
layout: post
title: "Xie's Mod v2 Status Update"
description: ""
category: 
tags: []
---
{% include JB/setup %}

<style>
img {
  display: block; margin-left: auto; margin-right: auto;
}
</style>

Refactoring is a slippery slope. You start by overhauling one entire section of code, and before you know it you're rebuilding almost everything... What started out as a simple update has turned into a code masacre, as I discover more and more rubbish code that I wrote years ago and loathe beyond reason.

So it is with mixed feelings that I announce Xie's Mod v2.0! Coming soon... er or later :P

<!--more-->

I know I've been promising an update for awhile, but this is a worthwhile project, and one that I've been meaning to do for a long while. It will make the mod more robust, maintainable and scalable, saving a lot of time in the future.

Having said that it's not all good news. While I'm at it I'm revising the format of .xie files, partly due to the changes made in Minecraft 1.5 (i.e. textures). This will render all currently authored mod content unusable in Minecraft 1.5+ versions of Xie's Mod. I cannot apologise enough for this, but I will be happy to help anyone who has written their own .xie files update to the new format. Furthermore if there's a lot of updating to do (I know I have a lot of content myself!) I may even take the time to write a converter - shouldn't be too difficult.

Also to help give you a sense of where I'm at with the project, I created this MSU diagram of my mod's inner workings, with indicators for how much progress I've made in each area. And not that it's any indicator, but the remake is about 20% of the line count of the original mod (which was ~15K) so far, but there was a lot of WET code amongst that lot, and a lot of it will be copy-pasted over as I go.

![Xie's Mod Graph](/assets/img/graphs/XiesMod_01.jpg)