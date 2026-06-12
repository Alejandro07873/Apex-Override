# **Auto Modder Studio Pro ⚙️**

**Auto Modder Studio Pro** is a comprehensive, all-in-one desktop toolkit designed to make Unreal Engine modding fast, visual, and highly automated. 

Whether you need to batch-package `.pak` files, inject textures directly into `.uasset` files without opening the editor, or auto-deploy your mods straight into your game, this tool handles the heavy lifting so you can focus on creating.

## 🖼️ Interface Preview

<p align="center">
  <img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152258" src="https://github.com/user-attachments/assets/2f1fc39f-8cd5-4572-b09d-d30c6fcd7205" />
<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152300" src="https://github.com/user-attachments/assets/f1fb37d6-cd0b-4043-9b4f-c0166ad6ea6f" />
<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152303" src="https://github.com/user-attachments/assets/131b4a50-e3fe-4cc3-abd4-7e5dffaeefa6" />
<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152305" src="https://github.com/user-attachments/assets/32b67f3f-86e5-4d88-8f94-8bd995d1fcb3" />
<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152307" src="https://github.com/user-attachments/assets/2f956b71-6271-4347-9df9-cc406ac6ec0d" />
<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152256" src="https://github.com/user-attachments/assets/1d78a860-825c-4709-a67f-f44dc889f17c" />

</p>

## ✨ Key Features

- 📦 **Smart Packaging:** Generate `.pak` files in single mode or batch-process multiple assets. Choose to pack everything into one unified mega-mod or split them into separate files automatically.
- 🎨 **Advanced Texture Engine:** Inject, export, and convert textures (`.dds`, `.png`, `.tga`) directly to and from `.uasset` files. Supports mipmap removal, uncompressed forcing, and batch processing.
- 🧹 **Auto-Cleanup Rules:** Define custom rules (e.g., `*PhysicsAsset*.*`, `*_Skeleton.*`) to automatically strip useless or heavy files before packaging, saving hours of manual deletion.
- 🚀 **1-Click Deploy:** Automatically copy generated mods to your game's `~mods` folder and launch the game executable immediately after packing.
- 📊 **Directory Explorer & Analysis:** Visually compare your Source (Cooked) Unreal project with your Temp Mod folder to track file sizes, spot physics assets, and validate integrity.
- 🌍 **Accessible UI:** Fully bilingual (English & Spanish) with a sleek Dark/Light mode toggle. Built with PySide6 and multithreading so the interface never freezes during heavy operations.

---

## 🧭 Quick Start Guide

- **1-** Open **Auto Modder Studio Pro**.
- **2-** Head over to the **Settings (📁)** tab:
  - Set your *Projects Root Folder* (Where your Cooked UE data is stored).
  - Set your *Temp Export Folder* and game paths (`~mods` and `.exe`).
- **3-** Go to the **Automation (⚙️)** or **Multi-Packaging (👥)** tab:
  - Select your active Unreal project from the dropdown.
- **4-** Check the tree structure and select the folders/assets you want to pack.
- **5-** *(Optional)* Head to **Cleanup & Deploy (🧹)** to ensure your mod is free of unnecessary skeleton files and enable auto-launch.
- **6-** Press **Package Main Asset** or **Start Multi-Packaging**.
- **7-** The app will clean, pack, copy the mod to your game, and launch it automatically!

---

## 🎯 Typical Workflows

- **The Texture Modder:** Use the **Texture Engine** tab to instantly inject a `.dds` into a character's `.uasset` without needing to re-cook the entire project in Unreal Editor.
- **The Batch Creator:** Working on 10 different character recolors? Use **Multi-Packaging -> SEPARATED mode** to spit out 10 individual `.pak` files in one click.
- **The Rapid Prototyper:** Turn on **Auto-Deploy** and **Auto-Start**. Hit pack, and watch your game launch automatically with the new mod already installed.

---

## ⚠ Notes & Warnings

- This tool performs direct operations on `.uasset` files and uses external packaging scripts (`UnrealPak.exe`). **Always keep backups of your original Cooked data.**
- If Windows Defender or your antivirus flags the executable, it is a **false positive**. This is common for Python-compiled executables (PyInstaller) that manage system files. The project is virus-free, but use it at your own discretion.
- Make sure your `UnrealPak` batch files are correctly placed inside the internal `pkgE` folder for the packager to work.

> My goal is to contribute a powerful tool that makes working with Unreal Engine assets easier, faster, and much less repetitive for the modding community.

---

## ❤️ Support & Donations

If this tool saves you hours of packaging and texture injection, consider supporting its development!

👉 **PayPal:** [https://www.paypal.com/paypalme/Alejo07378](https://www.paypal.com/paypalme/Alejo07378)

Any support is greatly appreciated and helps keep the project alive and improving.

---

## 🤝 Contributing

- Bug reports & Pull Requests
- Feature ideas (especially for the Texture Engine)
- Code improvements & UI/UX suggestions

All feedback is welcome! Feel free to open an issue to get started.

---
> Made with 💙 by Alejandro (Aweooppoe)
