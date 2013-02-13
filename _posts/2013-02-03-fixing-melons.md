---
layout: post
title: "Fixing Melons (Thing a Week #1)"
description: "Fixng melon drops and crafting recipe"
category: content
tags: [thingaweek]
thumbnail: "/assets/img/posts/melons/melon_seeds.jpg"
---
{% include JB/setup %}

<style>
img {
  display: block; margin-left: auto; margin-right: auto;
}
</style>

### [Download MelonOverride.xie](/assets/files/MelonOverride.xie)

## Melons Old and New
For the first "Thing a Week" I want to start small, with a tiny tweak for vanilla melons. Way back in the Minecraft Beta, long before melons found their way into vanilla Minecraft, I had added watermelons to the game in my farming mod. I of course removed them when vanilla melons were added.

<!--more-->

![The Original Xie's Farming Mod](/assets/img/posts/melons/growables.png)

One thing has always bugged me about vanilla melon behaviour however, and that is that they defy the laws of physics. I am referring of course to The Second Law of Thermodynamics (my favourite), which deals with concepts such as entropy and "The Arrow of Time". 

This law is demonstrated in Humpty Dumpty when all the King's horses and all the King's men couldn't put Humpty together again. Intuitively, the same principle should hold true for melons, yet in vanilla Minecraft it's backwards. You harvest melon pieces and then you just... smush them together and they magically become a whole melon again.

Sure, Minecraft isn't all about realism, but sometimes the little things count more than the big things. But instead of complaining about it some more, I'm going to *MOD IT*!

## Fixing Melons
So I created a blank text file called "MelonOverride.xie" and I added to this file a block declaration with an override property. The override property just replaces the original block by using its block ID, it doesn't copy any of its textures or other properties, so we need to add those as well:

[![Melon Block Declaration](/assets/img/posts/melons/melon_block.png)](http://instacode.linology.info/56759)

Note that I used "tile.melon" instead of just "melon". That's because the food item is also called "melon", and it's best not to confuse things.

That's the block done, now we need to deal with the recipes:

[![Melon Block Declaration](/assets/img/posts/melons/melon_recipes.png)](http://instacode.linology.info/56765)

Fairly straightforward, we're removing the old recipe to craft a melon, and adding a recipe that crafts four melon pieces.

Cranking up Minecraft, I'm delighted to see that this works (HAHAHA, yeah right! The first try I had a bunch of mistakes that I had to correct, I got it right on about the third try, but let's keep that between us!)

![Watermelon Farm](/assets/img/posts/melons/melons_growing.jpg)

Since that didn't take very long, I felt like going just a tiny bit farther. What's the most fun thing about eating watermelon? That's right! Spitting out the seeds! While we're at it, let's add an override for the melon pieces as well...

[![Melon Block Declaration](/assets/img/posts/melons/melon_item.png)](http://instacode.linology.info/56768)

Now whenever you eat a piece of melon, some melon seeds pop out! (I guess in vanilla Minecraft you just swallow them... but then you risk melon vines growing out of your ears!)

![Spit out the seeds](/assets/img/posts/melons/melon_seeds.jpg)

So that's that. Here's the complete code for MelonOverride.xie:

    {
      "blocks": {
        "melon": {
          "override": "tile.melon",
          "name": "Melon",
          "tex": {
            "sides": 136,
            "ends": 137
          },
          "hardness": "1.0",
          "stepsound": "wood",
          "material": "pumpkin",
          "drops": "tile.melon"
        }
      },
      "items": {
        "melon": {
          "override": "item.melon",
          "name": "Melon",
          "type": "food",
          "drops": "seeds_melon",
          "hunger": 2,
          "nourishment": 0.3,
          "icon": 109
        }
      },
      "recipes": {
        "cull": "tile.melon",
        "item.melon:4": "tile.melon"
      }
    }
	
##Download

If you want this in your game, download and install my mod (if you haven't already) and then copy [MelonOverride.xie](/assets/files/MelonOverride.xie) into your *minecraft/mods/Xie/content/* directory.