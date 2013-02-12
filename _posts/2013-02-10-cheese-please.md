---
layout: post
title: "Cheese Please! (Thing a Week #2)"
description: "Super simple cheese mod"
category: content
tags: [thingaweek]
thumbnail: "/assets/img/posts/cheese/houseofcheese.jpg"
---
{% include JB/setup %}

<style>
img {
  display: block; margin-left: auto; margin-right: auto;
}
</style>

[Download cheese.zip](/assets/files/downloads/cheese.zip)

## Cheese!!
Way back when I made Xie's Cooking Mod I added cheese to Minecraft. The mod added a "stove" block that let you "cook" food by adding items sequentially to the stove. Cheese was made by cooking milk on the stove and adding a yellow flower... While I have been meaning to update the old stove mod, here's a different method of making cheese in the meantime!

<!--more-->

![Smelting cheese](/assets/img/posts/cheese/smeltingcheese.jpg)

Smelt a bucket of milk, and it'll turn into a bucket of cheese (makes perfect sense!). You can then get a cheese block out of the bucket via the crafting grid, or by right-clicking the bucket on the world. The cheese block can be crafted into 9 cheese pieces, that can be eaten for 3 food-points.

![Crafting cheese](/assets/img/posts/cheese/craftingcheese.jpg)

If you're running my default farming and food content, cheese can also be added to sammiches, tacos, burritos and salads, in place of a "protein" component (such as chicken, beef, fish).

For anyone who's interested, here's the JSON for it:

	{
		"blocks": {
			"cheeseBlock": {
				"id": 4012,
				"name": "Cheese",
				"tex": {
					"texFile": "cheese.png",
					"all": 0
				},
				"drops": "cheeseBlock"
			}
		},
		"items": {
			"cheeseSlice": {
				"id": 10094,
				"name": "Cheese",
				"type": "food",
				"hunger": 6,
				"nourishment": 0.3,
				"texFile": "cheese.png",
				"icon": 1
			},
			"bucketOfCheese": {
				"id": 10095,
				"name": "Bucket of Cheese",
				"type": "seed",
				"growsInto": "cheeseBlock",
				"texFile": "cheese.png",
				"icon": 2,
				"container": "bucket",
				"stacksize": 1
			}
		},
		"recipes": {
			"cheeseSlice:9": "cheeseBlock",
			"bucketOfCheese": {
				"smelt": "milkBucket"
			},
			"cheeseBlock": "bucketOfCheese",
			"furnace": "dirt",
			"milkBucket": "dirt,dirt"
		},
		"aliases": {
			"protein": "cheeseSlice"
		}
	}

Cheese isn't just fun to eat, it's fun to build with!

![Building with cheese](/assets/img/posts/cheese/houseofcheese.jpg)

##Download

If you want this in your game, download and install my mod (if you haven't already) and then copy/extract [cheese.zip](/assets/files/downloads/cheese.zip) into your *minecraft/mods/Xie/content/* directory.