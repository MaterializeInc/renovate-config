# renovate-config

Shared [Renovate](https://docs.renovatebot.com/) preset for MaterializeInc repos.

```json
{
  "extends": ["github>MaterializeInc/renovate-config"],
  "constraints": { "rust": "1.99.1" }
}
```

`constraints.rust` should match the repo's pinned toolchain; the preset keeps it in sync with the other Rust version references. Libraries that publish an MSRV can stop Renovate from bumping it with a `packageRule` disabling `matchManagers: ["custom.regex"]`, `matchDepNames: ["rust"]`.
