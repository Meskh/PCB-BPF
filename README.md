# Band-Pass Filter PCB Design

A KiCad-based PCB design and circuit implementation of a 2nd-order Sallen-Key Butterworth band-pass filter, developed as part of the Technical Design module at the University of Surrey.

---

## Table of Contents

- [Overview](#overview)  
- [Features](#features)  
- [Project Structure](#project-structure)  
- [Circuit Design](#circuit-design)  
- [PCB Layout](#pcb-layout)  
- [3D Model & Enclosure](#3d-model--enclosure)  
- [Getting Started](#getting-started)  
- [Images to Include](#images-to-include)  
- [Technologies](#technologies)  
- [License](#license)  

---

## Overview

This project implements a band-pass filter with cutoff frequencies of 200 Hz and 4 300 Hz, suitable for audio and telecommunication applications. The design combines:

- A 2nd-order Sallen-Key low-pass stage  
- A 2nd-order Sallen-Key high-pass stage  
- Centre-tap virtual ground generation  
- PCB layout optimized for JLCPCB manufacturing  
- 3D-printable enclosure design  

---

## Features

- **Accurate Butterworth response** with flat passband and 40 dB/decade roll-off  
- **SMD components** for compact footprint and low parasitics  
- **Centre-tap virtual ground** using an op-amp buffer  
- **Full KiCad project** with schematic, PCB, and 3D model  
- **Enclosure design** for 3D printing in PETG
- Simulation testing and design details available in the ![report](https://github.com/Meskh/PCB-BPF/blob/main/report.pdf)   

---

## Circuit Design

1. **Conceptual diagram** shows block stages: LPF → buffer → HPF → buffer.  
   <figure>
      <img src="./Pictures/Chart.png" width="70%" alt="Conceptual Diagram Preview" />
      <figcaption>Conceptual block diagram overview</figcaption>
    </figure>  
2. **Stage schematics** for 2nd-order Sallen-Key LPF and HPF.  
3. **Centre-tap circuit** using a voltage divider and op-amp in follower mode.  
4. **Full BPF schematic** combining all stages with quad-op-amp and virtual ground.
   <figure>
      <img src="./Pictures/CircuitSchematic.png" width="70%" alt="Conceptual Diagram Preview" />
      <figcaption>Conceptual block diagram overview</figcaption>
    </figure>  

## PCB Layout

- Two-layer FR-4 board (29 × 20 mm, 1.6 mm thick)  
- SMD 0603 resistors and capacitors  
- JST EH connector for DC power  
- SMA edge-mount connectors for input/output  
- Full copper ground pours front and back  
- Four mounting holes for enclosure attachment

## 3D Model & Enclosure

- **PCB 3D model** exported from KiCad for visual verification  
- **Enclosure** designed in CAD (PETG, 3D print) with cutouts for SMA/DC connectors  
- **Barrel nut & bolt spacers** for secure PCB mounting

## Getting Started

1. Clone the repository:
    
        git clone https://github.com/<your-username>/BandPassFilter.git
        cd BandPassFilter

2. Open schematics in KiCad (v6 or later):
    - schematics/conceptual_circuit.kicad_sch  
    - schematics/full_filter.kicad_sch  

3. Inspect PCB layout:
    - pcb/bandpass.kicad_pcb  

4. View the 3D model in KiCad’s 3D viewer.  
5. Slice the enclosure STL files with your preferred slicer for PETG printing.

## Images to Include

Place these exported images in the `images/` folder and reference them in this README:

- **Conceptual circuit diagram** (conceptual_diagram.png)  
- **Stage schematics** (stage_schematics.png) showing LPF and HPF  
- **Centre-tap circuit** (centre_tap.png)  
- **Full BPF schematic** (full_filter_schematic.png)  
- **LPF/HPF/BPF simulation plots** (lpf_response.png, etc.)  
- **PCB front & back copper layers** (bandpass_front_copper.png, bandpass_back_copper.png)  
- **PCB 3D render** (bandpass_3d_model.png)  
- **Enclosure 3D render** (enclosure_3d_render.png)  
- **Op-amp pinout diagram** (opamp_pinout.png)

## Technologies

- **KiCad v6** for schematic capture and PCB layout  
- **Python/Ngspice** (optional) for circuit simulations  
- **FreeCAD or Shapr3D** for enclosure modeling  
- **PETG** filament for 3D printing

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
