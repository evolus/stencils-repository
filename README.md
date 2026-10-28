# Evolus Pencil Stencils Repository

This repository serves as the central distribution catalog and storage repository for stencil collections, templates, and vector icon resource bundles used by [Evolus Pencil](https://pencil.evolus.vn/), the open-source GUI prototyping and wireframing application.

Pencil utilizes structured XML repository definition feeds to discover, index, download, and install collections directly from within the application or via manual archive imports.

---

## Table of Contents

- [Overview](#overview)
- [How to Install and Use Stencils in Pencil](#how-to-install-and-use-stencils-in-pencil)
  - [Method 1: Direct In-App Installation](#method-1-direct-in-app-installation)
  - [Method 2: Manual Installation via ZIP Package](#method-2-manual-installation-via-zip-package)
  - [Method 3: Adding Custom Repository Feeds in Pencil](#method-3-adding-custom-repository-feeds-in-pencil)
- [Stencil Repository Sources](#stencil-repository-sources)
  - [1. Official Core Repository (`repository.xml`)](#1-official-core-repository-repositoryxml)
  - [2. Evolus Extended Collections and Resource Bundles (`repository-evolus.xml`)](#2-evolus-extended-collections-and-resource-bundles-repository-evolusxml)
  - [3. Legacy and Outdated Collections Archive (`repository-outdated.xml`)](#3-legacy-and-outdated-collections-archive-repository-outdatedxml)
- [License](#license)

---

## Overview

Stencils in Pencil are reusable visual components, diagrams, and vector shapes grouped into structured packages. A collection package contains shape definitions, geometry rules, properties, and preview metadata packaged as a compressed `.zip` archive.

This repository provides three distinct XML catalog feeds tailored for different project needs and platform compatibility:

1. **Official Core Repository (`repository.xml`)**: The standard collection feed preconfigured in Pencil, covering wireframes, modern Material Design components, and core authoring utilities.
2. **Evolus Extended Collections & Icon Bundles (`repository-evolus.xml`)**: Extended UI widgets, database schema shapes, and modern vector icon suites (Bootstrap Icons, Font Awesome, Heroicons, Lucide, Tabler) hosted directly in this repository.
3. **Legacy Collections Archive (`repository-outdated.xml`)**: Preserved historical stencils for older UI platforms and legacy mockups (Android ICS, early iOS, Dojo, ExtJS).

---

## How to Install and Use Stencils in Pencil

### Method 1: Direct In-App Installation

Pencil features an integrated collection browser that connects directly to configured repository feeds:

1. Open Evolus Pencil.
2. Navigate to **Tools** > **Manage Collections...**, then click **Install From Repository...**.
3. Select the desired repository source from the dropdown to browse available online collections.
4. Locate the desired stencil collection or icon bundle and click **Install**. Pencil downloads and activates the collection automatically.

### Method 2: Manual Installation via ZIP Package

If you work in an offline environment or prefer downloading packages manually:

1. Browse the collection tables below and download the target `.zip` package using the direct download link.
2. Open Evolus Pencil.
3. Navigate to **Tools** > **Manage Collections...**, then click **Install From File...**.
4. Select the downloaded `.zip` file.
5. The collection will be validated and loaded into your stencil library immediately.

### Method 3: Adding Custom Repository Feeds in Pencil

You can register additional repository XML feeds (such as `repository-evolus.xml`) into Pencil's advanced preferences:

1. Open Evolus Pencil and select **Settings...** from the main menu.
2. In the Settings dialog, switch to the **Advanced** tab.
3. In the **Preference Name** filter field, type `repo` to display repository-related configuration keys.
4. Select the `collection.repo.extra_repo_urls` row to open the editing prompt dialog.
5. In the input box, enter the repository label and raw XML feed URL using the format `Name=URL`. For example, to add the Evolus Extended repository:
   ```text
   Evolus=https://raw.githubusercontent.com/evolus/stencils-repository/master/repository-evolus.xml
   ```
   *(Note: Multiple repositories can be configured by separating each entry with a pipe `|` character, for example: `Repo1=URL1|Repo2=URL2`)*
6. Click **OK** to save the preference, then click **Close** to exit Settings.
7. Open **Tools** > **Manage Collections...** and click **Install From Repository...**. The newly added repository source will now appear in the repository selector for in-app browsing and installation.

---

## Stencil Repository Sources

### 1. Official Core Repository (`repository.xml`)

- **Feed URL:** `https://raw.githubusercontent.com/evolus/stencils-repository/master/repository.xml`
- **Identifier:** `sys:official`
- **Status:** Default active core repository

This is the primary repository bundled with modern versions of Pencil. It includes foundational wireframing components, responsive desktop and mobile Material Design stencils, quality control markup tools, and vector icon bundles.

| Collection | Description | Version | Last Updated | Author & License | Download |
| :--- | :--- | :---: | :---: | :--- | :---: |
| **Generic Wireframe**<br>`dgthanhan.GenericWireframe` | Low-fidelity placeholder shapes, form layouts, and typography elements for rapid UI wireframing. | 1.0<br>*(Pencil 3.0.2+)* | <nobr>2017-05-09</nobr> | Dương Thành An<br>`MIT` | [Download ZIP](https://github.com/dgthanhan/stencils/releases/download/SB-1.0-WF/GenericWireframe-1.0.zip) |
| **Desktop Material Mockup**<br>`dgthanhan.MaterialDesktopMockup` | Desktop application components and stencils designed following Google Material Design guidelines. | 1.0.4<br>*(Pencil 3.0.4+)* | <nobr>2019-08-15</nobr> | Dương Thành An<br>`MIT` | [Download ZIP](https://github.com/dgthanhan/stencils/releases/download/DMM1.0.4/DesktopMaterialMockup-1.0.4.zip) |
| **Community Material Vector Icons**<br>`icons.CommunityMaterialIcons` | Material icon resource bundle contributed by community developers and designers. | 1.1<br>*(Pencil 3.0.2+)* | <nobr>2026-06-01</nobr> | Contributors<br>`OFL-1.1` | [Download ZIP](https://github.com/evolus/stencils-repository/raw/refs/heads/master/ResourceBundles/CommunityMaterialIconsResourceBundle-1.1.zip) |
| **Mobile Material Mockup**<br>`dgthanhan.AndroidNougatWireframe` | Mobile UI components for prototyping Android and touch applications in Material Design style. | 0.9<br>*(Pencil 3.0.4+)* | <nobr>2017-06-27</nobr> | Dương Thành An<br>`MIT` | [Download ZIP](https://github.com/dgthanhan/stencils/releases/download/MMM091/MobileMaterialMockup-0.9.1.zip) |
| **Stencil Builder Shapes**<br>`Evolus.UI.StencilBuilder` | Primitives, metadata shapes, and structural elements designed for creating custom Pencil stencils. | 1.1<br>*(Pencil 3.0.2+)* | <nobr>2017-07-14</nobr> | Dương Thành An<br>`MIT` | [Download ZIP](https://github.com/dgthanhan/stencils/releases/download/SB-1.1/StencilBuilder-1.1.zip) |
| **Gnome 3 Widgets**<br>`Evolus.UI.Gnome3` | Basic set of desktop widget stencils for designing Linux applications under Gnome 3 HIG. | 1.0 | <nobr>2017-03-26</nobr> | Dương Thành An<br>`MIT` | [Download ZIP](https://github.com/dgthanhan/stencils/releases/download/v1.0.0/Gnome3UI-1.0.zip) |
| **Evolus QC Tools**<br>`evolus.QCTools` | Annotation markers, callout tags, and numbering pins tailored for bug tracking and design reviews. | 1.0<br>*(Pencil 3.0.4+)* | <nobr>2017-07-13</nobr> | Dương Thành An<br>`MIT` | [Download ZIP](https://github.com/dgthanhan/stencils/releases/download/QCTools-1.0/QCTools-1.0.zip) |

---

### 2. Evolus Extended Collections and Resource Bundles (`repository-evolus.xml`)

- **Feed URL:** `https://raw.githubusercontent.com/evolus/stencils-repository/master/repository-evolus.xml`
- **Status:** Extended repository hosted directly in this Git repository

This feed contains modern stencil packs, diagramming kits, and curated vector icon resource bundles. All assets are self-contained within this repository under dedicated folders and the `ResourceBundles/` directory.

#### UI and Diagram Collections

| Collection | Description | Version | Last Updated | Author & License | Download |
| :--- | :--- | :---: | :---: | :--- | :---: |
| **Simple Database Schema**<br>`dgthanhan.ERDSimple` | Basic entity-relationship diagrams and table schema shapes for database architecture. | 1.0 | <nobr>2019-10-08</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/dgthanhan.ERDSimple/dgthanhan_ERDSimple-1.0.zip) |
| **MDM - Data Widgets**<br>`evolus.mdm.data` | Supplemental data visualization widgets, tables, and metric displays. | 1.0 | <nobr>2019-10-08</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/evolus.mdm.data/evolus_mdm_data-1.0.zip) |
| **Ultimate Note Collection**<br>`dgthanhan.UltimateNote` | Styled sticky notes, callout cards, and documentation blocks for canvas notes. | 1.0 | <nobr>2019-10-08</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/dgthanhan.UltimateNote/dgthanhan_UltimateNote-1.0.zip) |
| **Uncategorized Shapes**<br>`evolus.Uncategorized` | General-purpose shapes, indicators, and structural helpers. | 1.0 | <nobr>2023-12-15</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/Uncategorized/evolus_Uncategorized-1.0.zip) |
| **Meme 01**<br>`dgthanhan.Meme01` | Standard meme templates for presentations and informal diagrams. | 1.0 | <nobr>2019-10-08</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/dgthanhan.Meme01/dgthanhan_Meme01-1.0.zip) |
| **Rage Comic Faces**<br>`dgthanhan.Meme02` | Vector character faces for storyboarding and social communication mockups. | 1.0 | <nobr>2019-10-08</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/dgthanhan.Meme02/dgthanhan_Meme02-1.0.zip) |

#### Vector Icon Resource Bundles

These packages provide clean, scalable SVG vector icon sets that integrate into Pencil's resource browser:

| Collection | Description | Version | Last Updated | Author & License | Download |
| :--- | :--- | :---: | :---: | :--- | :---: |
| **Bootstrap Official Icons**<br>`bootstrapOfficalIcons` | Official vector icons from the Bootstrap framework. | 1.0 | <nobr>2026-06-02</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/ResourceBundles/bootstrapOfficalIcons/bootstrapOfficalIcons-1.0.zip) |
| **Font Awesome Icons**<br>`fontawesomeIcons` | Font Awesome vector iconography for general web and application UI. | 1.0 | <nobr>2026-06-02</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/ResourceBundles/fontawesomeIcons/fontawesomeIcons-1.0.zip) |
| **Glow UI Icons**<br>`glowIcons` | Modern minimalist Glow UI icon set. | 1.0 | <nobr>2026-06-02</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/ResourceBundles/glowIcons/glowIcons-1.0.zip) |
| **Heroicons Outline Icons**<br>`heroiconsOutlineIcons` | Tailwind Labs Heroicons 24px outlined line style. | 1.0 | <nobr>2026-06-02</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/ResourceBundles/heroiconsOutlineIcons/heroiconsOutlineIcons-1.0.zip) |
| **Heroicons Solid Icons**<br>`heroiconsSolidIcons` | Tailwind Labs Heroicons 20px/24px solid filled style. | 1.0 | <nobr>2026-06-02</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/ResourceBundles/heroiconsSolidIcons/heroiconsSolidIcons-1.0.zip) |
| **Lucide Icons**<br>`lucideIcons` | Community-maintained fork of Feather Icons with extensive symbol coverage. | 1.0 | <nobr>2026-06-02</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/ResourceBundles/lucideIcons/lucideIcons-1.0.zip) |
| **Tabler Filled Icons**<br>`tablerFilledIcons` | Tabler design system filled vector icons. | 1.0 | <nobr>2026-06-02</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/ResourceBundles/tablerFilledIcons/tablerFilledIcons-1.0.zip) |
| **Tabler Outline Icons**<br>`tablerOutlineIcons` | Tabler design system outlined stroke vector icons. | 1.0 | <nobr>2026-06-02</nobr> | dgthanhan<br>`MIT` | [Download ZIP](https://raw.githubusercontent.com/evolus/stencils-repository/master/ResourceBundles/tablerOutlineIcons/tablerOutlineIcons-1.0.zip) |

---

### 3. Legacy and Outdated Collections Archive (`repository-outdated.xml`)

- **Feed URL:** `https://raw.githubusercontent.com/evolus/stencils-repository/master/repository-outdated.xml`
- **Identifier:** `sys:outdated`
- **Status:** Archived repository for legacy support

This catalog contains historical collections maintained to preserve backward compatibility for legacy `.ep` and `.epz` documents. While these kits may not represent current mobile or web design guidelines, they remain accessible for opening or updating older design documents.

| Collection | Description | Version | Last Updated | Author & License | Download |
| :--- | :--- | :---: | :---: | :--- | :---: |
| **Mobile - Android ICS**<br>`Evolus.AndroidICSHIFI` | High-fidelity UI elements for Android 4.0 Ice Cream Sandwich. | 1.0 | <nobr>2016-05-26</nobr> | Evolus Pencil Team<br>`GPL` | [Download ZIP](http://evoluspencil.googlecode.com/files/Android.GUI_v2.zip) |
| **Ext JS Neptune**<br>`extJSKitchenSink` | Desktop web interface widgets styled after Sencha Ext JS Neptune theme. | 1.0 | <nobr>2016-05-26</nobr> | Evolus Pencil Team<br>`GPL` | [Download ZIP](https://googledrive.com/host/0B3r4pjcouweYYnF6MXNFNFo2Q00/ExtJSKitchenSink-Neptune-v0.9.zip) |
| **Mobile - iOS UI Stencils**<br>`Evolus.iOS` | High-fidelity stencils for classic iPhone and iPad interface mockups. | 1.0 | <nobr>2016-05-26</nobr> | Evolus Pencil Team<br>`GPL` | [Download ZIP](http://evoluspencil.googlecode.com/files/iOS.GUI_v2.zip) |
| **Mobile - iOS Wireframe**<br>`Evolus.iOSWireframe` | Low-fidelity wireframing shapes for classic iOS screen flows. | 1.0 | <nobr>2016-05-26</nobr> | Evolus Pencil Team<br>`GPL` | [Download ZIP](http://evoluspencil.googlecode.com/files/iOS-Wireframe_v2.zip) |
| **Dojo Widgets**<br>`calle.bokedal.dojo.Widgets` | UI component library based on the Dojo Toolkit framework. | 1.0 | <nobr>2016-05-26</nobr> | Calle Bokedal<br>`MIT` | [Download ZIP](http://evoluspencil.googlecode.com/files/Dojo.GUI_v6.zip) |
| **Bootstrap**<br>`nz.nwatson.Bootstrap` | High-fidelity components based on early Bootstrap 3 UI styles. | 1.1.0 | <nobr>2016-05-26</nobr> | Nathaniel Watson<br>`MIT` | [Download ZIP](https://github.com/nathanielw/Bootstrap-Pencil-Stencils/releases/download/v1.1.0/bootstrap-pencil-stencils-v1.1.0.zip) |
| **Android Lollipop**<br>`nz.nwatson.AndroidLollipop` | Android 5.0 Lollipop UI components following early Material Design. | 1.1.0 | <nobr>2016-05-26</nobr> | Nathaniel Watson<br>`MIT` | [Download ZIP](https://github.com/nathanielw/Android-Lollipop-Pencil-Stencils/releases/download/v1.1.0/android-lollipop-pencil-stencils-v1.1.0.zip) |
| **Material Icons**<br>`nz.nwatson.MaterialIcons` | Over 800 original Google Material Design icons packaged as stencils. | 2.0.0 | <nobr>2016-05-26</nobr> | Nathaniel Watson<br>`MIT` | [Download ZIP](https://github.com/nathanielw/Material-Icons-for-Pencil/releases/download/v2.0.0/material-icons-for-pencil-v2.0.0.zip) |
| **Twemoji**<br>`nz.nwatson.Twemoji` | Twitter open-source emoji set packaged for drag-and-drop wireframing. | 1.1.0 | <nobr>2016-05-26</nobr> | Nathaniel Watson<br>`MIT` | [Download ZIP](https://github.com/nathanielw/Twemoji-for-Pencil/releases/download/v1.1.0/twemoji-for-pencil-v1.1.0.zip) |
| **Bootstrap Glyphicons**<br>`co.uk.cfisk.BootstrapGlyphicons` | Classic Bootstrap Glyphicons icon font elements as stencil shapes. | 0.1 | <nobr>2016-05-26</nobr> | Craig Fisk<br>`MIT` | [Download ZIP](https://github.com/Craig-Fisk/BootstrapGlyph-Pencil-Stencil/archive/0.1.zip) |

---

## License

The repository structure and metadata files are licensed under the [MIT License](LICENSE). Individual stencil collections and resource bundles retain their respective licenses as specified in their manifest entries (MIT, OFL-1.1, or GPL).
