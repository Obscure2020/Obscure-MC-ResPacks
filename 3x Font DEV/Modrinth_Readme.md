# The font for the 1080p everyman. Finally.

Let's face it. Most gamers (me included) have 1080p monitors. Whether it's a standalone screen or it's built into your laptop, 1080p is still the most common monitor resolution today, and this creates an interesting issue in Minecraft.

Anyone who's looked at Minecraft's `Video Settings` menu for more than 5 seconds has come across the **GUI Scale** option. And as my friends and I can attest, any savvy user who has a 1080p monitor will agree: **at 1080p, a GUI Scale of 3 looks the best.**

GUI Scale 2 ends up looking too small. GUI Scale 4 ends up too big, and screen real estate begins to dwindle. But herein lies the issue: if GUI Scale 3 reigns supreme, ***why doesn't anyone ever make any 48x resource packs?***

<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/Splash001_v2.png" style="image-rendering:pixelated;" alt="This is my time to shine.">

## Powers of Two _vs._ Multiples of 16
To make a long story short, the community of people who create Minecraft resource packs got addicted to the Powers of Two. It is therefore easy to find resource packs that are 8x, 16x, 32x, 64x, 128x, or even larger. But Minecraft's GUI Scale setting doesn't operate on Powers of Two. **It operates on Multiples of 16.**

Minecraft's default, inbuilt textures are 16x16 pixels, commmonly abbreviated to 16x. When you adjust the GUI Scale setting, you're actually selecting an integer multiple of 16x for the display scale of all GUI menus, buttons, and text.

**1 times 16 = 16x.** The default, the familiar.\
**2 times 16 = 32x.** Double the resolution of the default! [Faithful](https://modrinth.com/resourcepack/faithful-32x) is a great longstanding example.\
**4 times 16 = 64x.** Quadruple the resolution of the default!! [VanillaXBR](https://modrinth.com/resourcepack/vanillaxbr) is an example I've actually used myself, and may use again in the future.

But wait, we've skipped something. We're not Valve, we know how to count, right?

**3 times 16 = 48x.** Even though this totally works in-game, 48x gets literally no community recognition.

It's true, pretty much no one makes any 48x packs. Heck, Modrinth doesn't even have a *category* for 48x, making it difficult to advertise such a pack. (PlanetMinecraft doesn't have a tag for 48x either.) 32x and 64x are available in their menu, but 48x? Nope.

## Why would anyone want a 48x pack?

Well, how does Minecraft handle a mismatch between the scale of your resource pack and your GUI Scale setting? Pretty much the easiest way they could: ***nearest-neighbor image scaling.***

Now, Minecraft's default 16x textures can be easily upscaled to 32x, 48x, or 64x as dictated by the GUI Scale. They're all multiples of 16, after all. But what if you have a 32x or 64x pack installed? What happens then? Let's take a look.

## Why a 32x pack doesn't work
Here's Faithful at its native GUI Scale of 2:\
<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/Faithful_Good_Small.png" style="image-rendering:pixelated;" width="100%" alt="Smooth-looking 32x text.">

Here's Faithful again, at GUI Scale 3:\
<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/Faithful_Bad_Small.png" style="image-rendering:pixelated;" width="100%" alt="Jagged-looking 48x text.">

As you can see, 32x textures cannot be cleanly upscaled to 48x. Artifacts appear due to the non-integer transformation.

## Why a 64x pack doesn't work
Here's VanillaXBR at its native GUI Scale of 4:\
<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/VanillaXBR_Good_Small.png" style="image-rendering:pixelated;" width="100%" alt="Smooth-looking 64x text.">

Here's VanillaXBR again, at GUI Scale 3:\
<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/VanillaXBR_Bad_Small.png" style="image-rendering:pixelated;" width="100%" alt="EXTREMELY jagged-looking 48x text.">

The transformation from 64x to 48x is even worse. Pixels have to be _thrown out_ to perform nearest-neighbor downscaling, resulting in _horrendous_ artifacts. These characters look like they were chewed up by a dog.

# Finally, a 48x font

If I were to attempt to create an entire 48x pack, redoing every texture in the game, I'd likely end up working on the project forever. And that's _if_ I don't go nuts in the process.

<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/Splash002_v2.png" style="image-rendering:pixelated;" alt="But the font?">\
<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/Splash003_v2.png" style="image-rendering:pixelated;" alt="Oh yeah. That can be done.">

I have taken it upon myself to improve the lives of all my brethren of the church of GUI Scale 3 by creating a new and improved font ***actually designed to look good at GUI Scale 3.***

This font is not a Vanilla imitation or interpretation, but rather a revamp according to my own tastes. And *boy* does it look good in-game.

<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/3x_Good_Small_v2.png" style="image-rendering:pixelated;" width="100%" alt="Crisp and clean-looking 48x text.">\
<img src="https://raw.githubusercontent.com/Obscure2020/Obscure-MC-ResPacks/main/3x%20Font%20DEV/Splash004_v2.png" alt="Welcome to the Kingdom of NOT garbage. All hail King Obscure.">

## Progress

As of Version 1.1, only basic ASCII has been improved. Future versions will include support for accented characters and nonlatin European characters. I also plan to implement the "replace SGA with english characters" modification just for fun.