# Cave Generator
The docs are currently up to date with Cave Generator 0.16 for MC 1.12.2. You can get it [here](https://www.curseforge.com/minecraft/mc-mods/cave-generator).

Information has been grouped into the following pages:

- [Basics](), which covers the two basic fields.
- [Spawn Settings](), which has ways to limit generation to biomes and dimensions, and to allows tunneling through blocks.
- [Cave Parts](), which describes rooms, tunnels, ravines, and caverns.
- [Block Replacements](), which includes cave blocks, wall decoration, stone layers, and stone clusters
- [Decorations](), which includes stalactites, stalagmites, pillars, and other structures.
- [Noise Blocks](), which describes a way to use noise for randomization in detail.
- [ScalableFloats](), which provides more information on a datatype used frequently.

As of right now, all defaulting values, except most booleans, are assumptions. `int` datatypes are also assumptions, and may support float values.

## File Format
The format used by these presets is known as Hjson, a less picky and more readable counterpart to normal JSON. It accepts various comment styles, allows trailing commas in arrays, does not require commas in objects when elements are placed on new lines, and has other features that should prevent crashes related to syntax errors. You can visit [the official website](https://hjson.org) for more info on using it.

These presets have been extended with ".cave" by default so as to more clearly indicate their purpose; however, ".json" and ".hjson" are also accepted by the mod.
## Example Presets
Various presets are available, and are used as references throughout this Wiki. You can find each preset in full via the following links.
- [caverns.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/caverns.cave)
- [euclids_tunnels.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/euclids_tunnels.cave)
- [flooded_vanilla.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/flooded_vanilla.cave)
- [large_caves.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/large_caves.cave)
- [large_stalactites.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/large_stalactites.cave)
- [lower_caves.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/lower_caves.cave)
- [ravines.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/ravines.cave)
- [spirals.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/spirals.cave)
- [stalactites.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/stalactites.cave)
- [stone_clusters.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/stone_clusters.cave)
- [stone_layers.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/stone_layers.cave)
- [tunnels.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/tunnels.cave)
- [underground_forest.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/underground_forest.cave)
- [vanilla.cave](https://github.com/PersonTheCat/CaveGenerator/tree/master/src/main/resources/assets/cavegenerator/presets/vanilla.cave)
