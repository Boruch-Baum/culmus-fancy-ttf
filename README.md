# culmus-fancy-ttf

TrueType versions of specific Hebrew fonts from the '[Culmus Fancy](https://culmus.sourceforge.io/fancy/index.html)' project.

## Why does this repository exist?

While the core Culmus project distributes standard Hebrew fonts, several of the "Fancy" extension fonts (contributed by Maxim Iakovlev, Yoram Gnat, and others) are officially distributed in **OTF** (OpenType) or historical PostScript formats, scattered across different sub-archives.

This repository provides a clean, automated build that extracts these specific fonts and converts them into standard **TTF (TrueType)** format using `fontforge`. This is essential for environments, legacy software, or X11 configurations that require or perform better with TrueType versions.

* **Upstream Release Date:** 2022-10-23
* **Last Build & Sync Date:** 2026-05-28

---

## Included Fonts

This repository focuses strictly on providing TrueType (`.ttf`) versions for the following 9 fonts:

* **AnkaCLM-Bold.ttf**
* **ComixNo2CLM-Bold.ttf**
* **ComixNo2CLM-Medium.ttf**
* **DorianCLM-Book.ttf**
* **DorianCLM-BookItalic.ttf**
* **FarissolCLM-BoldItalic.ttf**
* **GanCLM-Bold.ttf**
* **GladiaCLM-Bold.ttf**
* **HillelCLM-Medium.ttf**
* **HorevCLM-Heavy.ttf**
* **JournalCLM-Light.ttf**
* **KtavYadCLM-BoldItalic.ttf**
* **KtavYadCLM-MediumItalic.ttf**
* **LulavCLM-Bold.ttf**
* **MakabiYG.ttf**
* **OzradCLM-Bold.ttf**
* **ShmulikCLM.ttf**
* **TrashimCLM-Bold.ttf**

---

## Packages & Downstream

* **Arch Linux (AUR):** This repository serves as the upstream source for the [`culmus-fancy-ttf`](https://aur.archlinux.org/packages/culmus-fancy-ttf) package.

Please open an issue if:
* This has been packaged for another distribution, so it can be linked here.
* The original upstream project officially adopts a unified TrueType distribution for these specific fonts.
* You encounter any rendering or hinting issues with the converted TTF files.

---

## Technical Details

The assets are synchronized with upstream using an automated build script. Non-TTF source assets are converted programmatically:
```bash
fontforge -lang=ff -c "Open(\$1); Generate(\$2);" input.otf output.ttf
```
