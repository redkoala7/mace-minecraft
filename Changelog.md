# 1.11.1 #

  * + Collapsed mineshaft sections.
  * > Fixed a bug that caused Mace to die horribly when building frequencies were changed in custom themes. Thanks to drmule for letting me know about this.

# 1.11 #

  * + Added two more city entrances.
  * + Added guards to the top of the walls. If Minecraft Villagers are selected, this will be iron golems. If Ghostdancer's NPCs are selected, this will be knights.
  * + Added cobweb moat. Thanks to coau14 for this suggestion.
  * + Added ankh emblem. Thanks for coau14 for this suggestion.
  * + Added empty plots, which are selectable in custom themes. These are useful if you want to start building straight away.
  * + Added a trap to the mineshaft.
  * + Added villagers to the main streets.

  * > Output worlds are in Anvil format.
  * > The resource world has been converted to Anvil format.
  * > Inverted stairs in the resource world are correctly handled when imported. Inverted half-slabs were already working.
  * > Items in brewing stands and dispensers in the resource world are now copied to the output world. Items in furnaces were already being copied over.
  * > Updated the door data to Anvil format. This means doors will be rotated correctly again.
  * > Desert cities are set to be in the desert biome. This means they will no longer get rain or snow.
  * > Fixed a bug in the city entrance validation code for custom themes. Thank you to empyreanunseen for letting me know about this.
  * > Fixed a bug with various plant types in custom themes. Thank you to coau14 for letting me know about this.
  * > A time warning will appear when generating ten or more cities.
  * > Fixed a bug when using the desert adjectives/nouns in custom themes. Thank you to Mitchell\_R for letting me know about this.
  * > Fixed animals not spawning in the barn. Thank you to coau14 for letting me know about this.
  * > Reduced the value of treasure found in houses.
  * > The type of wood planks and logs are randomised for each building.
  * > Ice walls no longer have torches on the walkways, moats that would melt them and lights on the side of the walls. Thanks to Jaceon for suggesting this.
  * > You can now cancel world generation. Thanks to Jaceon for suggesting this.
  * > Fixed the progress bar going above 100%.
  * > Building frequency distribution can be edited. Open the theme file and look for the frequency items in the options. Example syntax would be "10 8 5 2 1" without the quotes. Where 10 is very common buildings and 1 is very rare buildings . The numbers can add up to anything. Farm buildings are "20 16 12 8 4". Everything else is "9 8 7 6 5".

  * - Removed the SplitContainer control, so hopefully it will work on Linux and OSX again. Please let me know either way.

# 1.10 #

  * Theme generator! Click the "New..." button and then change as many options as you want.
  * The amount of underground ores generated can now be controlled from the main window.
  * Add a fence around the bedrock moat.
  * Put a real mushroom on top of the mushroom farm. Thanks to coau14 for this suggestion.
  * Moved buildings to more logical places in the resource world.
  * Added some more combinations to the desert city names.
  * Added some more combinations to the world names.
  * You can now control which levels of the mineshaft will appear. Edit the end of the mineshaft.xml file to do this.

# 1.9 #

**Farms**
  * Farms are now on one side of the city.
  * Removed the code-generated farms.
  * Added farm buildings: melon farms, pumpkin farms, wheat farms (large & small), cactus farms (large & small), orchards (oak, birch, spruce), sugar cane farms, animal farms, large mushroom farms.
  * Improved the top of the mushroom farms.
  * Farms now have torches.

**Buildings**
  * New buildings: Large ruins (medieval theme), Shop (desert theme), three houses (desert theme), compound (desert theme), gallows (medieval theme, unique), large market (medieval theme, unique), alchemist (medieval theme).
  * Lots of the new blocks are being used: window panes, stone bricks, iron bars, melons, pumpkins, slabs, fence gates...
  * Small improvements to a few existing buildings.
  * Added a different sky feature. Mace will randomly select one sky feature per medieval city.

**NPCs**
  * Added Ghostdancer's NPCs to the new buildings.
  * NPCs will now be placed directly into the world, rather than appearing via spawners.
  * Added a new NPCs option: Minecraft Villagers. This will place the various Minecraft villagers into appropriate places in your cities. This is the default option.
  * There's currently no NPCs placed into Novv's Medieval Buildings, but I'll add them in a future update.

**Options**
  * Added an option to export schematics of each city. These are saved in the world directory. I don't want to make it more complicated than that, because it would make compatibility with Linux/OSX harder.
  * Added buttons to save the logs to a file. These are saved in the world directory. I don't want to make it more complicated than that, because it would make compatibility with Linux/OSX harder.
  * Added an option to the theme files: "torches\_on\_walkways". When switched on, this will make the torches on the walkways and guard towers.  It's switched on for all themes, but can be switched off if you'd like ice walls. If you are making ice walls, remember to turn off all the other options that make fire/torches.

**Other**
  * The ground underneath desert cities will now contain more sand and sandstone.
  * Added random splash text, just like Minecraft!
  * Removed/added lots of the random text that makes up city/road names.
  * Added a new path type: raised edges.
  * Added more path block types.

**Code**
  * Updated to Substrate 1.0.3.
  * Moved the city entrance to the resource world. This will make it easier to modify and to have different city entrances.
  * Changed the Minecraft folder location for Macs, so hopefully the Mace code will run on a Mac now. As usual I have no way of testing this, so fingers crossed.
  * The building type tags (mineshaft\_section, etc) in the theme files have all been combined into the type tag.
  * Added rotation code for: brick stairs, nether brick stairs, stone brick stairs, fence gates, burning furnaces, open trapdoors, redstone repeaters, levers, pistons, detector rails, powered rails, vines, huge mushrooms.
  * Flag patterns are now stored in files in the resource folder.
  * Blocks that make up the underground are now specified in the theme files.
  * Each theme can now have multiple possible sky features. Mace will select a random one for each city.

# 1.8 - The Trinity Transition #

**Major updates:**
  * Multiple cities! Mace now generates multiple cities in the same world. You can specify the amount of cities that you would like.
  * City themes! The theme determines the buildings and the possible emblems, moats, flowers, paths, city names, tower additions, farms and more. Mace currently has three themes:
    * Medieval buildings - Most of the buildings from the previous version
    * Novv's medieval buildings - Used with permission. Thanks Novv!
    * Desert buildings - Just a small number at the moment.
  * New interface! The new interface is focussed on customising the world.

**Miner updates:**
  * Added five new emblems created by Ghostdancer. They are emblems of a creeper, a pickaxe, a sword, a tree and the crafters' guild.
  * Added a sandstone creeper mine entrance by Ghostdancer.
  * Generated worlds will now appear at the top of your Minecraft world list.
  * There's now two cactus moats - one at normal level and the original submerged one.
  * Added the progress percentage to the window title.
  * Lowered the fire and lava moats, to stop them setting fire to emblems.
  * You can decide to spawn inside/outside a random city, or away from the generated cities.
  * Cities without farms will now have flowers on the empty area outside.
  * The doors on farms are now fence gates.
  * The world type can be creative, survival or hardcore.
  * The cactus moat is a bit more random.
  * You can now view the normal log (same as before) or the verbose log (includes lots of details).
  * Redstone ore on the ground (layer 63) of the resource world will be turned into the city ground block.
  * Gold ore on the ground (layer 63) of the resource world will be turned into the path block.

# 1.7.2 #

  * This release fixes the lighting bug with chests. Thanks to jaquadro for providing the fix.

# 1.7.1 #

  * The bank now goes down to it's intended level. Thank you to shad3w44 for letting me know about that.
  * The position of the large sandstone house is now correct. Thank you to Curufea for letting me know about that.

# 1.7 - The Improvement Iteration #

NPCs

  * You can now tell Mace to include NPC spawners in the city, which will use Ghostdancer's Mobs for Mace. Please see the Mobs for Mace thread for download instructions.

Buildings

  * Added a windmill to the farming buildings (unique frequency).
  * Added a bank, which is inspired by coau14's bank (unique frequency).
  * Added a theatre (average frequency).
  * Added an igloo, which was created by coau14 (unique frequency).
  * Added a wool house with a hedge-garden (average frequency).
  * Added a blacksmith, tailor and water well (all rare frequency).
  * Added two sandstone houses (common frequency).
  * Added a wizard's tower (unique frequency).
  * Added a large park (unique frequency).

Mineshaft

  * Written in mineshaft features, which are things like lava pools, resting stations, dungeons...
  * The mineshaft now has a proper entrance that will appear in a random location in the city.
  * Added four mineshaft entrance designs, all created by Ghostdancer. Mace will select one entrance to use in the city.
  * The balloon will appear above the mineshaft entrance, which helps to locate it. Thanks to Ghostdancer for this suggestion.
  * Slightly changed the location of resources: gold + diamonds are in the lowest third, lapis + redstone are in the lowest two thirds and coal + iron are found everywhere.
  * In mineshaft chests the common blocks will now appear in larger amounts.
  * Mineshafts will no longer have gravel ceilings on the highest four levels and they will no longer have sand ceilings on the highest two levels. This stops the ceiling collapsing on you in the higher levels. Thank you to BrianSki for this idea.

Code / Config

  * The code has been successfully tested in Mono 2.6 RC1 on Windows. If you run it in that version on a mac, please let me know what happens - good or bad! Including error messages is very useful to me.
  * Made a lot of minor changes to the code to bring it more inline with C# standards. It's still got a long way to go though.
  * Updated to Substrate 0.7.
  * Sponge in the resource world is turned into a random wool colour for each building. This is useful for randomly coloured carpets.
  * The list of farm buildings, mineshaft sections and mineshaft entrances are taken from buildings.xml, which means anyone can add new buildings of these types. These buildings can use all the frequency values.
  * The rail rotation code saves more frequently, which should hopefully fix any remaining issues. It is applied to the whole city now, so any rails placed in resource buildings will be turned appropriately. It doesn't look at different elevations yet.

Bugs

  * Outside fire lights will no longer set fire to the flags.

Moat

  * Added a fire moat, which will appear 10% of the time. Thanks to coau14 for this suggestion.

Minor Stuff

  * City walls now go down to bedrock. Thanks to Commander Keen for this suggestion.
  * Added an option to export the city as a schematic.
  * Apartment frequency has been switched to "very rare" instead of "average".
  * Flowers and grass will appear in more places in the city.
  * The mini farms are now enclosed to stop animals destroying them.
  * Added some more combinations to the brothel names.
  * Street signs are now on posts. Thanks to shad3w44 for this suggestion.
  * House chests now have a slightly larger variety of items.
  * Improved the house signs.
  * Mace will now randomly choose between the usual glowstone street lights and the new torch street lights. Thanks to BrianSki for this idea.
  * Very small cities had an unrealistically large number of unique buildings, so I've disabled prioritising unique buildings on very small cities.
  * Added some more wall materials.
  * Buildings have little paths, which link to the roads when possible.

# 1.6.1 #

  * Portrait bug is fixed. Thank you to Ghostdancer for letting me know about that.
  * Fixed the rail rotation bug. Thank you to Commander Keen for letting me know about that.
  * Added lots more library sections and tavern combinations. All provided by SoNick - thanks!
  * Changed the way the lighting is called, which seems to have reduced the lighting bugs.
  * Cities without farms now have 8 empty blocks outside, rather than 16. Thank you to Arschkrampi for hassling me into that!
  * Made a couple of minor changes to the buildings.
  * Added a new compact house, submitted by coau14. Thanks!
  * Set the application support directory for Mac OSX, but I'm unable to test this, so it might not work.
  * If an obsidian wall is selected and "Valuable blocks in architecture" is unchecked, the first option will take preference. So consequently the obsidian wall will stay. Thanks to Keypadzzz for letting me know about this conflict.

# 1.6 - The Underground Update #

  * The code is now significantly more compatible with Linux and has been tested successfully in Mono on Ubuntu 11.04. Massive thank you to Surrogard for rewriting my code to make it friendly to Windows and Linux.
  * Added a mineshaft below the city. The entrance is in the middle of the city.
  * Underground terrain is now stone, dirt, gravel and sand (with occasional sandstone).
  * Ores are generated underground.
  * Added a new frequency type: "unique". Each unique building will appear a maximum of once per city. Unique buildings must be at least 10 squares away from another unique building.
  * Added a cathedral, archery range, prison, pyramid and large fountain. These all have the "unique" frequency.
  * Added a castle, which was designed by [TheMegaMiner](http://www.youtube.com/user/TheRealMegaMiner). The castle has the "unique" frequency value.
  * Added a simple house made of stone and bricks.
  * Added a tent building.
  * Added an apartment building. Thanks to redjay17 for this suggestion.
  * A small number of barns will now appear sporadically between the farms.
  * The noticeboard is now a building, that will randomly appear somewhere in most cities. It has the "unique" frequency.
  * Made a whole bunch of small improvements to the existing buildings. Items in the bakery, more noticeboard messages, paintings, basements, changing room in the baths, longer diving board, lava instead of fire in the baths, random drink names in the tavern, random library sections...
  * City wall material is now selectable. It will default to a random type.
  * Guard towers now allow for flags, instead of fire beacons. You can let Mace randomly chose between the two, or pick one yourself.
  * Churches are now "very rare" frequency, rather than "rare".
  * Graveyards are now excluded, because the cathedral has a graveyard.
  * Added help to all of the controls in the application.
  * Added an option to make all chests empty.
  * Added an option to turn valuable blocks in architecture to less valuable blocks.
  * Mob spawners placed in the Mace resource world will now work. Thanks to Ghostdancer for letting me know they were broken.
  * I accidentally extinguished all the fires in a previous version, but they are now back to normal.
  * Added two new emblems: heart and cobweb

# 1.5.1 #

  * This version fixes a bug that prevented people from setting the world name. Thank you to shad3w44 for letting me know about that.

# 1.5 #

  * Added nine new buildings: market, house with a garden roof, shrine, baths, library, mosque, swimming pool and two ruined buildings
  * "Very rare" buildings will not spawn within 50 blocks of the same type of building. "Rare" buildings will not spawn within 25 blocks of the same type of building.
  * Greenhouses are now "rare" frequency, rather than "average". Thanks to Sammmiii for this suggestion.
  * Streets names are now all unique.
  * Mace will now automatically work out the height of imported buildings. The starting Y axis is set to 63 (ground level) by default, which can be overwritten by adding `<source_start_y>7</source_start_y>` (change 7 to be the lowest point of your building) to the relevent section of the buildings.xml file.
  * Building names on signs are now unique. Gravestones are unique within each graveyard.
  * Street signs now have torches on top of them.
  * The mini farms in the city will no longer have naughty pigs ruining them. Thanks to Sammmiii for letting me know about that.
  * House chests around the city now have random assorted items in them. Thanks to Ghostdancer for pointing out how empty they all were
  * Added a FAQ (Frequently Asked Questions) page to the wiki
  * You can now specify the city/world name, as long as it doesn't already exist. Thanks to Ghostdancer for suggesting this.
  * Buildings are rotated to the nearest path
  * City names will no longer be the same word twice (i.e. Carnivalcarnival)
  * Street lights have moved to the side of the roads
  * Random sign types are no longer hard-coded. Thanks to Curufea for suggesting this
  * The project is now compatible with Mono 2.6 Beta 3, so in theory (I can't test this) it should be possible to load the project in that on a Mac or Linux and run it
  * Coffins are now chests, full of bones and other items. Thanks to infraspace for this suggestion
  * Added/modified/removed some of the random sign text
  * Changed the size properties of the Mace window, so hopefully it won't go all massive on some computers.
  * You can now specify a random seed for the MineCraft world and a random seed for the city generation. The seeds are displayed on the noticeboard. Please note, changing any options in Mace will usually affect the random number generator for the city, so if you share your seed with anyone else, remember to tell them which options you used. Also note that seeds are version specific, so using a seed in V1.5 will result in a different city to using it in V1.6.
  * A very small amount of the larger ponds will now be lava, rather than water. Thanks to Lokomo for this suggestion
  * Added a Credits page to the wiki
  * City emblem data is now stored in text files in the resources folder. You can add/remove/edit them as much as you like.
  * Portraits are imported from the source world. Thanks to jaquadro for helping me with the code for this
  * Download size is massively reduced, from 1955kb to 263kb
  * Added glass blocks to the fountain, which will hopefully stop wolves getting stuck in there. Thanks to shad3w44 for letting me know about this bug.

# 1.4 #

  * Rewrote the path layout code, to divide the city into rectangles
  * Random buildings are imported into the city. They are chosen by weighted randomness (so more houses and trees, rather than statues and graveyards)
  * Buildings are stored in the Mace world (in the Resources folder), which can be edited in MineCraft
  * Building data is stored in buildings.xml, which means it is possible to add and remove buildings, or change how frequently they appear
  * Made about twenty buildings
  * Added main roads going through the city, which link the north/south entrance and the east/west entrance. They are slightly wider and have street lights
  * Removed the sewer. I want to focus development time on the city
  * Wheat farms are now covered in glass, to stop spiders destroying them. Thanks to Curufea for letting me know about that.
  * Added flowers/grass between buildings and farms
  * Outside light sources will now be fires or torches. This can be specified before generating
  * Beacons are now optional
  * Wrote name generators for the taverns, brothels, gravestones, bakery, library, statue and churches
  * Added two city emblems
  * Added mushroom farms
  * Added street names
  * City size now aligns with chunk size, to make the edges a little better

# 1.3 #

  * Added three city emblems (by default Mace will choose a random one, but you can specify if you prefer, or just not have one)
  * Added cactus moats
  * Added a new room to the bottom half of the guard towers, with beds and doors to the city.
  * Added several million squiggly brackets to the code
  * Water moat is now one block higher, so the player and mobs can get out easily
  * Crenels now have a new design. Thanks to Golgrinn for the design and suggestion
  * Fixed the city saplings being unstackable with regular saplings. Thanks to Golgrinn for the bug report
  * The range of city names is now massively increased, thanks to SoNick
  * It's now possible to have paths without buildings, or vice-versa, if you like
  * Added light sources to the inside/outside/top of the walls and guard towers
  * Initial time is now random
  * City saplings are now a random type.
  * Added fire beacons above the guard towers
  * Added orchards
  * Added small hills and ponds in amongst the farms
  * There's now slightly less empty land between the farms and the natural world
  * Some noticeboard messages will now only occur once for each world
  * Right-clicking the city picture on the main screen will show fifty random city names
  * Thanks to Curufea for these suggestions:
    * Fences now appear about 50% of the time on sugarcane farms
    * Some farms will now have hedges instead of fences
    * Maximum size of a farm has been increased from 14 to 24 blocks
    * New moat option: drop to bedrock

# 1.2 #

  * The interface is done. It allows for switching off sections (moat, guard towers, farms, etc) along with setting the moat liquid and city size.
  * Thanks to Curufea for this suggestion:
    * City name data is now stored in two text files: CityStartingWords.txt and CityEndingWords.txt. The city name is made by combining a random word from the first file with a random word from the second file. Feel free to add more words or suggest words to me and I'll add them to the official version.

# 1.1 #

  * Added murder holes above the drawbridges
  * Added some more words to the city name generator
  * The sewer layout now has loops and more tunnels on each level (it's still empty though)
  * Plots are now different sizes
  * Plots are no longer in a rigid grid layout. They look more natural now
  * Plots will now be rotated randomly
  * Added archery slots to the guard towers
  * Added noticeboard
  * Added cactus farms
  * The new version of Substrate has fixed the lighting bugs

# 1.0 #

  * First version!