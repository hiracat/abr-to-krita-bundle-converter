# ABR to Krita Bundle Converter

The reason why this is forked is because the original crashes when dealing with 16 bit files. 
I got claude to fix it and plan on making further improvements, either by hand or with AI either assistance or primarily.
It works with them now. 
Some other things are still broken. Please open issues with brushes which dont behave the way you expect them to.
Thumbnails dont exist. .abr files dont include them, so the krita ends up with a white thumbnail.

Brush engines besides pixel are not supported.
Having brush fields vary with anything besides pressure doesnt work.
Custom curves for brush fields also doesnt work.




Convert Photoshop `.abr` brush files into Krita resource bundles (`.bundle`).
This does not need to be run as a krita plugin and can be easily run standalone. I forget how and am not putting directions. but directions do exist in the freyalupen original brush converter repo. 

## Installation

1. Copy the `abr_to_krita_bundle_converter/` folder and `abr_to_krita_bundle_converter.desktop` to your Krita Python plugins folder:
   - **Linux:** `~/.local/share/krita/pykrita/`
   - **Linux (Flatpak):** `~/.var/app/org.kde.krita/data/krita/pykrita/`
   - **macOS:** `~/Library/Application Support/krita/pykrita/`
   - **Windows:** `%APPDATA%\krita\pykrita\`
2. Restart Krita
3. Enable it in **Settings → Configure Krita → Python Plugin Manager → ABR to Krita Bundle Converter**

## Usage

1. Go to **Tools → Scripts → Convert ABR brushes to bundle...**
2. Select your `.abr` file
3. Click **Convert** — the `.bundle` is saved in the same folder as the `.abr` file
4. Import it in Krita via **Settings → Manage Resources → Import Bundle/Resource**

## Credits

Based on [procreate-to-krita-brush-converter](https://invent.kde.org/freyalupen/procreate-to-krita-brush-converter/) by **Freya Lupen** (GPL-3.0-or-later).

## License

GPL-3.0-or-later
Same as above, but also dumps any material data found into folders with the brushes' names in the folder /pathto/output/.
