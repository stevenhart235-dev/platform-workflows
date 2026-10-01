# Platform Workflows

This repository owns reusable GitHub Actions orchestration. Application
repositories consume versioned workflows through `workflow_call`.

## Friday golden-path compatibility

| Platform workflow release | Golden-path implementation |
| --- | --- |
| `v2.0.0` | `stevenhart235-dev/platform-golden-path@v0.5.0` |

The Friday reusable workflow owns this dependency pin. Consumers select only
the platform workflow release and cannot override the internal golden-path
version.

Both listed releases are publication prerequisites. The golden-path release
must exist before the workflow release is made available to consumers.
