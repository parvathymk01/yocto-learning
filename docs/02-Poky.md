# Poky

## What is Poky?
Poky is the reference build system provided by the Yocto Project. It includes everything needed to start building Embedded Linux images, such as BitBake, metadata, and example configurations.

---
## What does Poky include?
Poky consists of:
- BitBake (build engine)
- OpenEmbedded-Core metadata
- Example BSPs
- Build configuration files
- Sample Linux images

---

## Why is Poky important?
Poky provides a complete starting point for building custom Embedded Linux distributions. Instead of creating everything from scratch, developers can use Poky and add their own layers, recipes, and configurations.
---

## How I Used Poky
During my work, I used the Poky build environment to:
- Configure the build environment
- Build Linux images
- Add custom metadata layers
- Integrate third-party libraries
- Customize images for Intel x86, Raspberry Pi CM4, and TI AM62 platforms
---

## Typical Directory Structure
poky/
├── bitbake/
├── meta/
├── meta-poky/
├── meta-yocto-bsp/
├── build/
└── oe-init-build-env


---
## Important Components

### bitbake/
Contains the BitBake build tool.

### meta/
Contains the OpenEmbedded-Core metadata, including common recipes and classes.

### meta-poky/
Contains Poky-specific configuration.

### meta-yocto-bsp/
Contains Board Support Package (BSP) metadata for supported hardware.

### oe-init-build-env
A script used to initialize the Yocto build environment.
---

## source oe-init-build-env
This command sets up the environment and creates (or enters) the build directory.
---

