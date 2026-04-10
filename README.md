Ender 3 Pro — Full Rebuild & Klipper Upgrade
A long-term project to push an Ender 3 Pro beyond stock performance through iterative hardware upgrades and firmware customization. The printer was completely disassembled, upgraded with modern components, and migrated from stock Marlin to Klipper running on a Raspberry Pi.

Hardware Upgrades

Mainboard

BTT SKR Mini E3 V3 — replaced the stock Creality board for silent TMC2209 stepper drivers, better thermal management, and native Klipper compatibility

Auto Bed Leveling

BLTouch — installed for automatic mesh bed leveling; eliminates manual tramming and compensates for bed warping across the entire surface

Mechanical

Upgraded bed springs — replaced stock springs with stronger yellow springs for more consistent bed tension and reduced drift during printing

Single-Board Computer

Raspberry Pi — runs Klipper firmware + Moonraker API + Mainsail web interface for remote monitoring and control

Software & Firmware

Klipper — replaced Marlin for faster print speeds, input shaping support, and real-time tuning via web interface
Mainsail — browser-based UI for print management, monitoring, and configuration
Moonraker — API layer connecting Klipper to Mainsail
Cura — slicer with custom profiles tuned for this printer's upgraded capabilities

Tuning & Calibration

PID tuning for hotend and heated bed temperature stability
Input shaping / resonance compensation to eliminate ringing and ghosting artifacts
BLTouch mesh bed leveling with 5×5 probe grid
Pressure advance calibration for cleaner corners and better extrusion
G-code start/end macros optimized for fast homing and clean prints

What's in This Repo

printer.cfg — full Klipper configuration with all tuned parameters
mainsail.cfg — Mainsail macros (PAUSE, RESUME, CANCEL_PRINT)
cura-profiles/ — material profiles for PLA, PETG
mods/ — notes on hardware modifications and installation steps

What I Learned

How FDM printers work at a mechanical and firmware level
PID control applied to real-world thermal systems
Klipper architecture: host process on Raspberry Pi + microcontroller firmware on SKR board
Linux basics: SSH, systemd services, file editing on Raspberry Pi
Closed-loop calibration and resonance tuning with accelerometer data
Diagnosing and fixing common print quality issues

Timeline
March 2021 – August 2023 | Independent Project
