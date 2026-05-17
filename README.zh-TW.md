<p align="right">
  <a href="README.md">English</a> ·
  <a href="README.zh-CN.md">简体中文</a> ·
  <strong>繁體中文</strong> ·
  <a href="README.ko.md">한국어</a>
</p>

<p align="center">
  <img src="docs/images/Crazyracing_Kartrider_(logo).png" alt="跑跑卡丁車" width="360">
</p>

<h1 align="center">KartRider Tools</h1>

<p align="center">
  解包並轉換 <a href="https://zh.wikipedia.org/wiki/%E8%B7%91%E8%B7%91%E5%8D%A1%E4%B8%81%E8%BB%8A">跑跑卡丁車</a>（CrazyRacing KartRider）的遊戲資源，匯出為可直接用於生產的 USD 場景。
</p>

<p align="center">
  <a href="#功能特性"><strong>功能特性</strong></a> ·
  <a href="#下載"><strong>下載</strong></a> ·
  <a href="#cinema-4d-外掛"><strong>Cinema 4D 外掛</strong></a> ·
  <a href="#免責聲明"><strong>免責聲明</strong></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-Freeware-blue?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/format-USD-green?style=flat-square" alt="USD">
</p>

<p align="center">
  <img src="docs/images/banner.jpg" alt="KartRider 2005" width="720">
</p>

---

掃描並轉換跑跑卡丁車（CrazyRacing KartRider）的遊戲資源 —— 解包 `.rho` 歸檔、解析私有 `.1s` 二進位格式，輸出包含幾何體、材質、貼圖與動畫的完整 3D 場景。

## 功能特性

- **資源掃描與轉換** — 批次掃描 `.rho` 歸檔與 `.1s` 模型檔案，轉換為 USD
- **地圖** — 完整場景匯出，包括路面幾何、場景物件、天空盒、裝飾、物體動畫、UV/材質動畫與透明度
- **角色** — 含骨骼層級的蒙皮模型，支援按動作分別匯出動畫並自動匹配表情貼圖
- **賽車** — 完整模型層級，支援各部件動畫
- **動畫** — 支援所有動畫類型：物體變換、UV、材質、骨骼
- **直接可算圖** — 自動剔除碰撞體、觸發區等非視覺遊戲資料
- **多語言介面** — 支援英文、簡體中文、繁體中文和韓文；資源名稱（賽道、賽車、角色）以當前語言顯示

所有資源統一匯出為 USD —— 之後可在任意 DCC 工具或算圖管線中使用。

---

## 下載

請前往 [**Releases**](https://github.com/nixliuxin/KartRider-Tools/releases) 頁面下載最新版本。

發佈包內含：

| 檔案 | 說明 |
|------|-----|
| `KartRider-Tools.exe` | 主程式（GUI），雙擊執行 |
| `KartRiderTools for Cinema 4D/` | Cinema 4D 匯入外掛 |

無需安裝。下載解壓後直接執行。

---

## Cinema 4D 外掛

目前僅支援 **Cinema 4D 2026**。

### 安裝

1. 將 `KartRiderTools for Cinema 4D` 資料夾複製到你的 Cinema 4D `plugins` 目錄：
   ```
   C:\Users\<使用者名稱>\AppData\Roaming\Maxon\Maxon Cinema 4D 2026_<hash>\plugins\
   ```
2. 重新啟動 Cinema 4D
3. 外掛會出現在 **Extensions → KartRider Tools** 選單下

### 功能

- 同時支援標準算圖器與 Redshift 材質
- Diffuse（受光）/ Flat（無光）一鍵切換
- UV 動畫重建
- Alpha 通道與透明度處理
- 自動座標系轉換（Z-up → Y-up）
- 自動跳過碰撞體與非視覺元素

---

## 免責聲明

> **請注意**：本專案所有官方文件以英文版本為準。本繁體中文譯本僅供閱讀參考；如譯文與英文原版存在任何歧義，以 [README.md](README.md) 英文版為準。

本專案**僅用於教育、研究及個人非商業目的**。本軟體按「現狀」提供，不附帶任何明示或默示的擔保，包括但不限於適銷性、特定用途適用性以及不侵權的擔保。

**跑跑卡丁車 / CrazyRacing KartRider**、所有遊戲資源、美術素材及相關商標均歸 **NEXON Korea Corporation**、**Tiancity** 及/或其各自的被許可方與關聯方所有。本專案**與上述任何公司均無關聯、未獲其認可、亦未受其贊助**。

本工具**不包含、不打包、不散佈**任何受著作權保護的遊戲內容。它僅提供讀取與轉換檔案格式的手段，用於互通性目的。使用者須自行負責確保其使用行為符合所有適用法律、法規及遊戲服務條款。

在任何情況下，作者或貢獻者均不對因軟體本身或軟體之使用所引發的任何索賠、損害或其他責任承擔責任，無論是基於合約、侵權或其他法理。

如任何權利人認為本專案侵犯其智慧財產權，請透過 issue 聯絡我們，我們將儘快處理。

## 致謝

- [Kartrider-File-Reader](https://github.com/xpoi5010/Kartrider-File-Reader) 作者 xpoi5010 — `.rho` 歸檔解包
- [kartrider_model_1s_to_obj](https://github.com/VT-Tuzki/kartrider_model_1s_to_obj) 作者 VT-Tuzki — 早期 `.1s` 模型解析工作，啟發了二進位格式的研究
- LuoHui666 — 在地圖場景提取的關鍵問題上提供了寶貴討論

## 授權

Copyright © 2026 nixliuxin. All rights reserved.

本軟體免費提供，**僅限個人非商業用途**。禁止再散佈、逆向工程與反編譯。本軟體按「現狀」提供，不附帶任何形式的擔保。

---

<p align="center">
  <sub>桌布美術作品 © 2005 NEXON Corporation</sub>
</p>
