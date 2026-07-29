# Yocto Layers

## What are Layers?
A layer is a collection of metadata such as recipes, configuration files, classes, and patches used by the Yocto Project.
Layers help organize software components and make it easier to add, remove, or customize functionality without modifying the core Yocto files.

---

## Why are Layers Used?
Instead of keeping everything in one place, Yocto separates functionality into different layers.

This approach allows developers to:
- Organize recipes
- Add support for new hardware
- Include third-party software
- Maintain custom project configurations
- Reuse existing metadata
---

## Common Layers
### meta
Contains the OpenEmbedded-Core metadata, including common recipes and classes required for building Linux images.
### meta-poky
Contains Poky-specific configuration files.
### meta-yocto-bsp
Provides Board Support Package (BSP) metadata for supported hardware platforms.
### meta-openembedded
Provides additional community-maintained recipes that are not part of the core metadata.
Examples include:
- Networking packages
- Multimedia libraries
- Python packages
- Development tools
### Custom Layer
A project can also contain its own custom layer.

For example:
meta-myproject
This layer can contain:
- Custom recipes
- Image recipes
- Configuration files
- Application packages

---

## Layer Structure
Example:
meta-myproject/
conf/
recipes-core/
recipes-apps/
recipes-kernel/
classes/


---

## Layer Configuration

Layers are enabled in:
build/conf/bblayers.conf
This file tells BitBake which layers should be included during the build.


## Useful Command
bitbake-layers show-layers
Displays all enabled layers.


## How I Used Layers

During my Embedded Linux work, I worked with multiple layers such as:
- poky
- meta-openembedded
- meta-raspberrypi
- meta-qt5
- project-specific custom layers

These layers were used to build Linux images for different hardware platforms and to integrate required packages and libraries.

