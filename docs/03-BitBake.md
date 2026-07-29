# BitBake

## What is BitBake?
BitBake is the build engine used by the Yocto Project. It reads recipe files (`.bb`), resolves dependencies, and executes tasks required to build software and generate a Linux image.
---

## Why is BitBake Needed?
Building an Embedded Linux image involves many steps:
- Downloading source code
- Applying patches
- Configuring the source
- Compiling
- Installing files
- Packaging software
- Creating the Root File System (RootFS)
- Generating the final image
BitBake performs these steps automatically based on the instructions defined in recipes.

---
## How I Used BitBake
During my Embedded Linux work, I used BitBake to:

- Build custom Linux images
- Compile packages
- Integrate third-party libraries
- Clean and rebuild packages
- Troubleshoot build failures
- Generate bootable images for different hardware platforms

---

## Common BitBake Commands
### Build an Image
bitbake core-image-minimal
Builds the `core-image-minimal` image.
---
### Build a Specific Recipe
bitbake <recipe-name>
Example:
bitbake asterisk
---
### Clean Build Output
bitbake -c clean <recipe-name>
Removes compiled output while keeping downloaded source files.
---
### Clean Everything
bitbake -c cleansstate <recipe-name>
Removes build output and shared state cache for the recipe, forcing it to rebuild.
---
### List Available Recipes
bitbake-layers show-recipes
Displays all available recipes from the enabled layers.
---
### Show Enabled Layers
bitbake-layers show-layers
Lists all layers included in the build.

## BitBake Build Process
Recipe (.bb)
      │
      ▼
Fetch Source
      │
      ▼
Configure
      │
      ▼
Compile
      │
      ▼
Install
      │
      ▼
Package
      │
      ▼
Create RootFS
      │
      ▼
Generate Image
---
## Common Tasks
- do_fetch
- do_unpack
- do_patch
- do_configure
- do_compile
- do_install
- do_package
- do_rootfs

---
