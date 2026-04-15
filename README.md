<p align="center">
  <img src="docs/images/Crazyracing_Kartrider_(logo).png" alt="CrazyRacing KartRider" width="360">
</p>

<h1 align="center">KartRider Tools</h1>

<p align="center">
  Extract and convert <a href="https://en.wikipedia.org/wiki/KartRider">KartRider</a> game assets into production-ready USD scenes.
</p>

<p align="center">
  <a href="#features"><strong>Features</strong></a> ·
  <a href="#download"><strong>Download</strong></a> ·
  <a href="#cinema-4d-plugin"><strong>Cinema 4D Plugin</strong></a> ·
  <a href="#disclaimer"><strong>Disclaimer</strong></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-Freeware-blue?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/format-USD-green?style=flat-square" alt="USD">
</p>

<p align="center">
  <img src="docs/images/banner.jpg" alt="KartRider 2005" width="720">
</p>

---

Scan and convert CrazyRacing KartRider game assets — unpack `.rho` archives, parse the proprietary `.1s` binary format, and produce complete 3D scenes with geometry, materials, textures, and animations.

## Features

- **Asset scanning & conversion** — batch scan `.rho` archives and `.1s` model files, convert to USD
- **Maps** — full scene export including road geometry, scenery, sky dome, decorations, object animations, UV/material animations, and transparency
- **Characters** — skinned meshes with bone hierarchy, per-action animation export with automatic face texture matching
- **Karts** — full model hierarchy with per-part animation support
- **Animation** — all animation types supported: object transform, UV, material, skeletal
- **Render-ready output** — automatic cleanup of collision volumes, trigger zones, and other non-visual game data

All assets export to USD — from there you can bring them into any DCC tool or rendering pipeline.

---

## Download

Go to the [**Releases**](https://github.com/nixliuxin/KartRider-Tools/releases) page and download the latest version.

The release package contains:

| File | Description |
|------|-------------|
| `KartRider-Tools.exe` | GUI application — double-click to run |
| `KartRiderTools for Cinema 4D/` | Cinema 4D importer plugin |

No installation required. Just download and run.

---

## Cinema 4D Plugin

Currently supports **Cinema 4D 2026** only.

### Installation

1. Copy the `KartRiderTools for Cinema 4D` folder to your Cinema 4D `plugins` directory:
   ```
   C:\Users\<you>\AppData\Roaming\Maxon\Maxon Cinema 4D 2026_<hash>\plugins\
   ```
2. Restart Cinema 4D
3. The plugin appears under **Extensions → KartRider Tools**

### Features

- Standard and Redshift renderer material support
- Diffuse (lit) and Flat (unlit) shading modes with one-click swap
- UV animation reconstruction
- Alpha channel and transparency handling
- Automatic coordinate conversion (Z-up → Y-up)
- Auto-skip collision bodies and non-visual elements

---

## Disclaimer

This project is intended **strictly for educational, research, and personal non-commercial purposes**. It is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement.

**KartRider**, all game assets, artwork, and related trademarks are the property of **NEXON Korea Corporation**, **Tiancity**, and/or their respective licensors and affiliates. This project is **not affiliated with, endorsed by, or sponsored by** any of these companies.

This tool **does not include, bundle, or distribute** any copyrighted game content. It only provides the means to read and convert file formats for interoperability purposes. Users are solely responsible for ensuring their use complies with all applicable laws, regulations, and the game's terms of service.

In no event shall the authors or contributors be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software.

If any rights holder believes this project infringes on their intellectual property, please open an issue and we will address it promptly.

## Acknowledgements

- [Kartrider-File-Reader](https://github.com/xpoi5010/Kartrider-File-Reader) by xpoi5010 — `.rho` archive unpacking
- [kartrider_model_1s_to_obj](https://github.com/VT-Tuzki/kartrider_model_1s_to_obj) by VT-Tuzki — early `.1s` model parsing work that inspired the binary format investigation
- LuoHui666 — discussions that helped solve a key challenge in map scene extraction

## License

Copyright © 2026 nixliuxin. All rights reserved.

This software is provided free of charge for **personal and non-commercial use only**. Redistribution, reverse engineering, and decompilation are prohibited. This software is provided "as is", without warranty of any kind.

---

<p align="center">
  <sub>Wallpaper artwork © 2005 NEXON Corporation</sub>
</p>
