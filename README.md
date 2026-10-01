# Platform Workflows

This repository owns reusable GitHub Actions orchestration. Application
repositories consume versioned workflows through `workflow_call`.

## Friday golden-path compatibility

| Platform workflow release | Golden-path implementation |
| --- | --- |
| `v2.0.0` | `stevenhart235-dev/platform-golden-path@v0.5.0` |
| `v2.0.1` | `stevenhart235-dev/platform-golden-path@v0.5.0` |
| proposed `v2.1.0` | proposed `stevenhart235-dev/platform-golden-path@v0.6.0` |

The Friday reusable workflow owns this dependency pin. Consumers select only
the platform workflow release and cannot override the internal golden-path
version.

The proposed V6.1 release adds platform-owned AzureRM remote-state
initialization to the trusted-plan workflow. The workflow continues to perform
normalization and governance validation before Azure authentication and
remains plan only.
