# Ender 3 Pro - Full Rebuild & Klipper Upgrade

![Klipper](https://img.shields.io/badge/Firmware-Klipper-orange?style=flat-square&logo=klipper)
![Mainsail](https://img.shields.io/badge/UI-Mainsail-blue?style=flat-square)
![Moonraker](https://img.shields.io/badge/API-Moonraker-blueviolet?style=flat-square)
![Cura](https://img.shields.io/badge/Slicer-Cura-00adef?style=flat-square)
![Marlin](https://img.shields.io/badge/Was-Marlin-green?style=flat-square)

![BTT SKR Mini E3](https://img.shields.io/badge/Board-BTT_SKR_Mini_E3_V3-red?style=flat-square)
![BLTouch](https://img.shields.io/badge/Leveling-BLTouch-success?style=flat-square)
![Raspberry Pi](https://img.shields.io/badge/SBC-Raspberry_Pi-c51a4a?style=flat-square&logo=raspberrypi)
![Springs](https://img.shields.io/badge/Springs-Upgraded_Yellow-yellow?style=flat-square)
![TMC2209](https://img.shields.io/badge/Drivers-TMC2209_Silent-lightgrey?style=flat-square)

A long-term project to push an Ender 3 Pro beyond stock performance through iterative hardware upgrades and firmware customization. Completely disassembled, upgraded with modern components, and migrated from stock Marlin to Klipper running on a Raspberry Pi.

---

## ⚙️ Hardware Upgrades

### 🖥️ Mainboard
- **BTT SKR Mini E3 V3** - replaced the stock Creality board for silent TMC2209 stepper drivers, better thermal management, and native Klipper compatibility

### 📍 Auto Bed Leveling
- **BLTouch** - installed for automatic mesh bed leveling; eliminates manual tramming and compensates for bed warping across the entire surface

### 🔩 Mechanical
- **Upgraded bed springs** - replaced stock springs with stronger yellow springs for more consistent bed tension and reduced drift during printing

### 🍓 Single-Board Computer
- **Raspberry Pi** - runs Klipper firmware + Moonraker API + Mainsail web interface for remote monitoring and control

---

## 💻 Software & Firmware

| Component | Role |
|-----------|------|
| **Klipper** | Firmware — runs split between Raspberry Pi (host) and SKR board (MCU) |
| **Moonraker** | API layer connecting Klipper to the web interface |
| **Mainsail** | Browser-based UI for print management, monitoring, and config |
| **Cura** | Slicer with custom profiles tuned for this printer's capabilities |

---

## 📊 Stock vs Upgraded

| Feature | Stock | Upgraded |
|---------|-------|----------|
| Mainboard | Creality 4.2.2 | BTT SKR Mini E3 V3 |
| Stepper drivers | A4988 (noisy) | TMC2209 (silent) |
| Bed leveling | Manual (4 screws) | BLTouch auto mesh 5×5 |
| Bed springs | Soft stock springs | Strong yellow springs |
| Firmware | Marlin (stock) | Klipper on Raspberry Pi |
| Interface | LCD screen only | Mainsail web UI + mobile |
| Input shaping | ❌ | ✅ resonance compensation |
| Pressure advance | ❌ | ✅ calibrated per material |

---

## 🎯 Tuning & Calibration

- 🌡️ PID tuning for hotend and heated bed temperature stability
- 📳 Input shaping / resonance compensation to eliminate ringing and ghosting
- 📐 BLTouch mesh bed leveling with 5×5 probe grid
- 🔁 Pressure advance calibration for cleaner corners
- 📝 G-code start/end macros optimized for fast homing and clean prints

---

## 📁 What's in This Repo

- `printer.cfg` - full Klipper configuration with all tuned parameters
- `mainsail.cfg` - Mainsail macros (PAUSE, RESUME, CANCEL_PRINT)
- `cura-profiles/` - material profiles for PLA, PETG
- `mods/` - notes on hardware modifications and installation steps

---

## 🧠 What I Learned

- How FDM printers work at a mechanical and firmware level
- PID control applied to real-world thermal systems
- Klipper architecture: host process on Raspberry Pi + MCU firmware on SKR board
- Linux basics: SSH, systemd services, file editing on Raspberry Pi
- Closed-loop calibration and resonance tuning with accelerometer data
- Diagnosing and fixing common print quality issues

---

## 📅 Timeline

**March 2021 - August 2023** | Independent Project
