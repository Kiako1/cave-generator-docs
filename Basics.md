# Basic Fields
```
enabled: true
blankSlate: true
```
- enabled: `boolean`
  - Determines if the preset should be used. All examples have this set to `false` initially. Although this field is optional, it is typically a good idea to include. *Optional, defaults to* `true`*.*


- blankSlate: `boolean`
  - If a feature is missing in the config, this determines if the generator should revert to vanilla defaults or if it should not generate the feature at all. `true` causes it to not use vanilla defaults. *Optional, defaults to* `true`*.*
