# Noise Blocks
Noise blocks are a common way to produce controlled randomization. Minecraft uses this to determine the topology of the surface, among many other things.

The majority of all noise parameters below have            
equivalent counterparts in the standard FastNoise library. The easiest way to learn what they do is to visit [this link]() and see them in action. It would be a great idea to download the FastNoise preview application and try changing the parameters on your own to get a fast, graphical representation of how your changes will look in-game.   

## Noise2D
Noise2D objects are used anywhere where values are relative to (x, z) coordinates. This can be used to determine the minimum or maximum height of a block or determine whether a particular horizontal space is acceptable for decoration based on a threshold which is calculated from `scale`.

```
noise2D: {
  scale: 1.0
  frequency: 2.0
  minVal: 8
  maxVal: 16
}
```
- noise2D: `{Noise2D object}`
  - *Optional. Only include a Noise2D object in your code if you want randomization based on Noise.*


- scale: `float`
  - Limits the range of acceptable values. In a sense, this increases or decreases the width of each peak of values generated (such as making a steeper or flatter mountain.) In most cases throughout this mod, changing the scale in a noise block alters the size of each area that gets decorated. This parameter is only used whenever the noise generator is used to produce a boolean. It works by scaling the threshold of acceptable values. *Assumedly required.*


- frequency: `float`
  - Alters the distance between peaks of values. *Assumedly required.*


- minVal: `int`
  - The minimum value to be produced by the generator. *Assumedly required.*


- maxVal: `int`
  - The maximum value to be produced by the generator. For example, this is why you don't see mountains >>y=180. *Assumedly required.*



## Noise3D                      
Noise3D objects are used anywhere where values are relative to (x, y, z) coordinates. This will produce 3-dimensional clusters of space. For example, rock clusters are generated with Noise3D. Just because one y-coordinate is valid does not imply everything below it is also valid.
```
noise3D: {
  scale: 1.0
  frequency: 2.0
  scaleY: 1.0
  lacunarity: 1.0
  gain: 0.5
  jitter: 0.45
  octaves: 1
  perturb: false
  perturbAmp: 1.0
  perturbFreq: 0.1
  invert: false
  type: "SimplexFractal"
  interp: "Hermite"
  fractal: "FBM"
  distFunc: "Euclidian"
  returnType: "Distance2"
  cellularLookup: "Simplex"
}
```
- noise3D: `{Noise3D object}`
  - *Optional. Only include a Noise3D object in your code if you want randomization based on Noise.*


- scale: `float`
  - Limits the range of acceptable values. In a sense, this increases or decreases the width of each peak of values generated (such as making a steeper or flatter mountain.) In most cases throughout this mod, changing the scale in a noise block alters the size of each area that gets decorated. This parameter is only used whenever the noise generator is used to produce a boolean. It works by scaling the threshold of acceptable values. *Assumedly required.*


- frequency: `float`
  - Alters the distance between peaks of values. *Assumedly required.*


- scaleY: `float`
  - Stretches and skews the scale on the vertical axis. Literally causes clusters to be shorter or taller.


- lacunarity: `float`
  - The octave lacunarity of fractal noise types. Higher values produce deeper and more precise fractals. *Optional, defaults to* `1.0`*.*


- gain: `float`
  - The octave gain for fractal noise types. *Optional, defaults to* `0.5`*.*


- jitter: `float`
  - The maximum distance a cellular point can move from its grid position when using cellular types. *Optional, defaults to* `0.45`*.*


- octaves: `int`
  - The number of generation passes. This effectively increases the resolution of clusters (makes them less smooth) at the cost of performance. *Optional, defaults to* `1`*.*

- perturb: `boolean`
  - Whether to apply a gradient perturb all values input to the noise generator, warping the output. *Optional, defaults to* `false`*.*


- perturbAmp
  - Sets the maximum amount to warp coordinates when perturb is enabled. *Optional, defaults to* `1.0`*.*


- perturbFreq
  - The frequency used in warping input coordinates. *Optional, defaults to* `0.1`*.*


- invert: `boolean`
  - Inverts the noise generator's output. *Optional, defaults to* `false`*.*


- type: `NoiseType value from String`
  - The type of noise to be used by the generator. Values include: `Value`, `ValueFractal`, `Perlin`, `PerlinFractal`, `Simplex`, `SimplexFractal`, `Cellular`, `WhiteNoise`, `Cubic`, and `CubicFractal`. Case insensitive. *Optional, defaults to* `SimplexFractal`*.*


- interp: `Interp value from String`
  - The type of interpolation to use. Values include: `Linear`, `Hermite`, and `Quintic`. Case insensitive. *Optional, defaults to* `Hermite`*.*


- fractal: `FractalType value from String`
  - Determines how the noise will be fractalized, when applicable. Values include: `FBM`, `Billow`, and `RigidMulti`. Case insensitive. *Optional, defaults to* `FBM`*.*


- distFunc: `CellularDistanceFunction type from String`
  - The type of distance function in cellular noise calculations. Values include: `Euclidian`, `Manhattan`, and `Natural`. Case insensitive. *Optional, defaults to* `Euclidian`*.*


- returnType: `CellularReturnType type from String`
  - The return type from cellular noise calculations. Possible values include: `CellValue`, `NoiseLookup`, `Distance`, `Distance2`, `Distance2Add`, `Distance2Sub`, `Distance2Mul`, `Distance2Div`, `Distance3`, `Distance3Add`, `Distance3Sub`, `Distance3Mul`, and `Distance3Div`. Case insensitive. *Optional, defaults to* `Distance2`*.*


- cellularLookup: `NoiseType type from String`
  - Sets the noise type when `returnType: NoiseLookup`. See `type` for possible values. *Optional, defaults to* `Simplex`*.*
