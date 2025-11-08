# 🚨 Siren Flash App – by eyupensrr

**Siren App** is a desktop siren simulator built with Python.  
It features realistic police/ambulance siren sounds, flashing light effects, mode switching, and customizable themes and languages — all packed into a fullscreen Tkinter interface.

---

## ✨ Features (v2.0)

- 🌐 **Multilingual interface:** English 🇺🇸 & Turkish 🇹🇷  
- 🎨 **Dynamic theme switching:** Instantly toggle between Light & Dark modes  
- 🔊 **Realistic sound system:** Three independent siren modes — **ARMAS**, **CSR**, and **ZER**  
- 📣 **Horn mode:** Press-and-hold horn playback that resumes previous siren when released  
- 🔁 **Extended siren:** One-shot “EL” siren playback for quick bursts  
- 💡 **Flashing light simulation:** Smooth alternating red/blue screen light animation  
- 🧩 **Automatic media folder detection:** Automatically finds or asks for the correct sound folder  
- ⚙️ **Persistent configuration:** Remembers language, theme, and media path in `config.txt`  
- 🧱 **Responsive fullscreen UI:** Adapts to any screen resolution  
- 💾 **Self-contained:** Works with only Python and pip installed — no external frameworks needed  
- 💬 **Live warnings:** Shows missing sound files or folder errors directly in the interface  
- 🔄 **Seamless restarts:** Theme switching reloads UI without restarting the app manually  
- 🧰 **Cross-platform ready:** Works on Windows and compatible with macOS/Linux *(remove ctypes console-hide line if needed)*

---

### 🧩 Technical Updates in Version 2.0

- Cleaner, safer **configuration management** (`load_config` and `save_config` rewritten)  
- More reliable **media folder handling** — fallback to local `/media` directory if not found  
- Improved **first-run setup screen** for theme/language selection  
- Smoother **flash effect cycle** and non-blocking animation  
- Simplified **main UI layout** with centered grid and better scaling  
- Better **error handling** for missing or invalid sound files  
- Still **hides console on Windows only** (safe with try/except)  
- Ready for **PyInstaller packaging** without extra modification

---

✅ *This feature list applies to version 2.0 of Siren Flash App.*  

---

## ⚙️ System Requirements

| Component | Requirement |
|------------|--------------|
| **Python** | 3.9 or newer |
| **Operating System** | Windows 10+ (Linux/macOS compatible with small edits) |
| **Libraries** | `tkinter`, `pygame` |
| **Audio Format** | `.ogg` (stored inside `/media` folder) |

---

## 🚀 Installation & Setup

### 1️⃣ Install Python 3.9 or higher
- Download from [python.org/downloads](https://www.python.org/downloads/)
- During installation, make sure to check **“Add Python to PATH”**.

---

### 2️⃣ Install dependencies
```bash
pip install pygame
```
*(Tkinter is included by default with most Python installations.)*

---

### 3️⃣ Get the project

You can **clone** the repository:
```bash
git clone https://github.com/eyupensrr/siren-flash-app.git
cd siren-flash-app
```

Or **download it directly as a ZIP file**:  
➡️ [Download from GitHub](https://github.com/eyupensrr/siren-flash-app/archive/refs/heads/main.zip)

Then extract it anywhere on your computer.

---

### 4️⃣ Folder structure
```
siren-flash-app/
│
├── siren_app_main.py
├── config.txt
└── media/
    ├── a_1.ogg
    ├── a_2.ogg
    ├── a_3.ogg
    ├── a_horn.ogg
    ├── c_1.ogg
    ├── z_1.ogg
    └── ... (other .ogg files)
```

---

### 5️⃣ Run the application
```bash
python siren_app_main.py
```

On the first launch, you’ll be prompted to:
- Choose a **language** (English or Turkish)
- Choose a **theme** (Light or Dark)
- Select your **media folder** (if not automatically detected)

All preferences are saved in `config.txt`.

---

## 🧩 Packaging (Optional)

If you’d like to make a standalone `.exe` file to share the app:

```bash
pip install pyinstaller
pyinstaller --onefile --noconsole --add-data "media;media" siren_app_main.py
```

Your standalone file will appear in the `dist/` folder.

---

## 🧰 Troubleshooting

| Problem | Possible Cause | Solution |
|----------|----------------|----------|
| App doesn’t open | Missing dependencies | Run `pip install pygame` |
| Media not found | Missing or wrong path | Select folder when prompted |
| No sound | Pygame or driver issue | Try reinstalling `pygame` or check sound drivers |
| Tkinter not found | Minimal Python install | Reinstall Python (full installer from python.org) |
| Console flash or instant exit | Non-Windows system | Comment out the `ctypes.windll` console-hide line |

---

## 🧠 Technical Details

- **GUI Framework:** Tkinter  
- **Audio Engine:** pygame.mixer  
- **Persistent Config:** `config.txt`  
- **Languages:** English, Turkish  
- **Themes:** Light / Dark  
- **Flash effect:** Implemented with `after()` for smooth, non-blocking loops  
- **Fullscreen:** Uses `root.attributes("-fullscreen", True)` (can be replaced with `root.state("zoomed")` for Linux)

---

## 🧱 Project Structure

```
siren_app_main.py      # Main application script
config.txt             # User settings (auto-created)
media/                 # Folder containing .ogg sound files
README.md              # Project documentation
```

---

## 📜 Credits & License

This project is developed and maintained by **eyupensrr**.  
You’re welcome to use, modify, and redistribute this project **for personal or educational purposes**.

> ⚠️ **If you use this code, or any part of it (including the media files or configuration system), please give proper credit.**  
> Example:  
> “Based on *Siren Flash App* by eyupensrr – [GitHub Repository](https://github.com/eyupensrr/siren-flash-app)”

---

## 🧩 Future Plans

- Add volume & brightness sliders  
- Add keybindings for quick siren control  
- Add on-screen flashing light animation  
- Cross-platform packaging for macOS & Linux  
- Optional night mode improvements

---

### 🖤 Made with Python and caffeine.
