# setup-tofu

The m0un10/setup-tofu action is a composite action that sets up OpenTofu CLI in your GitHub Actions workflow.

Until release binaries exist for OpenTofu, it will build from the source. This can take a couple of minutes at first but it is cached for subsequent runs.

## Usage

The OpenTofu CLI can be installed with a one-liner

```
steps:
- uses: m0un10/setup-tofu@main
- run: tofu --version
```

Or, it can build and install from a specific upstream branch of [opentofu](https://github.com/opentofu/opentofu)

```
steps:
- uses: hashicorp/setup-terraform@v2
  with:
    tofu_version: feature-branch-x
```
