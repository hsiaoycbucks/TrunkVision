# 林業數位孿生展示系統 (Forest Digital Twin)

## 📌 專案簡介

本專案是一個基於 **Web-AR** 技術的林業數位孿生（Digital Twin）展示系統。

它實現了從 **林業調查數據（CSV）** 到 **自動化立體建模（Blender Python）**，最後封裝為 **跨平台網頁互動展示（Google <model-viewer>）** 的完整工作流。

使用者無需下載任何 App，即可在 PC 或智慧型手機上流暢閱覽真實比例的立體樹幹模型。極致的呈現功能是，透過手機的 AR 模式，可以將這片數據森林直接「種」在現實世界的環境中，實現沉浸式的數據視覺化。

## 🚀 核心功能

* **自動化幾何生成：** 利用 Blender Python 腳本，根據 CSV 數據（座標、直徑）精確生成每一棵樹的立體幾何模型。
* **科學數據綁定：** 每棵樹都精確計算並綁定了標準胸徑（DBH at Z=1.3m）與分段圓台材積數據。
* **互動式 Hotspots (熱點)：** 網頁端設有互動熱點，點擊樹木即可從 JSON 資料庫中即時調用並顯示樹木編號、胸徑、材積與樹高。
* **一鍵 Web-AR 投影：** 支援 Android (ARCore) 與 iOS (ARKit) 原生 AR 模式，實現虛實整合的場景展示。
* **零伺服器部署：** 完全相容 GitHub Pages (HTTPS)，具備極佳的分享與存取便利性。

---

## 📱 立即體驗 (Live Demo)

此專案已發佈至 GitHub Pages。您可以使用智慧型手機掃描下方 QR Code 進行體驗：

<div align="center">
  <img src="https://hsiaoycbucks.github.io/TrunkVision/TrunkVisionQRcode.png" alt="Scan QR Code to view Forest Digital Twin" width="200" />
  <br>
  <a href="https://hsiaoycbucks.github.io/TrunkVision/">👉 點擊此處直接開啟網頁</a>
</div>

---

## 📸 AR 掃碼操作說明 (How to Use AR)

為了在手機上獲得最佳的 AR 體驗，請參考以下步驟：

| 步驟 | 圖示 | 操作說明 |
| :--- | :---: | :--- |
| **1. 掃描與開啟** | <img src="https://hsiaoycbucks.github.io/TrunkVision/QRcodeScanner.png" alt="Scan QR Code to view Forest Digital Twin" width="200" /> | 使用智慧型手機相機或 LINE 掃描上方的 QR Code，在瀏覽器（建議 Chrome 或 Safari）中開啟網頁。 |
| **2. 載入模型** | <img src="https://hsiaoycbucks.github.io/TrunkVision/MobileView.png" alt="Scan QR Code to view Forest Digital Twin" width="200" /> | 網頁開啟後，請等待立體森林模型載入完畢。您可以用手指旋轉、縮放模型進行預覽。 |
| **3. 啟動 AR** |  | 點擊螢幕右下角的 **「進入 AR 模式」的按鈕**（或是「立體方塊 (3D Cube)」圖示）。 |
| **4. 環境掃描** |  | 相機開啟後，請將鏡頭對準一片空曠的**地板或桌面**，慢慢左右移動手機，直到畫面上出現網格或圓點，代表系統已成功識別平面。 |
| **5. 投影模型** | <img src="https://hsiaoycbucks.github.io/TrunkVision/MobileARView.png" alt="Scan QR Code to view Forest Digital Twin" width="200" /> | 點擊網格區域，立體數據森林就會以 1:1 或自動比例投影在現實世界中。 |
| **6. 數據互動** |  | 您可以手持手機在投影出的森林中走動。點擊樹木上的**黃色熱點 (Hotspot)**，底部會滑出該樹木的詳細胸徑、材積與樹高數據卡片。 |

> **💡 技術提醒：**
> * 您的手機必須支援 **Google ARCore** (Android) 或 **Apple ARKit** (iOS)。
> * 請在光線充足、地板有紋理（非純白或純鏡面）的環境下進行 AR 投影，效果最佳。

---

## 🛠 技術堆疊

* **Modeling:** Blender 4.x (using Python API for auto-generation)
* **3D Format:** glTF 2.0 (GLB) with Draco compression
* **Web Renderer:** Google `<model-viewer>` (powered by Three.js)
* **Hosting:** GitHub Pages (HTTPS enabled)

---

## 📄 專案文檔與科學依據

* (待定)

## ⚖️ 授權條款 (License)

(待定)
