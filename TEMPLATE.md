#### Bundle `metadata.json`

``` json
{
  "metadata_version": 1,
  "bundle": "my-bundle",
  "target": "b2p",
  "display_name": "My Bundle!",
  "description": "A collection of curated recipes for a specific environment.",
  "kernels": ["linux", "windows-nt"],
  "architectures": ["arm64", "i686", "x86_64"],
  "tags": ["cli", "bundle", "collection"],
  "categories": ["development"],
  "aliases": ["my-coolest-bundle", "cool-bundle"],
  "maintainers": ["My self", "My team"],
  "default": {
    "gnu-linux": {
      "flavor": "vanilla",
      "bundle_version": "1.0.0"
    },
    "windows": {
      "flavor": "vanilla",
      "bundle_version": "1.0.0"
    }
  }
}
```

#### Bundle `manifest.json`

``` json
{
  "manifest_version": 1,
  "b2p_requirement": ">=1.0.0",
  "bundle": "my-bundle",
  "bundle_version": "1.0.0",
  "flavor": "vanilla",
  "environment": {
    "kernel": "windows-nt"
  },
  "recipes": [
    {
      "package": "tool-alpha",
      "recipe_version": "latest",
      "package_version": ">=1.0 <2.0"
    },
    {
      "package": "tool-beta",
      "recipe_version": "1.5.0",
      "package_version": "any"
    },
    {
      "package": "extra-config-lib",
      "recipe_version": "1.0.0"
    }
  ]
}
```

#### Generic `label.md`

``` md
# My Bundle

> A short, punchy tagline that describes the flavor of this bundle.

## ✨ Highlights

- **Key Feature 1:** Why is this bundle special?
- **Key Feature 2:** What problem does it solve?
- **Key Feature 3:** Why download the `b2p` version?

## 🚀 Quick Taste

Example command to show the app in action:

    my-app --help

## 📝 About

A more detailed description of the ingredients and what the user can expect after the installation.
```