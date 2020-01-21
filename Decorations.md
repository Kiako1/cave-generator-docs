# Stalactites and Stalagmites
Pointing structures formed from sediment deposited by dripping water. Stalactites are on the ceiling, and stalagmites are on the ground.
```
largeStalactites: [
  {
    state: null
    wide: true
    maxLength: 3
    chance: 0.167
    minHeight: 11
    maxHeight: 55
    matchers: []
    noise2D: {
      scale: 0.7125
      frequency: 0.025
      minVal: -1
      maxVal: 1
    }
  }
]
```
- largeStalactites: `[{object} array]`
  - *Optional. Will not spawn if left out.*


- state: `String`
  - Block it should be made of. *Required.*


- wide: `boolean`
  - If `true`, will generate full-sized stalactites. *Optional, defaults to* `true`*.*


- maxLength: `int`
  - Maximum number of blocks the structure can be.


- chance: `float`
  - Chance to spawn, out of 1. *Optional, defaults to* `true`*.*


- minHeight: `int`
  - Minimum y value to spawn a stalactite. *Optional, defaults to* `true`*.*


- maxHeight: `int`
  - Maximum y value to spawn a stalactite. *Optional, defaults to* `true`*.*


- matchers: `[String array]`
  - Block to be attached to. *Optional, defaults to* `true`*.*


- noise2D: `{Noise2D object}`
  - Optional, performs better without. `minVal` and `maxVal` are not used. *Optional.*


```
largeStalagmites: []
```
- largeStalagmites: `[{object} array]`
  - Uses the exact same values as `largeStalactites`. *Optional. Will not spawn if left out.*


# Pillars
```
giantPillars: [
  {
    state: null
    stairBlock: null
    frequency: 15
    minHeight: 10
    maxHeight: 50
    minLength: 4
    maxLength: 12
  }
]
```
- giantPillars: `[{object} array]`
  - *Optional. Will not spawn if left out.*


- state: `String`
  - Block that makes up the body of the pillar. *Required.*


- stairBlock: `String`
  - Block that makes up the stairs. Cannot be null. *Optional, will not spawn stairs if left out.*


- frequency: `int`
  - Number of spawn tries per chunk. *Optional, defaults to* `15`*.*


- minHeight: `int`
  - Minimum y value for a pillar to spawn. *Optional, defaults to* `10`*.*


- maxHeight: `int`
  - Maximum y value for a pillar to spawn. *Optional, defaults to* `50`*.*


- minLength: `int`
  - Minimum pillar height. *Optional, defaults to* `4`*.*


- maxLength: `int`
  - Maximum pillar height. *Optional, defaults to* `12`*.*


# Custom Structures
Structures are ideal for small decorations. Larger decorations (Larger than 16x16) may cause cascading generation lag and should be handed by another mod, such as Recurrent Complex or OTG. Structures will be centered around X and Z, but not Y. Most of this information can be left out.
```
structures: [
  {
    name: null
    integrity: 1.0
    offset: [0, 0, 0]
    frequency: 1
    chance: 0.05
    minHeight: 10
    maxHeight: 50
    airMatchers: []
    solidMatchers: []
    nonSolidMatchers: []
    waterMatchers: []
    debugSpawns: false
    rotateRandomly: false
  }
]
```
- structures: `[{object} array]`
  - *Optional. Will not spawn if left out.*


- name: `Resource location or File name`
  - The resource location or file name. Cannot be null. *Required.*


- integrity: `float`
  - The 0.0-1.0 ratio of blocks to retain when spawning. *Optional, defaults to* `1.0`*.*


- offset: `[int array]`
  - The X, Y, and Z spawn offset. *Optional, defaults to* `[0,0,0]`*.*


- frequency: `int`
  - Number of tries per chunk. Should be low. *Optional, defaults to* `1`*.*


- chance: `float`
  - Chance of success, out of 1. *Optional, defaults to* `0.05`*.*


- minHeight: `int`
  - *Optional, defaults to* `false`*.*


- maxHeight: `int`
  - *Optional, defaults to* `false`*.*


- airMatchers: `[[int array] array]`
  - Blocks that must be air. See below. *Optional.*


- solidMatchers: `[[int array] array]`
  - Blocks that must be solid. See below. *Optional.*


- nonSolidMatchers: `[[int array] array]`
  - Blocks that must be nonsolid. See below. *Optional.*


- waterMatchers: `[[int array] array]`
  - Blocks that must be water. See below. *Optional.*


- debugSpawns: `boolean`
  - If `true`, will log the coordinates every time the structure successfully is spawned. *Optional, defaults to* `false`*.*


- rotateRandomly: `boolean`
  - If `true`, the structure will be rotated when spawning. If `false`, it can only face the predetermined way. *Optional, defaults to* `false`*.*


## Matchers
A place to list relative coordinates that *must* be a certain state (air, solid, nonsolid, or water.) Format should be as an array of coordinate arrays, relative to the origin defined by `offset`. See below for an example.
```
airMatchers: [
  [0, 1, 0],
  [0, 3, 0]
]
```
