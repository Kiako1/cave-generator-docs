# ScalableFloats
Many of the fields inside of tunnels and ravines are
referred to internally as `ScalableFloats`. These
objects technically all contain the same fields, but
those fields are not used as consistently as in noise
blocks. This is why they are not named according to their
type, unlike noise blocks.

ScalableFloats essentially serve to update a floating-point value each time it gets used. So, their parameters
are a reflection of that process. The basic function of
this type of field is documented below.

```
valueName: {
  startVal: 1.0
  startValRandFactor: 2.0
  factor: 3.0
  randFactor: 4.0
  exponent: 5.0
}
```
- startVal: `float`
  - The initial value. *Requirement status unknown.*


- startValRandFactor: `float`
  - A random value from 0 to `startValRandFactor` is multiplied by `startVal`. *Optional, default unknown.*


- factor: `float`
  - A constant which multiplies the current value when used. *Optional, defaults to* `1.0`*.*


- randFactor: `float`
  - A random value from 0 to `randFactor` which multiplies the current value when used. *Optional, default unknown.*


- exponent: `float`
  - A constant value that the current value is raised to the power of. For example, a value of `3.0` would output `value^3`. *Optional, defaults to* `1.0`*.*




## Shorthand

Despite the inconsistency in terms of which fields are
actually used, their identical structure and use of only
one single value type allows them to be written with a much
prettier syntax. Some users may prefer this syntax thanks
to its concision. The following example shows how this
would look.

Example values. Helps clarify the order.
```
standard: {
  startVal: 1.0
  startValRandFactor: 2.0
  factor: 3.0
  randFactor: 4.0
  exponent: 5.0
}
```
Make sure to use an array here, not an object.
Trailing values (near the end) can be omitted, but
intermediate values cannot, since the order does
matter.
```
shorthand: [ 1.0, 2.0, 3.0, 4.0, 5.0 ]
```
