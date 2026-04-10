<p align="center">
  <img src="docs/images/Crazyracing_Kartrider_(logo).png" alt="CrazyRacing KartRider" width="360">
</p>

<h1 align="center">KartRider-Tools</h1>

<p align="center">
  Extract and convert <a href="https://en.wikipedia.org/wiki/KartRider">KartRider</a> game assets into production-ready USD scenes.
</p>

<p align="center">
  <a href="#features"><strong>Features</strong></a> ·
  <a href="#installation"><strong>Installation</strong></a> ·
  <a href="#usage"><strong>Usage</strong></a> ·
  <a href="#dcc-plugins"><strong>DCC Plugins</strong></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/python-3.10+-yellow?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/format-USD-green?style=flat-square" alt="USD">
</p>

<p align="center">
  <img src="docs/images/banner.jpg" alt="KartRider 2005" width="720">
</p>

---

Unpack `.rho` game archives, parse the proprietary `.1s` binary format, and produce complete 3D scenes — maps, karts, and characters — with geometry, materials, textures, and animations all in one file.

## Features

### Maps

- Complete scene export: road geometry, scenery, sky dome, decorations
- Object animations with loop support
- UV / material animations
- Transparency and alpha channel support
- Automatic cleanup of non-visual game data (collision volumes, trigger zones, gameplay mechanics) — output is render-ready

### Characters

- Skinned meshes with bone hierarchy and dual-weight skinning
- Automatic face model alignment — face geometry is correctly positioned without manual adjustment

### Karts

- Full model hierarchy with per-part animation support

### Output

All assets export to USD with complete scene information — geometry, materials, textures, animations, and hierarchy are fully preserved. From USD you can bring your assets into any DCC tool or rendering pipeline.

### GUI & CLI

A desktop GUI application for batch extraction and conversion with asset filtering, progress tracking, and stop control. A CLI is also available for scripting and automation.

---

## DCC Plugins

- **Cinema 4D** — importer plugin with:
  - Standard renderer material support
  - Redshift renderer material support
  - UV animation reconstruction
  - Alpha channel and transparency handling
- More DCC plugins planned

---

## Installation

```bash
pip install -e .
```

Pre-compiled `RhoLoader.exe` is included. To rebuild (requires .NET 8 SDK):

```bash
cd vendor/Kartrider-File-Reader
dotnet build -c Release
```

## Usage

### GUI

```bash
karttools-gui
```

### CLI

```bash
karttools map <map_dir> -f usda --c4d
karttools map <map_dir> --scale 1.0 --alpha-extract
karttools model <source_dir>
karttools anim  <source_dir> -a f01.1s
```

---

## Disclaimer

This project is intended **strictly for educational, research, and personal non-commercial purposes**. It is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement.

**KartRider**, all game assets, artwork, and related trademarks are the property of **NEXON Korea Corporation**, **Tiancity**, and/or their respective licensors and affiliates. This project is **not affiliated with, endorsed by, or sponsored by** any of these companies.

This tool **does not include, bundle, or distribute** any copyrighted game content. It only provides the means to read and convert file formats for interoperability purposes. Users are solely responsible for ensuring their use complies with all applicable laws, regulations, and the game's terms of service.

In no event shall the authors or contributors be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software.

If any rights holder believes this project infringes on their intellectual property, please open an issue and we will address it promptly.

## Acknowledgements

- [Kartrider-File-Reader](https://github.com/xpoi5010/Kartrider-File-Reader) by xpoi5010 — `.rho` archive unpacking, integrated as vendor code in this project
- [kartrider_model_1s_to_obj](https://github.com/VT-Tuzki/kartrider_model_1s_to_obj) by VT-Tuzki — early `.1s` model parsing work that inspired the binary format investigation
- LuoHui666 — discussions that helped solve a key challenge in map scene extraction

---

<p align="center">
  <sub>Wallpaper artwork © 2005 NEXON Corporation</sub>
</p>
