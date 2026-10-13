# RPR4 Smart Probe Licensing Policy

The RPR4 Smart Probe Project uses a multi-licensing model to provide the most suitable open-source terms for each component of the project:

| Component | Scope | License | SPDX Identifier |
| :--- | :--- | :--- | :--- |
| **Documentation** | Specifications, manuals, guides, schematics diagrams in docs | **CC BY 4.0** | `CC-BY-4.0` |
| **Hardware** | Schematics, PCB layouts, Gerber, BOM, CPL, 3D models | **CERN-OHL-P-v2** | `CERN-OHL-P-2.0` |
| **Firmware & Software** | RP2040 firmware, PIO programs, WebSerial PWA, CLI scripts | **MIT License** | `MIT` |

---

## 1. Documentation License (CC BY 4.0)

All documentation, architecture guides, illustrations, and explanatory text within the `docs/` and `hardware/` directories are licensed under the **Creative Commons Attribution 4.0 International License**.

* You are free to share (copy and redistribute) and adapt (remix, transform, and build upon) the material for any purpose, including commercial use.
* **Attribution Requirement:** You must give appropriate credit to the **RPR4 Smart Probe Project Contributors**, provide a link to the license, and indicate if changes were made.

---

## 2. Hardware License (CERN-OHL-P-v2)

All hardware design files, schematic files, PCB layout files, manufacturing packages (Gerber, drill files), Bill of Materials (BOM), and mechanical CAD files located in the `hardware/` directory are licensed under the **CERN Open Hardware Licence Version 2 – Permissive (CERN-OHL-P-2.0)**.

* You may manufacture, distribute, and sell physical products based on these designs.
* You may modify the design files without being required to release your modifications under the same license (permissive nature).
* **Attribution & Notice:** You must retain copyright notices and license headers on all distributed design files.

---

## 3. Firmware & Software License (MIT License)

All source code, drivers, PIO programs, web applications, and utility scripts located in `firmware/` and `webapp/` are licensed under the **MIT License**.

```text
Copyright (c) 2026 RPR4 Smart Probe Project Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
