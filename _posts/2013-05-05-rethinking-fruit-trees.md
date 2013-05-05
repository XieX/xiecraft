---
layout: post
title: "Rethinking fruit trees"
description: ""
category: 
tags: []
thumbnail: "/assets/img/posts/fruittrees/appleTree.jpg"
---
{% include JB/setup %}

<style>
img {
  display: block; margin-left: auto; margin-right: auto;
}
</style>

Yes, still working on Xie's Mod v2 (I really need to come up with a better name for my mod :P), but while I'm at it I've been wondering what to do about fruit trees. I'm not completely happy with having to demolish your orchards in order to get fruit from them if you're starving. I've been wanting to do this for awhile, and over time I've gotten some great ideas from mod users.

<!--more-->

![Fruit trees back in beta](/assets/img/posts/fruittrees/fruittrees.jpg)

The method most like vanilla Minecraft would be to, in a similar fashion to jungle trees with their cocoa pods, have fruit trees spawn fruit blocks. Smashing these fruit blocks would drop fruit, and they would respawn after a time. Obviously one of my modding goals is to adhere to design precedent, and that in itself is a strong argument for this approach, however I must admit I'm not that keen to go this path. I'm just not sure I can get it to look that great. Cocoa pods work fine, since you break them to drop cocoa beans, but making a cube-shaped apple appear on the side of a tree that mysteriously turns into a round apple item just wouldn't feel right.

![Apple pods](/assets/img/posts/fruittrees/applepods.jpg)

That could be fixed with an "item frame" approach, which is very similar to the above, but instead of making the fruit appear as "blocks", you can stick them to the sides of the leaf blocks as they would appear were they inside an item frame (minus the frame itself, of course). That way the transition from "hanging" fruit to inventory fruit is more natural.

![Frame? What frame!](/assets/img/posts/fruittrees/appleswithoutframes.jpg)

Alternatively, there's the "bush like" approach, which is to make leaf blocks act similarly to tomato and cotton bushes from my mod. That is, when a fruit-bearing leaf block is broken, it drops the fruit, and turns into an "empty" leaf block. The leaf block then grows over time, visibly changing back into a fruit-bearing leaf block again. This method is most similar to the mod's current behaviour, but takes the guesswork out of smashing leaves to find fruit, as it's visually obvious which leaves will drop.

![Shedding](/assets/img/posts/fruittrees/shedding.jpg)

As for "shedding", or naturally spawning fruit under trees, I'm not sure what to do with it. It's a great feature, though it can be a bit of a resource drain on lower-end computers, or if you have massive orchards. The obvious evolution for shedding would be to have fruit blocks (or bush-like leaf blocks) eventually pop themselves, and drop the fruit to the ground. However the original purpose of the feature was to make fruit trees sustainable, so it will no longer be needed if they are sustainable in themeslves. Having said that I'll most likely leave it in but disable it by default - one of my modding mantras is "let the user decide for themselves", since from a group of 10 Minecraft players, you'll get at least 10 different playing styles :P

Anyway, I should get back to work! XD