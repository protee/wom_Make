<div align="center">

<!-- Header with left text and right logo -->
<div style="display: flex; align-items: center; justify-content: space-between; width: 100%;">
  <div style="text-align: left;">
    <strong style="font-size: 1.2em;">The Genesis Engine</strong><br>
    <strong style="font-size: 1em;">Mantra:</strong> One command, a thousand builts.<br>
    <strong style="font-size: 1em;">Tagline:</strong> Build and more. One breath.
  </div>
  <div>
    <img src="https://www.protee.org/images/wom_Make/wom_Make.png" alt="wom_Make Logo" width="60" style="border-radius: 12px;">
  </div>
</div>

<!-- Title and badges -->
# wom_Make

[![4D Component](https://img.shields.io/badge/4D-Component-blue)](#)
[![License: Commercial](https://img.shields.io/badge/License-Commercial-red.svg)](#license)
[![Platform: macOS & Windows](https://img.shields.io/badge/Platform-macOS%20%7C%20Windows-lightgrey)](#)
[![4D v21+](https://img.shields.io/badge/4D-v21%2B-brightgreen)](#)

</div>

## Overview

wom_Make is a powerful automation tool that streamlines the process of building, packaging, and notarizing your 4D components and databases. It transforms the complex, multi-step build pipeline into a single, repeatable command.

It's a **development component** that eliminates the manual, error-prone tasks associated with preparing your work for distribution, allowing you to focus on development.

---

## Key Features

- **One-Command Build**: Executes a complete build process from a single command, reducing manual steps and potential for errors.
- **Smart Configuration Parsing**: Automatically reads your `buildApp.4DSettings` file to understand your build configuration, including build folder name, and options for Client/Server (CS), standalone (mono), or component builds.
- **Automated Version Archiving**: Automatically creates a timestamped and versioned ZIP archive of your source code (e.g., `2023-0112 woc_Colours 2.2.00 SRC.zip`), making it easy to manage release versions.
- **Post-Build Enhancements**: Automatically adds a versioned "Macro V2" file and `info.plist` to your build.
- **Web Folder Integration**: Seamlessly includes a designated web folder into the final build file.
- **Callback Support**: Allows you to define a callback method in your host database, which is automatically launched after the build process to perform any additional, custom tasks.
- **Complete Notarization Pipeline**: Handles the entire Apple notarization process for macOS distribution, including:
    - **Signing**: Codesigns the built product.
    - **Ditto**: Creates a distributable `.dmg` image.
    - **Notarytool**: Submits the `.dmg` to Apple for notarization and waits for the result.
    - **Stapling**: Staples the notarization ticket to the `.dmg` for offline verification.
- **Customizable Icon**: Displays your product's icon from `Resources/pictures/logo_product.png` in the final build, or a generic one if not found.
- **Exceptionally Simple**: Designed for ease of use, especially for automating the builds of your components.

---

## Installation & Dependencies

### Prerequisites
- **4D v21** or higher (Project mode recommended).
- [**wok_Krolific**](https://github.com/protee/wok_Krolific) – Licensing component (mandatory dependency).
- The [**4D SVG component**](https://github.com/4d/4D-SVG) must be available in your project.

### Installation via Dependencies Manager (GitHub)

Starting with 4D v21, the recommended way to install wom_Make (and any ogTools component) is through the **Dependencies Manager** using the **GitHub repository**:

1. In your 4D project, open the **Dependencies Manager** (`Project > Dependencies`).
2. Click the `+` button and select **Add a dependency from a Git URL**.
3. Enter the following Git URL:`protee/wom_Make`
4. Choose the desired version (e.g., `main`, `latest`, or a specific release tag).
5. Confirm the installation – the component will be automatically fetched from GitHub, placed in the `Components` folder, and linked to your project.

> **Note**: For team development, commit the dependency configuration file (`dependencies.json`) to your source control so all team members automatically fetch the same version from GitHub.

---

## How It Works

1.  **Configuration**: You define your build settings once in the standard `buildApp.4DSettings` file.
2.  **Execution**: You run the `wom_Make` build command.
3.  **Automation**: The component automatically performs the following sequence:
    - Parses your build settings.
    - Archives your source code with a versioned name.
    - Executes the build process.
    - Injects the `Macro V2` and `info.plist` files.
    - Includes your specified web folder.
    - Calls your custom callback method (if provided).
    - Runs the complete notarization pipeline (sign, dmg, notarize, staple).
    - Uses your custom product icon.

---

## Part of the ogTools Suite

wom_Make is the build and automation pillar of the comprehensive **ogTools suite**—an integrated development ecosystem for 4D. Other key components include:

| Component | Description |
|-----------|-------------|
| **wok_Krolific** | Centralized licensing system. |
| **wox_Xlibrary** | Core utilities for everyday development tasks. |
| **zen_Nucleus** | The complete ORDA framework binding your database to a sophisticated UI. |
| **woc_Colours** | Advanced, indexed color management engine. |
| **waz_Wazar** | Intelligent UI widgets for modern interfaces. |
| **wor_Recursive** | Manage hierarchical data with ease. |
| **wob_Boxes** | Secure, Dropbox-like file repository. |
| **wod_DevTools** | Instant documentation generation. |

> Together, these components form a powerful framework that allows developers to focus on unique business logic rather than reinventing the wheel.

---

## License

wom_Make is a **commercial component** and is part of the paid ogTools suite. A valid license is required for use. For licensing options and trial requests, please contact the sales team directly.

---

## Localization

wom_Make supports the following languages out-of-the-box:

- 🇺🇸 English (EN)
- 🇫🇷 French (FR)
- 🇪🇸 Spanish (ES)
- 🇩🇪 German (DE)

Localization affects error messages, UI prompts, and built-in pane texts.

---

## Support & Resources

- **Official Website**: [https://www.protee.org](https://www.protee.org)
- **4D Forum**: [Discuss ogTools suite](https://discuss.4d.com) – A vibrant community for questions and best practices.
- **Documentation**: Full documentation and HDI (Host Database Interface) demos are included with your purchase.

For direct inquiries:
- **Email**: [og@protee.org](mailto:og@protee.org)
- **Phone**: +33 6 3718 5941

---

## About the Creator

wom_Make and the ogTools suite are developed by **Protée sarl**, a company with over 30 years of expertise in 4D development. Led by Olivier Grimbert, the team focuses on delivering high-quality, production-grade tools that enhance developer productivity and application reliability.

---

<div align="center">
  <sub>Built with ❤️ for the 4D community by Protée sarl. © 2016 - Present</sub>
</div>