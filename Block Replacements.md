# Cave Blocks
Determines what to use as "air".
```
caveBlocks: [
  {
    states: ["lava"]
    chance: 1.0
    minHeight: 0
    maxHeight: 10
    noise3D: {Noise3D object}
  }
]
```
- caveBlocks: `[{object} array]`
  - *Optional*


- states: `[String array]`
  - Block to replace air with. *Assumedly required.*


- chance: `float`
  - Chance to occur, out of 1. *Optional, defaults to* `1.0`*.*


- minHeight: `int`
  - Minimum height to occur. *Optional, defaults to* `0`*.*


- maxHeight: `int`
  - Maximum height to occur. *Optional, defaults to* `50`*.*


- noise3D: `{Noise3D object}`
  - See the [Noise3D documentation]() for more information. Exclude if noise-generation is not desired. *Optional.*


# Wall Decoration
Decorates the walls with various blocks.
```
wallDecorators: [
  {
    states: ["clay"]
    chance: 1.0
    minHeight: 10
    maxHeight: 50
    directions: ["north"]
    matchers: ["stone"]
    preference: replace_match
    noise3D: {Noise3D object}
  }
]
```
- wallDecorators: `[{object} array]`
  - *Optional.*


- states: `[String array]`
  - List of blocks to replace with. *Assumedly required.*


- chance: `float`
  - Chance to occur, out of 1. *Optional, defaults to* `1.0`*.*


- minHeight: `int`
  - Minimum height to occur. *Optional, defaults to* `10`*.*


- maxHeight: `int`
  - Maximum height to occur. *Optional, defaults to* `50`*.*


- directions: `[String array]`
  - Direction of wall to replace blocks on. Accepted values are `"north"`, `"south"`, `"east"`, and "`west`". *Optional, defaults to all values.*


- matchers: `[String array]`
  - Blocks to be replaced. *Optional, defaults to* `["stone"]`*.*


- preference: `value`
  - Method of replacement. Accepted values are `replace_match` and `replace_original`. `replace_match` only replaces exact matches, while `replace_original` replaces blocks that started out as the block. For example, ores started out as stone. *Optional, defaults to* `replace_match`*.*


- noise3D: `{Noise3D object}`
  - See the [Noise3D documentation]() for more information. Exclude if noise-generation is not desired. *Optional.*




# Stone Layers
Creates layers of stones, similar to real life deposit buildup.
```
stoneLayers: [
  {
    state: null
    maxHeight: 0
    noise2D: {
      scale: 0.5
      frequency: 0.015
      minVal: -7
      maxVal: 7
    }
  }
]
```
- stoneLayers: `[{object} array]`
  - *Optional. Will not spawn if left out.*


- state: `String`
  - What block the layer should be made up of. *Required to be nonnull generate layers. Defaults to* `null`*.*


- maxHeight: `0`
  - How high the layer should extend. The layer extends downwards until it hits the next lowest layers. *Required to be nonzero to generate layers. Defaults to* `0`*.*


- noise2D: `{Noise2D object}`
  - Optional block to randomize height. `frequency` determines distance between peaks. `minVal` is how far downwards it can extend. `maxVal` is how far above this layer can extend. *Optional, defaults to* `0.015`*,* `-7`*, and* `7`*, respectively.*



# Stone Clusters
Clusters of stone, similar to granite, diorite, and dirt.
```
stoneClusters: [
  {
    states: []
    chance: 0.15
    radiusX: 16
    radiusY: 12
    radiusZ: 16
    radiusVariance: 6
    startHeight: 32
    heightVariance: 16
  }
]
```
- stoneClusters: `[{object} array]`
  - *Optional. Will not spawn if left out.*


- states: `[String array]`
  - List of blocks to put in the cluster. *Required.*


- chance: `float`
  - Spawn probability, out of 1. *Optional, defaults to* `0.15`*.*


- radiusX: `int`
  - Radius of the cluster on the x-axis. *Optional, defaults to* `16`*.*


- radiusY: `int`
  - Radius of the cluster on the y-axis. *Optional, defaults to* `12`*.*


- radiusZ: `int`
  - Radius of the cluster on the z-axis. *Optional, defaults to* `16`*.*


- radiusVariance: `int`
  - Maximum variance in radius. *Optional, defaults to* `6`*.*


- startHeight: `int`
  - Height for clusters to spawn. *Optional, defaults to* `32`*.*


- heightVariance: `int`
  - Maximum variance in spawn height. *Optional, defaults to* `16`*.*
