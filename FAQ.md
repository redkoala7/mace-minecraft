## Contents ##

  * [Overview](http://code.google.com/p/mace-minecraft/wiki/FAQ#Overview)
  * [Installation and Running](http://code.google.com/p/mace-minecraft/wiki/FAQ#Installation_and_Running)
  * [Problems](http://code.google.com/p/mace-minecraft/wiki/FAQ#Problems)
  * [Suggestions](http://code.google.com/p/mace-minecraft/wiki/FAQ#Suggestions)
  * [Buildings](http://code.google.com/p/mace-minecraft/wiki/FAQ#Buildings)
  * [Distribution and Modifying](http://code.google.com/p/mace-minecraft/wiki/FAQ#Distribution_and_Modifying)

## Overview ##

**What is Mace?**
> Mace is a tool for MineCraft, which creates a regular world with randomly generated cities. You can use the cities for exploration, expansion, destruction, creation, inspiration, modification...

**When will Mace be finished?**
> My aim with Mace is to randomly generate a complete city, so from that perspective it is done. However, there are many more features that I would like to add. Eventually I'll declare it as finished, then move on to something else.

**When will the next version of Mace be released?**
> I don't know. The amount of free time I have available is unpredictable, so it is hard for me to estimate when the next version will be done.

**Are there any other city generators available for MineCraft?**
> Yes indeed! Such as [Formivore's city, wall & road generators](http://www.minecraftforum.net/topic/171188-v173formivores-mods-city-wall-road-generator/) and [Kinniken's Millénaire](http://www.minecraftforum.net/topic/227822-173-millenaire-npc-village-114-indian-parchments-slovenian-translation/).

> Seen any other city generators? Let me know and I'll add them here.

**Which programming language is Mace written in?**
> Mace is written in [C#](http://en.wikipedia.org/wiki/C_Sharp_(programming_language)). Some of the data files are written in [XML](http://en.wikipedia.org/wiki/XML).

**When tools do you use to make Mace?**
> The code is written in [Microsoft Visual Studio](http://en.wikipedia.org/wiki/Microsoft_Visual_Studio) 2010 Ultimate. I use the [Substrate library](http://code.google.com/p/substrate-minecraft/), which handles all the complicated world editing and creation. I use two mods to make the city buildings, which are [Single Player Commands](http://www.minecraftforum.net/topic/94310-172-single-player-commands-v210-1-new-update/) and [TooManyItems](http://www.minecraftforum.net/topic/140684-172-toomanyitems-in-game-invedit-july-1/). I use [Cartograph G](http://www.minecraftforum.net/topic/153066-cartograph-g-map-your-beta-17/) to render the world as an image, which is very useful for debugging. I use [Google Code](http://code.google.com/) for project hosting.

## Installation and Running ##

**How do I install Mace?**
> There is no installer for Mace. Just extract all the files anywhere and then run Mace.exe. If you have any problems, you are very welcome to post in the [Mace topic](http://www.minecraftforum.net/topic/357201-mace-v140-random-city-generator/).

**How do I remove Mace from my computer?**
> Delete the Mace folder. Mace doesn't edit any other areas of your computer, except for the MineCraft saves folder.

**Will Mace still work when a new version of MineCraft is released?**
> Yes. Mace is a tool, rather than a mod, so consequently it doesn't need updating with every version of MineCraft.

> Mace might break if the world format changes. However, this is an extremely rare thing and Notch would most likely provide an automatic converter, so that shouldn't be a problem.

**Does Mace work on Windows 7? Does it work with 64-bit Windows?**
> Mace is written entirely on Windows 7 (64-bit), so it definitely does!

**I am on Linux/OSX, so can't run Mace. What can I do?**
> You could download Mono 2.6 Beta 3 (or later) and open the code in that. Then run the project and Mace will appear. I haven't tested this, so can't guarantee that it will work :(

> Alternatively, you could check the [downloads page](http://code.google.com/p/mace-minecraft/downloads/list) to see if worlds are available for the latest version. If not, you are welcome to post in the [Mace topic](http://www.minecraftforum.net/topic/357201-mace-v140-random-city-generator/) and I will create some worlds for you.

**Do I need to close MineCraft whilst using Mace?**
> Mace doesn't interact with MineCraft, so it's okay if MineCraft is open or closed.

**Can Mace generate a city in an existing world?**
> This is currently not possible and I don't have any immediate plans to do this. However, it is possible to move a generated city into an existing world using a tool like [McEdit](http://www.minecraftforum.net/topic/13807-mcedit-minecraft-world-editor-compatible-with-mc-beta-166/).

**Can I use a Mace world on my MineCraft server?**
> Yes, this is possible. Smash\_Cuber has created a video guide, called [How to use Mace in SMP](http://www.youtube.com/watch?v=NZGxl-6RtkU).

**Can Mace overwrite any of my existing worlds?**
> No, so don't worry! Mace will keep generating random city names until it finds an unused one.

**Does Mace change the way MineCraft generates terrain? Will my other worlds have cities in them?**
> No, Mace doesn't change the behaviour of MineCraft in any way.

**I feel imbalanced with all this construction. Is there any way to bring some destruction to the city?**
> Yes! Have a look at Commander Keen's tool, called [Teeth of Time](http://www.minecraftforum.net/topic/269176-teeth-of-time-ruin-your-world-v03-brawler/).

**Can I use Mace with Tales of Kingdoms?**
> Yes! Please look at [Ghostdancer's guide](http://www.minecraftforum.net/topic/357201-mace-v19-random-cities-generator/page__view__findpost__p__11977877).

## Problems ##

**Are there any known issues with Mace?**
> Yes, please check out the KnownIssues page.

**I spotted a bug. Would you like to know?**
> Yes, please let me know in the [Mace topic](http://www.minecraftforum.net/topic/357201-mace-v140-random-city-generator/). It would help me a great deal if you can provide details about the bug, such as the version of Mace you are using, a screenshot, the generated world, any installed mods, and your MineCraft version. If you can find steps to reproduce the bug, that would help me as well.

**The terrain difference between the city and the natural terrain is very weird! Why is that?**
> Mace creates the city part of the world, then MineCraft creates the natural terrain around it. The terrain does not match up because it is created by two separate applications. Fixing this is outside the scope of Mace, but I might write a separate tool to fix this in the future.

## Suggestions ##

**I have a suggestion, would you like it?**
> Definitely! It might be something I've already got planned, so have a quick look through the [ToDo](ToDo.md) list to see if it's listed.

**Can I include NPCs in Mace?**
> Yes! Ghostdancer has created the [Mobs for Mace](http://www.minecraftforum.net/topic/532831-173-mobs-for-mace-npc-mod/) mod, which allows you to add NPCs to the city.

**Is it possible to change the biome that the city is in?**
> Unfortunately the biome data is decided by MineCraft at run time, so it is not possible for Mace to change it.

**Is it possible to specify the type of terrain around the cities?**
> In the future this might be possible, but I'm currently not focussing on terrain generation.

**When a new feature is added to MineCraft, will you add it to Mace?**
> If I can find a good use for it, then I definitely will!

## Buildings ##

**Can I submit a building to you?**
> Yes. Thank you! Buildings are very welcome. Ideally they should be submitted as a schematic file that can be loaded into McEdit. It's best if the overall area of your schematic is roughly square. For example, you might have a rectangular building next to a rectangular garden, making it a square overall.

> Unfortunately I can't use all buildings that are submitted. They might not fit into a city theme or they might not be appropriate for Mace. Please don't be disappointed if I can't include your building.

> To comply with forum regulations and to avoid any awkward situations, all contributed schematics must have a license. Any open source license is okay. You can also generate a [creative commons license](http://creativecommons.org/choose/). To be compatible with Mace the license must allow for modifications.

**Can I change how often a building appears?**
> Yes. Go to the Resources folder, then the Themes folder. Open the appropriate theme file in Notepad. Scroll down and look at the building names. Once you find the building, change the frequency value to "very common", "common", "average", "rare", "very rare", "unique" or "exclude". Excluded buildings will not appear on the map. Unique buildings appear a maximum of once per city.

**Building X didn't appear in my city. Why is that?**
> The unique buildings appear a maximum of once per city. There's a lot of unique buildings, so each city will contain a subset of them. Larger cities will contain more unique buildings.

**Can I modify the buildings that Mace puts in the city?**
> Yes. Please see [Ghostdancer's instructions](http://www.minecraftforum.net/topic/357201-mace-v150-random-city-generator/page__view__findpost__p__6854916) for all the details.

**Can I add new buildings for Mace to generate in the city?**
> Yes. Please see [Ghostdancer's instructions](http://www.minecraftforum.net/topic/357201-mace-v150-random-city-generator/page__view__findpost__p__6854916) for all the details.

> Alternatively, SmashCuber has created a [video guide for adding buildings](http://www.youtube.com/watch?v=HQSFDYwsT3I&feature=channel_video_title).

**All Mace buildings are square, any plans to change that?**
> Currently I don't have any plans to change this. Squares are a lot easier to deal with and rectangular/circular buildings can be created within squares, so it's all good!

**Do Mace buildings have a theme?**
> My inspiration for buildings is anything you would find in a typical medieval or Dungeons & Dragons city. I also include buildings that make sense for MineCraft, such as a crafting hut.

**Are you going to add more buildings to Mace?**
> Yes, there's several more buildings that I'd like to add.

**Could you add skyscrapers to Mace?**
> I don't have any plans to do this, because they wouldn't fit with the current buildings. I want the buildings to be small and detailed, rather than large and empty.

**Would you like my suggestion for a building?**
> Suggestions for buildings are always welcome. It might already be planned, in which case it'll be on to the [ToDo](ToDo.md) list or the [UnreleasedChanges](UnreleasedChanges.md).

**Can I modify the signs that Mace puts on buildings?**
> Yes. In the Resources folder there are lots of text files, which contain the data for signs. You can remove/add/edit the files as you like. Take note of any comments at the top of the file. Please do not use pipe characters "|" in these files. "~" characters are used to force a new line on the sign text. See the gravestone.txt file for examples of that.

**Can I make my own city emblems?**
> Yes! Please see [Ghostdancer's guide](http://www.minecraftforum.net/topic/357201-mace-v150-random-city-generator/page__view__findpost__p__6347117).

> SmashCuber has also made a [video guide to creating emblems](http://www.youtube.com/watch?v=EoT2LIa0tA8&feature=player_embedded).

## Distribution and Modifying ##

**Can I include Mace in my mod/tool compilation or website?**
> Yes. You are very welcome to do this. Mace is released under the GNU GPL license, which has terms [roughly similar to this](http://creativecommons.org/licenses/by-sa/3.0/).

**Can I use a Mace city for my adventure map or let's play series?**
> Yes. I'd love to see Mace being used for anything like this, so it would be great if you let me know about it.

**Can I change the code in Mace?**
> Yes. The entire Mace code and all resources can be found on the downloads page. Mace is written in C# and edited in Visual Studio 2010. "Other IDEs are available!"

**Can I distribute my changes to Mace?**
> Yes. Mace is released under the GNU GPL license, which has terms [roughly similar to this](http://creativecommons.org/licenses/by-sa/3.0/). I'm always interested to see what people do with Mace, so it would be nice if you'd let me know.