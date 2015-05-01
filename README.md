#Institute system documentation
This system was commissioned by Portius and developed by Rialorm. It requires Vadi’s m&m to function.

##Target
**`t <target>`** - This alias sets and highlights your target. It only accepts a single word, so use the base noun to target mobiles. This is case sensitive, meaning if you enter “t portius” that Portius won’t be highlighted.

**`tcol <colour>`** - This alias sets the colour to highlight in and will save this configuration to the settings file. Mudlet’s showColor() function lists what colours are available to use. Some simple accepted values are red, green or blue.

##Tarot
**`fl <name> [g]`** - A smart function that will attempt to fling your chosen card at an appropriate target. Uses an inventory tracker to determine whether you already have such a card in your inventory, and if not will outdeck one for you to use. Targeted cards such as hangedman will be flung at the target, while cards such as princess will be flung at the ground. Hermit will outdeck and activate one if none are in the inventory, if one is then it will fling this at the ground. Tracking and management of multiple hermit cards is not possible. Lust will be flung at the target unless the g modifier is added at the end, in which case it will be flung at the ground. Soulless will sniff the card and rub it or fling it depending on the number of imprints.

**`acther`** - Manually outdeck and activate a hermit card. 

##Aeonics
**`tc <skill> [t]`** - Smart timechanting of skills, either untargeted for spells such as alacrity or on the target for directed spells like aeon. Timequake can be cast on the target with the modifier t, or untargeted without the modifier. 

##Harmonics
**`cpall`** - Starts a sequence which takes one of each gem out of the gem rift and spins it, ending with deactivating all gems in the crystalplex.

**`cp <gem> [e|enemies|affliction]`** - Smart function that will take the needed gems out of the rift and spin them. If a targeted combination such as ruby is chosen, it will spin this at the target. An untargeted one such as mendingstone will simply be spun. Malefactgem will target enemies when the modifier e, enemies, or no modifier is chosen. If the name of a valid affliction (such as paralysis) or it’s first letter (such as p) is entered as modifier then malefactgem will be cast at the target with this respective affliction. If a single gem is chosen, such as jade, it will take one from the rift and spin that. 

**`cphostile`** - Points all hostile crystalplex gems to your target.

**`cpfriendly [name]`** - Points all friendly crystalplex gems to the name, or to yourself if no modifier is chosen.

##Configuration
The package will create a file called institute.lua in your profile folder which stores the package settings. The settings file only gets overwritten on correct logout (praying), or when the tc alias is used. This means that if you set your target and then shut down the client incorrectly, it will not be preserved and instead next time will load whatever the last saved target was. Targets change often and writing to disk every time this happens could cause slowdowns and results in a lot of wasteful writing operations. 

When you load your profile, the package will attempt to fetch the last stored configuration. 
