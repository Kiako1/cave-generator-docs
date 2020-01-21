# Biomes
The biomes fields are used to restrict which biomes the preset will generate in. The mods Biomes O' Plenty and BiomeTweaker generate configs listing all biomes, and CraftTweaker can also output a list of biomes.
```
biomes: {
  names: []
  IDs: []
  types: []
}
useBiomeBlacklist: false
```
- biomes: `{}`
  - A list of biomes to generate the features of the presets in. *Optional, defaults to all biomes.*


- names:`[String array]`
  - A list of names of biomes to generate features in. For example, `"SAVANNA"`. *Optional list.*


- IDs: `[String array]`
  - A list of IDs of biomes to generate features in. For example, `15`. *Optional list.*


- types: `[String array]`
  - A list of biome types to generate features in. Examples of valid inputs are `"HOT"`, `"ICY"`, `"COLD"`, and `"WARM"`. *Optional list.*


- useBiomeBlacklist: `boolean`
  - If enabled, prevents the preset from loading in the listed biomes, rather than restricting the preset to those biomes. *Optional, defaults to* `false`*.*



# Dimensions
The dimensions fields are used to restrict which dimensions the preset will generate in. The mod BiomeTweaker generates configs listing all dimensions, and CraftTweaker can also output a list of dimensions.
```
dimensions: []
useDimensionBlacklist: false
```
- dimensions: `[int array]`
  - A list of IDs of dimensions to generate the features of the preset in. *Optional, defaults to* `[0]`*.*


- useDimensionBlacklist: `boolean`
  - If enabled, prevents the preset from loading in the listed dimensions, rather than restricting the preset to those dimensions. *Optional, defaults to* `false`*.*



# Replaceable Blocks
These fields are used to decide where tunnels can be generated in.
```
replaceableBlocks: ["stone", "dirt"]
replaceDecorators: true
```
- replaceableBlocks: `[String array]`
  - A list of blocks the generator should replace. At the time of cave generation, typically only dirt, stone, and water have been generated. Use this field if another mod is adding decoration early on. *Optional, defaults to* `["stone", "dirt"]`*.*


- replaceDecorators: `boolean`
  - Allows various decorators to be replaced by tunnels. Should be enabled to prevent floating decorators when caves intersect. *Optional, defaults to* `???`*.*
