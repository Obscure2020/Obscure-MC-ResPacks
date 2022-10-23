# The font for the 1080p everyman. Finally.

Let's face it. Most gamers (me included) have 1080p monitors. Whether it's a standalone screen or it's built into your laptop, 1080p is still the most common monitor resolution today, and this creates an interesting issue in Minecraft.

Anyone who's looked at Minecraft's `Video Settings` menu for more than 5 seconds has come across the **GUI Scale** option. And as my friends and I can attest, any savvy user who has a 1080p monitor will agree: **at 1080p, a GUI Scale of 3 looks the best.**

GUI Scale 2 ends up looking too small. GUI Scale 4 ends up too big, and screen real estate begins to dwindle. But herein lies the issue: if GUI Scale 3 reigns supreme, ***why doesn't anyone ever make any 48x resource packs?***

```
This is my time to shine.
```

## Powers of Two _vs._ Multiples of 16
To make a long story short, the comminity of people who create Minecraft resource packs got addicted to the Powers of Two. It is therefore easy to find resource packs that are 8x, 16x, 32x, 64xx, 128x, or even larger. But Minecraft's GUI Scale setting doesn't operate on Powers of Two. **It operates on Multiples of 16.**

Minecraft's default, inbuilt textures are 16x16 pixels, commmonly abbreviated to 16x. When you adjust the GUI Scale setting, you're actually selecting an integer multiple of 16x for the display scale of all GUI menus, buttons, and text.

**1 times 16 = 16x.** The default, the familiar.\
**2 times 16 = 32x.** Double the resolution of the default! [Faithful](https://modrinth.com/resourcepack/faithful-32x) is a great longstanding example.\
**4 times 16 = 64x.** Quadruple the resolution of the default!! [VanillaXBR](https://modrinth.com/resourcepack/vanillaxbr) is an example I've actually used myself, and may use again in the future.

But wait, we've skipped something. We're not Valve, we know how to count, right?

**3 times 16 = 48x.** Literally no support.

It's true, pretty much no one makes any 48x packs. Heck, Modrinth doesn't even have a *category* for 48x, making difficult to advertise such a pack. (PlanetMinecraft doesn't have a tag for 48x either.) 32x and 64x are available in their menu, but 48x? Nope.

## Why would anyone want a 48x pack?

Well, how does Minecraft handle a mismatch between the scale of your resource pack and your GUI Scale setting? Pretty much the easiest way they could: ***nearest-neighbor upscaling.***

Now, Minecraft's default 16x textures can be easily upscaled to 32x, 48x, or 64x. They're all multiples of 16, after all. But what if you have a 32x or 64x pack installed? What happens then? Let's take a look.

## Why a 32x pack doesn't work
Here's Faithful at its native GUI Scale of 2:\
<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/Faithful_Good.png" style="image-rendering:pixelated;">

Here's Faithful again, at GUI Scale 3:\
<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/Faithful_Bad.png" style="image-rendering:pixelated;">

As you can see (zoom in for a clearer look), 32x textures cannot be cleanly upscaled to 48x. Artifacts appear due to the non-integer transformation.

## Why a 64x pack doesn't work
Here's VanillaXBR at its native GUI Scale of 4:\
<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/VanillaXBR_Good.png" style="image-rendering:pixelated;">

Here's VanillaXBR again, at GUI Scale 3:\
<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/VanillaXBR_Bad.png" style="image-rendering:pixelated;">

The transformation from 64x to 48x is indeed worse. Pixels have to be _thrown out_ to perform this non-integer downscale, resulting in _horrendous_ artifacts. (I mean just _look_ at those angle brackets and the lowercase `x`. They are ***suffering.***)

# Finally, a 48x font

If I were to attempt to create an entire 48x pack, redoing every texture in the game, I'd likely end up working on the project forever. And that's _if_ I don't go nuts in the process.

```
But the font?
```
```
Oh yeah. That can be done.
```

I have taken it upon myself to improve the lives of all my brethren of the church of GUI Scale 3 by creating a new and improved font ***actually designed to look good at GUI Scale 3.***

This font is not a Vanilla imitation or interpretation, but rather a revamp according to my own tastes. And *boy* does it look good in-game.

```
Welcome to the kingdom of NOT garbage.
```

## Progress

As of Version 1, only basic ASCII has been redone. Future versions will include support for accented characters and nonlatin European characters. I also plan to implement the "replace SGA with english characters" modification just for fun.