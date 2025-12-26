curl -s https://api.github.com/repos/eyupensrr/siren-flash-app/releases | egrep 'download_count'  | cut '-d:' -f 2 | sed 's/,/+/' | xargs echo | xargs -I N echo N 0  | bc

* * *

🚨 Siren Flash App v3.0
=======================

**Advanced Police/EMS Siren & Flash Controller**  
Developed by **eyupensrr**

* * *

🌟 Overview
-----------

Siren Flash App is a powerful and customizable siren controller designed for roleplay, simulation setups, and emergency signaling demonstrations.  
Version **3.0** introduces:

*   Fullscreen icon support (Light & Dark)
*   Improved configuration system
*   Keyboard shortcuts
*   Theme switching
*   Flashing light effects
*   Automatic media folder detection
*   Cleaner UI & optimized system

* * *

✨ Features
----------

### 🎵 Sound System

*   3 Sound Modes: **ARMAS**, **CSR**, **ZER**
*   Siren types:
    *   🔊 Siren 1
    *   🔊 Siren 2
    *   🔊 Siren 3 (with switch mode)
    *   📢 Horn (press & hold)
    *   ➕ Extended Siren
*   Instant stop button
*   Automatic mode-based sound switching
*   Missing media detection

### 💡 Flash System

*   Left/Right alternating flash
*   Adjustable via shortcut key
*   Uses large background frames for realistic effect

### 🎨 Theme System

*   **Light** and **Dark** theme
*   Live switching without restarting
*   Fully applied to all UI components

### 🔧 First-Run Setup

*   Language selection
*   Theme selection
*   Media folder selection
*   Config saved automatically to `config.txt`

* * *

⌨️ Keyboard Shortcuts
---------------------

| Key | Function |
| --- | --- |
| **Q** | ARMAS Mode |
| **W** | CSR Mode |
| **E** | ZER Mode |
| **1** | Siren 1 |
| **2** | Siren 2 |
| **3** | Siren 3 |
| **H** | Horn (hold) |
| **V** | Switch Mode |
| **S** | Stop All Sounds |
| **L** | Flash Toggle |
| **I** | Extended Siren |
| **T** | Toggle Theme |
| **F11** | Fullscreen Toggle |
| **ESC** | Exit Fullscreen |

* * *

### IMPORTANT NOTE

If you download the .exe file, you don't need to download or install anything more. Just run the file.

* * *

📁 Media Folder Requirements
----------------------------

Your `media/` directory **must contain** the following files:

### 🔊 Siren Files

```
a_1.ogg
a_2.ogg
a_3.ogg
a_4.ogg
a_el.ogg
a_horn.ogg
c_1.ogg
c_2.ogg
c_3.ogg
c_4.ogg
c_el.ogg
c_horn.ogg
z_1.ogg
z_2.ogg
z_3.ogg
z_4.ogg
z_el.ogg
z_horn.ogg
```

### 🖼️ Fullscreen Icons

```
dark_fsc.png
light_fsc.png
```

* * *

🚀 Installation
---------------

### 🔧 Requirements

*   Python **3.10+**
*   Modules:
    *   `pygame`
    *   `tkinter` (comes with Python)
    *   `Pillow` (optional, for PNG icons)

### 💾 Install dependencies

```
pip install pygame pillow
```

### ▶️ Run the app

```
python siren_app_main_v3.0.py
```
or simply double click the file!

* * *

## 📜 Credits & License

This project is developed and maintained by **eyupensrr**.  
You’re welcome to use, modify, and redistribute this project **for personal or educational purposes**.

> ⚠️ **If you use this code, or any part of it (including the media files or configuration system), please give proper credit.**  
> Example:  
> “Based on *Siren Flash App* by eyupensrr – [GitHub Repository](https://github.com/eyupensrr/siren-flash-app)”


---

### 🖤 Made with Python and caffeine.
