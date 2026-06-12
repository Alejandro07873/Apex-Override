# ⚡ Apex Override ⚡

**Apex Override** is a comprehensive, all-in-one desktop toolkit designed to make Unreal Engine modding fast, visual, and highly automated. 🛠️🎮

Whether you need to batch-package `.pak` files, inject textures directly into `.uasset` files without opening the editor, or auto-deploy your mods straight into your game directory, this tool handles the heavy lifting so you can focus entirely on creating. 🧠🔥

---

## 🖼️ Interface Preview

<p align="center">

<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152256" src="https://github.com/user-attachments/assets/faaf5a36-4b9f-48c5-871e-5eb7fb5c1e6b" />
<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152258" src="https://github.com/user-attachments/assets/4235150a-17b9-4572-a511-08c0dd659f29" />
<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152300" src="https://github.com/user-attachments/assets/ec700b81-6356-48aa-b14c-6bad6c961d09" />
<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152303" src="https://github.com/user-attachments/assets/580a0cf2-5492-4004-bea3-45ed61903312" />
<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152305" src="https://github.com/user-attachments/assets/4bb619cc-9c22-44b7-af22-dce872c12cac" />
<img width="1366" height="728" alt="Captura de pantalla 2026-06-12 152307" src="https://github.com/user-attachments/assets/12f533f1-049b-43bc-91f0-4ae1b1f0efcd" />


</p>


---

## ✨ Key Features

* 📦 **Smart Packaging:** Generate `.pak` files in single mode or batch-process multiple assets. Choose to pack everything into one unified mega-mod or split them into separate, isolated files automatically.
* 🎨 **Advanced Texture Engine:** Inject, export, and convert textures (`.dds`, `.png`, `.tga`) directly to and from `.uasset` files. Supports mipmap removal, uncompressed forcing, and batch processing without Unreal Editor.
* 🧹 **Auto-Cleanup Rules:** Define custom rules to automatically scrub useless or heavy files before packaging, saving hours of manual deletion.
* 🚀 **1-Click Deploy:** Automatically copy generated mods to your game's `~mods` folder and launch the game executable immediately after packing.
* 📊 **Directory Explorer & Analysis:** Visually compare your Source (Cooked) Unreal project with your Temp Mod folder to track file sizes, spot stray physics assets, and validate integrity.
* 🌍 **Accessible UI:** Fully bilingual (English & Spanish) with a sleek Dark/Light mode toggle.

---

## 🔬 Under the Hood (Technical Architecture)

Apex Override is built with software engineering best practices in mind, ensuring a scalable and highly performant experience: 🖥️💡

* 🧩 **Decoupled UI & Debouncing:** Built with PySide6, the visual construction (`UIManager`) is strictly decoupled from event logic. Text inputs utilize `QTimer` debouncing to prevent memory bottlenecks and crashes during rapid user input.
* ⚡ **Asynchronous Multithreading:** Heavy operations (UnrealPak execution, Texture processing) are offloaded to secondary `QThread` workers. The app parses `subprocess.Popen` standard output in real-time to update progress bars, delivering a 100% fluid, non-blocking UI—matching the standard of professional game engines.
* 💾 **Intelligent Memory Management:** Internal paths and file hierarchies are cached using dynamic dictionary pooling (`img_pool`, `uasset_pool`, `asignaciones`), drastically minimizing expensive disk I/O operations.
* ⚙️ **Regex-Powered Cleanup Engine:** A dynamic pre-packaging routine uses custom expressions (like `*PhysicsAsset*.*` or `*_Skeleton.*`) to sanitize the build environment, automating what is traditionally a tedious manual process.

---

## 🧭 Quick Start Guide

1. 🏁 Open **Apex Override**.
2. 📁 Head over to the **Settings (📁)** tab:
   * Set your *Projects Root Folder* (Where your Cooked UE data is stored).
   * Set your *Temp Export Folder* and game paths (`~mods` and `.exe`).
3. ⚙️ Go to the **Automation (⚙️)** or **Multi-Packaging (👥)** tab:
   * Select your active Unreal project from the dropdown.
4. 🗂️ Check the tree structure and select the folders/assets you want to pack.
5. 🧹 *(Optional)* Head to **Cleanup & Deploy (🧹)** to ensure your mod is free of unnecessary skeleton files and enable auto-launch.
6. ▶️ Press **Package Main Asset** or **Start Multi-Packaging**.
7. 🎉 The app will clean, pack, deploy the mod to your game, and launch it automatically!

---

## 🎯 Typical Workflows

* 🖌️ **The Texture Modder:** Use the **Texture Engine** tab to instantly inject a `.dds` into a character's `.uasset` without needing to re-cook the entire project in Unreal Editor.
* 📦 **The Batch Creator:** Working on 10 different character recolors? Use **Multi-Packaging -> SEPARATED mode** to spit out 10 individual `.pak` files in one click.
* 🏃‍♂️ **The Rapid Prototyper:** Turn on **Auto-Deploy** and **Auto-Start**. Hit pack, and watch your game launch automatically with the new mod already installed.

---

## ⚠️ Notes & Warnings

* 🚨 This tool performs direct operations on `.uasset` files and uses external packaging scripts (`UnrealPak.exe`). **Always keep backups of your original Cooked data.**
* 🛡️ If Windows Defender or your antivirus flags the executable, it is a **false positive**. This is a known behavior for Python-compiled executables (PyInstaller) that manage system files and subprocesses. The project is open-source and virus-free, but use it at your own discretion.
* 📂 Ensure your `UnrealPak` batch files are correctly placed inside the internal `pkgE` folder for the packager to function.

> *My goal is to contribute a powerful, optimized tool that makes working with Unreal Engine assets easier, faster, and much less repetitive for the modding community.* 🤝

---

## ❤️ Support & Donations

If this tool saves you hours of packaging and texture injection, consider supporting its development! ☕💸

👉 **PayPal:** [https://www.paypal.com/paypalme/Alejo07378](https://www.paypal.com/paypalme/Alejo07378)

Any support is greatly appreciated and helps keep the project alive and improving. 🙌

---

## 🛠️ Contributing

* 🐛 Bug reports & Pull Requests
* 💡 Feature ideas (especially for the Texture Engine)
* 🎨 Code improvements & UI/UX suggestions

All feedback is welcome! Feel free to open an issue to get started. 🚀

---
> Made with 💙 by Alejandro (Aweooppoe) 👨‍💻

