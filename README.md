# 🚀 Boost Converter Design DC (12V to 24V)

This project implements a **DC-DC Boost Converter** that steps up **12V DC to ~24V DC**, designed using **LTspice** and **KiCad**, and validated through simulation and analysis. Two versions were tested:
- Without feedback loop
- With feedback loop and **ferrite bead** for EMI-conscious design

## 📂 Project Structure
├── DFMEA
│   ├── DFMEA_Boost_combined.xlsx
│   └── DFMEA_SCREENSHOT_BOOST.png
│
├── KICAD
│   ├── BOM_ALLIGNES_BOOST.xlsx
│   ├── CKT_DIAGRAM.png
│   ├── LAYOUT_VIEW.png
│   ├── PCB_3D_VIEW.png
│   ├── PCB_RARE_3D_VIEW.png
│   └── gerber_gbr_drl.rar
│
├── LTSPICE
│   ├── WITH_FB
│   │   ├── boost_with_fb.asc
│   │   ├── Boost_waveform_full.png
│   │   ├── .asc_screenshot_FB.png
│   │   └── Ripple_analysis_screenshot.png
│   │
│   └── Without_Ferrite_Bead
│       ├── boost_no_fb.asc
│       ├── boost_waveform_screenshot.png
│       ├── .asc_screenshot.png
│       └── Ripple_analysis_boost.png

---

## ⚙️ Specifications

- **Input Voltage:** 12V DC  
- **Output Voltage:** ~24V DC  
- **Switching Frequency:** ~1 kHz (open-loop)  
- **MOSFET Used:** IRFZ44N  
- **Diode:** 1N5819  
- **Ferrite Bead:** Added in feedback version to reduce EMI

> Note: In open-loop (no feedback) simulation, voltage overshoots beyond 24V due to lack of regulation. With feedback + ferrite bead, stable 24V output is maintained.

---

## 🔍 Ripple & Frequency Analysis

| Configuration         | Peak Voltage (V) | Valley Voltage (V) | Ripple (mV) | Frequency |
|----------------------|------------------|---------------------|-------------|-----------|
| Without Feedback      | 27.502           | 27.212              | 289.78 mV   | ~1.002 kHz |
| With Ferrite Bead FB  | 24.083           | 23.691              | 392.09 mV   | ~1.000 kHz |

---

## 🧪 EMI-Conscious Design Consideration

To improve EMI behavior:
- A **Ferrite Bead** is introduced in the feedback path.
- KiCad layout shows optimized routing and component placement for reduced noise.

---

## 📝 Tools Used

- **LTspice** – Simulation of Boost Converter circuit  
- **KiCad** – Schematic & PCB Design (with 3D views & Gerber files)  
- **Excel** – DFMEA, BOM  
- **GitHub** – Documentation, Project Archival  

---

## 📌 Key Learnings

- Open-loop converters may cause overvoltage due to lack of control  
- Feedback helps regulate output but can increase ripple slightly  
- EMI considerations are essential in power electronics design  
- DFMEA ensures structured risk evaluation at design stage  

---

## ✅ Outcome

A complete working simulation and PCB layout of a 12V to 24V Boost Converter with:
- Dual circuit validation
- EMI-conscious component selection
- Design risk mitigation (via DFMEA)
- Complete ripple & frequency analysis

---

## 🔗 Author

**Vishal Singh**  
Power Electronics | DFT | Hardware Design
https://www.linkedin.com/in/vishal-singh-542338161/
