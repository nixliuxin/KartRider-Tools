<p align="right">
  <a href="README.md">English</a> ·
  <strong>简体中文</strong> ·
  <a href="README.zh-TW.md">繁體中文</a> ·
  <a href="README.ko.md">한국어</a>
</p>

<p align="center">
  <img src="docs/images/Crazyracing_Kartrider_(logo).png" alt="跑跑卡丁车" width="360">
</p>

<h1 align="center">KartRider Tools</h1>

<p align="center">
  解包并转换 <a href="https://baike.baidu.com/item/%E8%B7%91%E8%B7%91%E5%8D%A1%E4%B8%81%E8%BD%A6">跑跑卡丁车</a>（CrazyRacing KartRider）的游戏资源，导出为可直接用于生产的 USD 场景。
</p>

<p align="center">
  <a href="#功能特性"><strong>功能特性</strong></a> ·
  <a href="#下载"><strong>下载</strong></a> ·
  <a href="#cinema-4d-插件"><strong>Cinema 4D 插件</strong></a> ·
  <a href="#免责声明"><strong>免责声明</strong></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-Freeware-blue?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/format-USD-green?style=flat-square" alt="USD">
</p>

<p align="center">
  <img src="docs/images/banner.jpg" alt="KartRider 2005" width="720">
</p>

---

扫描并转换跑跑卡丁车（CrazyRacing KartRider）的游戏资源 —— 解包 `.rho` 归档、解析私有 `.1s` 二进制格式，输出包含几何体、材质、贴图与动画的完整 3D 场景。

## 功能特性

- **资源扫描与转换** — 批量扫描 `.rho` 归档与 `.1s` 模型文件，转换为 USD
- **地图** — 完整场景导出，包括路面几何、场景物件、天空盒、装饰、物体动画、UV/材质动画与透明度
- **角色** — 含骨骼层级的蒙皮模型，支持按动作分别导出动画并自动匹配表情贴图
- **赛车** — 完整模型层级，支持各部件动画
- **动画** — 支持所有动画类型：物体变换、UV、材质、骨骼
- **直接可渲染** — 自动剔除碰撞体、触发区等非视觉游戏数据
- **多语言界面** — 支持英文、简体中文、繁体中文和韩文；资源名称（赛道、赛车、角色）以当前语言显示

所有资源统一导出为 USD —— 之后可在任意 DCC 工具或渲染管线中使用。

---

## 下载

请前往 [**Releases**](https://github.com/nixliuxin/KartRider-Tools/releases) 页面下载最新版本。

发布包内含：

| 文件 | 说明 |
|------|-----|
| `KartRider-Tools.exe` | 主程序（GUI），双击运行 |
| `KartRiderTools for Cinema 4D/` | Cinema 4D 导入插件 |

无需安装。下载解压后直接运行。

---

## Cinema 4D 插件

目前仅支持 **Cinema 4D 2026**。

### 安装

1. 将 `KartRiderTools for Cinema 4D` 文件夹复制到你的 Cinema 4D `plugins` 目录：
   ```
   C:\Users\<用户名>\AppData\Roaming\Maxon\Maxon Cinema 4D 2026_<hash>\plugins\
   ```
2. 重启 Cinema 4D
3. 插件会出现在 **Extensions → KartRider Tools** 菜单下

### 功能

- 同时支持标准渲染器与 Redshift 材质
- Diffuse（受光）/ Flat（无光）一键切换
- UV 动画重建
- Alpha 通道与透明度处理
- 自动坐标系转换（Z-up → Y-up）
- 自动跳过碰撞体与非视觉元素

---

## 免责声明

> **请注意**：本项目所有官方文档以英文版本为准。本中文译本仅供阅读参考；如译文与英文原版存在任何歧义，以 [README.md](README.md) 英文版为准。

本项目**仅用于教育、研究及个人非商业目的**。本软件按"现状"提供，不附带任何明示或默示的担保，包括但不限于适销性、特定用途适用性以及不侵权的担保。

**跑跑卡丁车 / CrazyRacing KartRider**、所有游戏资源、美术素材及相关商标均归 **NEXON 韩国公司**、**世纪天成（Tiancity）**及/或其各自的被许可方与关联方所有。本项目**与上述任何公司均无关联、未获其认可、亦未受其赞助**。

本工具**不包含、不打包、不分发**任何受版权保护的游戏内容。它仅提供读取与转换文件格式的手段，用于互操作目的。用户须自行负责确保其使用行为符合所有适用法律、法规及游戏服务条款。

在任何情况下，作者或贡献者均不对因软件本身或软件之使用所引发的任何索赔、损害或其他责任承担责任，无论是基于合同、侵权或其他法理。

如任何权利人认为本项目侵犯其知识产权，请通过 issue 联系我们，我们将尽快处理。

## 致谢

- [Kartrider-File-Reader](https://github.com/xpoi5010/Kartrider-File-Reader) 作者 xpoi5010 — `.rho` 归档解包
- [kartrider_model_1s_to_obj](https://github.com/VT-Tuzki/kartrider_model_1s_to_obj) 作者 VT-Tuzki — 早期 `.1s` 模型解析工作，启发了二进制格式的研究
- LuoHui666 — 在地图场景提取的关键问题上提供了宝贵讨论

## 许可

Copyright © 2026 nixliuxin. All rights reserved.

本软件免费提供，**仅限个人非商业用途**。禁止再分发、逆向工程与反编译。本软件按"现状"提供，不附带任何形式的担保。

---

<p align="center">
  <sub>壁纸 © 2005 NEXON Corporation</sub>
</p>
