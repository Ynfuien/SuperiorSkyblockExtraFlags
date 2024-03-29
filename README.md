# SuperiorSkyblockExtraFlags
Module for [SuperiorSkyblock2](https://github.com/BG-Software-LLC/SuperiorSkyblock2) adding extra island flags and privileges. Made for version 1.17.1 but should also work on higher versions.

# List of extra island flags and privileges
## Flags (settings)
- **NATURAL_MONSTER_SPAWN_NORMAL**
- **NATURAL_MONSTER_SPAWN_NETHER**
- **NATURAL_MONSTER_SPAWN_THE_END**

These flags enable or disable natural monster spawn separately for each world.

## Privileges (permissions)
- **USE_BUTTONS** - Allows to use buttons
- **USE_DOORS** - Allows to use doors
- **USE_TRAPDOORS** - And so on...
- **USE_PRESSURE_PLATES**
- **USE_LEVERS**
- **USE_REPEATERS**
- **USE_COMPARATORS**
- **USE_DAYLIGHT_DETECTORS**
- **USE_JUKEBOXES**
- **USE_FENCE_GATES**
- **USE_BEDS**
- **USE_DRIPLEAF**
- **USE_BELLS**
- **USE_COMPOSTERS**
- **USE_CAULDRONS**
- **USE_FLOWER_POTS**
- **USE_ANVILS**
- **USE_BEACONS**
- **USE_ENCHANTING_TABLES**
- **USE_BREWING_STANDS**
- **USE_ENDER_CHESTS**
- **USE_BARRELS**
- **USE_SHULKER_BOXES**
- **USE_HOPPERS**
- **USE_DISPENSERS**
- **USE_DROPPERS**
- **USE_ELYTRA**
- **USE_NETHER_PORTAL**
- **USE_END_PORTAL**
- **SHOOT_CROSSBOW**
- **SHOOT_BOW**
- **THROW_EGGS**
- **THROW_SNOWBALLS**
- **THROW_POTIONS**
- **THROW_EXPERIENCE_BOTTLE**
- **EAT_CAKE**
- **EAT_CHORUS_FRUIT**
- **PAT_DRAGON_EGG**
- **CARVE_PUMPKINS**
- **USE_LECTERNS** - Allows to change book on lectern
- **USE_TRIPWIRES** - Allows to activate tripwire by standing on it
- **USE_NOTE_BLOCKS** - Allows to increase the note pitch up
- **USE_CANDLES** - Allows to light and extinguish candles (also on cake)
- **USE_FURNACES** - Allows to use furnace, blast furnace and smoker
- **USE_CHESTS** - Allows to use chest and trapped chest
- **USE_ARMOR_STANDS** - Allows to manipulate armor stand equipment
- **USE_ITEM_FRAMES** - Allows to take item from and put item in item frame
- **COLLECT_SWEET_BERRIES** - Allows to collect sweet berries from bush
- **COLLECT_GLOW_BERRIES** - Allows to collect glow berries from cave vines
- **COLLECT_HONEY** - Allows to collect honey from bee nest and beehive
- **ROTATE_ITEM_FRAME_ITEMS** - Allows to rotate item in item frame
- **DYE_COLLARS** - Allows to dye wolf/cat collar
- **DYE_SHEEP** - Allows to dye sheep

**Some privileges also deny from destroying block/entity even if player has `BREAK` privilege. These privileges are: `USE_ANVILS`, `USE_BELLS`, `USE_BEACONS`, `USE_BARRELS`, `USE_BREWING_STANDS`, `USE_COMPOSTERS`, `USE_SHULKER_BOXES`, `USE_ENDER_CHESTS`, `USE_ENCHANTING_TABLES`, `USE_HOPPERS`, `USE_DISPENSERS`, `USE_DROPPERS`, `USE_PRESSURE_PLATES`, `USE_FURNACES`, `USE_CHESTS`, `USE_ARMOR_STANDS`, `USE_ITEM_FRAMES`**

### Additionally, in the config you can set your own interact permissions for any blocks you want.

# How to use
## Installation
First of, it's a SS2's module, so you have to put it in the modules folder
`server/plugins/SuperiorSkyblock2/modules`
Then after server start, config should be here
`server/plugins/SuperiorSkyblock2/modules/ExtraFlags/config.yml`
And you can edit all... few options in it 

## Default flags and privileges
Most of extra flags and privileges are replacement for few default ones. So the best way is to enable them by default and to remove them from /is _settings/perms_, so players can't change them.

Those flags are:
- NATURAL_MONSTER_SPAWN

And privileges:
- USE
- CHEST_ACCESS
- ITEM_FRAME

For privilege `INTERACT` I recommend to just edit file `interactables.yml`, so it has other blocks that aren't covered by extra privileges, like loom, stonecutter, smithing table and whatever you want.

## Extra flags and privileges
You must enable by default those extra flags, for proper monsters spawn in each world:
- NATURAL_MONSTER_SPAWN_NORMAL
- NATURAL_MONSTER_SPAWN_NETHER
- NATURAL_MONSTER_SPAWN_THE_END

Default island flags (settings) can be set in `config.yml` of SuperiorSkyblock2 in section `default-settings`

Default island privileges (permissions) for different roles you can set in section `island-roles` also in `config.yml` and I recommend to do it.

If you want to give players access to change these flags and privileges, and I assume you want to, you have to edit files `menus/settings.yml` and `menus/permissions.yml`, and add extra flags/privileges just like default ones. For flag/privilege name use name from the list in lower case.

# Default config
```yml
# SuperiorSkyblockExtraFlags by Ynfuien

messages:
  # Prefix for hex colors in messages.
  # Default: '&#'
  hex-prefix: '&#'

  # Message that will appear when the player isn't allowed to do something on island.
  # Default: '&c&lError | &7This island is protected.'
  island-protected: '&c&lError | &7This island is protected.'

  # Island protected messages for specific permissions, so you can customize messages
  # for every situation. To add new messages just follow the pattern. If you want to
  # disable message, set it empty: ''
  specific-permissions:
    USE_ELYTRA: '&c&lError | &7You can''t fly on this island!'
    USE_BUTTONS: '&c&lError | &7You can''t use buttons on this island!'
    # <permission>: '<message>'

# Custom interact permissions are permissions that you can edit at your own will.
# They restrict interaction with given blocks using RMB (right mouse button).
# You can add to the list almost every block. If you don't want any additional permissions,
# just comment items in the list.
# The end permission for each block will be "INTERACT_<block>".
# !! This function may not work for every block. !!
# !! It's general option and I won't test it with every block. !!
custom-interact-permissions:
  - CRAFTING_TABLE # INTERACT_CRAFTING_TABLE
  - SMITHING_TABLE # INTERACT_SMITHING_TABLE
```