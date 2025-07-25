# Boost-Converter/12VDCIN - 24VDCOUT #
# ⚡ Boost Converter Design – Simulation + Layout + DFMEA

This project demonstrates a **DC-DC Boost Converter** design using both simulation and PCB layout tools. It highlights the effect of **EMI-conscious design** by comparing circuits *with* and *without ferrite bead*, and includes DFMEA analysis for real-world reliability.

---

## 🔁 Project Structure

```
Boost_Converter/
├── LTspice/
│   ├── Without_Ferrite_Bead/
│   │   ├── boost_no_fb.asc
│   │   └── waveform_no_fb.png
│   └── With_Ferrite_Bead/
│       ├── boost_with_fb.asc
│       └── waveform_with_fb.png
│
├── KiCad/
│   ├── layout.png
│   ├── Gerber/
│   └── BOM.xlsx
│
├── DFMEA/
│   └── dfmea_summary.png
```

---

## 🔧 Design Summary

- **Input Voltage:** 12V
- **Output Voltage Target:** ~24V
- **Control Type:** Open-loop PWM
- **Switching Element:** IRFZ44N NMOS
- **Diode:** 1N5819 Schottky
- **Inductor:** 220µH
- **Capacitors:** 220µF + 0.1µF (output filter)

---

## 🧪 Simulation (LTspice)

Two simulations were performed:
1. **Without Ferrite Bead**  
   - Shows higher ripple & EMI noise  
   - Output waveform: `waveform_no_fb.png`
2. **With Ferrite Bead**  
   - EMI noise significantly reduced  
   - Output waveform: `waveform_with_fb.png`

---

## 🛠️ PCB Design (KiCad)

- Designed only for **EMI-optimized version** (with ferrite bead)
- Includes:
  - `layout.png` (PCB layout screenshot)
  - `Gerber/` folder for fabrication
  - `BOM.xlsx` with all component specs

---

## 🔍 DFMEA (Design Failure Mode & Effects Analysis)

- Performed on EMI-optimized design
- Key risks analyzed: Overheating, Load drop, Component failure
- Output file: `dfmea_summary.png`

---

## ✅ Learning Outcomes

- LTspice simulation + waveform validation
- EMI-conscious circuit improvement
- PCB layout using KiCad
- DFMEA risk awareness
- Bill of Material (BOM) creation
- GitHub project documentation & structure

---

## 💻 Tools Used

- LTspice (Simulation)
- KiCad (Layout + Gerber + BOM)
- Excel / Visual for DFMEA
- GitHub for structure, versioning

---

## 📎 Screenshots Preview

| Without Ferrite Bead | With Ferrite Bead |
|----------------------|-------------------|
| ![](LTspice/Without_Ferrite_Bead/waveform_no_fb.png) | ![](LTspice/With_Ferrite_Bead/waveform_with_fb.png) |

---

#BoostConverter #LTspice #KiCad #PowerElectronics #DFMEA #PCBdesign
