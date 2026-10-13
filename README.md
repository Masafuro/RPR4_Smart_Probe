# RPR4 Smart Probe

> **The Programmable, Galvanically Isolated Smart RS-485 Probe & Protocol Sniffer**  
> Powered by Raspberry Pi RP2040 PIO. Tool-less Terminal & Smartphone WebSerial Ready.

[![Hardware License](https://img.shields.io/badge/Hardware-CERN--OHL--P--v2-blue.svg)](LICENSE.md)
[![Firmware License](https://img.shields.io/badge/Firmware-MIT-green.svg)](LICENSE.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/Masafuro/RPR4_Smart_Probe/issues)

---

## What is RPR4 Smart Probe?

**RPR4 Smart Probe** is an open-source, pocket-sized hardware debugger, protocol sniffer, and programmer designed for field engineers, makers, and embedded developers working with RS-485 networks.

Traditional USB-to-RS485 dongles are dumb bridges: they cannot detect non-standard timings, lack galvanic isolation (putting host laptops at risk), fail to generate LIN/DMX BREAK signals reliably, and require tiny screwdrivers in harsh environments.  
**RPR4 solves all of these problems in a slim pencil-sized stick for under $25.**

---

## Key Features

- **⚡ Full Galvanic Isolation**: Built-in isolated DC-DC power and transceiver circuitry. Electrically floats your PC, tablet, or smartphone to eliminate ground loops and protect against high-voltage surges in harsh field environments.
- **🚀 RP2040 PIO Power**: Hardware-level pulse generation and microsecond timing analysis. Effortlessly generates and captures non-standard signals (LIN BREAK, DMX BREAK, custom timing gaps) without host OS jitter.
- **📱 Smartphone PWA (WebSerial) Native**: Plug directly into an Android phone or PC via USB-C and open the browser. Zero driver installation, zero app store hurdles.
- **🛠️ Tool-Less Spring Clamp Terminal**: SMD push-in spring terminals (`HDGC4001SMD-S-2P`, 4mm pitch). One-push field wiring—no tiny screwdrivers required.
- **🔍 Multi-Protocol Sniffer & Analyzer**:
  - Auto-baudrate & parity detection
  - Modbus RTU packet inspection & CRC validator
  - DMX512 / RDM tester
  - **ADX CORE-A High-Speed OTW Flasher** (3-second over-the-wire sketch update)

---

## Hardware Specifications

| Item | Specification |
| :--- | :--- |
| **Main MCU** | Raspberry Pi RP2040 (Dual ARM Cortex-M0+ @ 133MHz) |
| **Transceiver** | Isolated RS-485 Transceiver with integrated isolated DC-DC power (rev1: `TDA51S485HC`) |
| **Host Interface** | USB 2.0 Type-C (WebSerial / WebUSB CDC-ACM) |
| **Field Terminal** | 2-pin SMD Push-in Spring Clamp (`A`, `B`) + Optional GND |
| **Form Factor** | Slim pencil stick (~16mm x 55mm) |
| **Estimated PCBA Cost** | ~$6.02 @ 150pcs (JLCPCB PCBA) |

---

## Repository Structure

```text
RPR4_Smart_Probe/
├── hardware/           # Hardware design & production files (EDA-agnostic)
│   ├── design/         # Source schematic/PCB design files & review notes
│   ├── manufacturing/  # Fab-ready files (Gerber, BOM, CPL) separated by revision
│   └── exports/        # Schematic PDFs, 3D models (STEP/STL) for easy viewing
├── firmware/           # RP2040 C-SDK & PIO state machine firmware
├── webapp/             # Smartphone & PC WebSerial PWA debug application
└── docs/               # Architecture guides, pinouts, and quickstart tutorials
```

---

## Supported Modes & Protocols

1. **Auto-Baud Sniffer**: Passively monitors differential voltage and calculates baudrate, parity, and stop bits.
2. **Modbus RTU Analyzer**: Real-time packet inspection, slave address filtering, function code decoding.
3. **DMX512 / Lighting Probe**: Accurate 88µs BREAK generation, packet timing jitter measurement.
4. **ADX Platform OTW Flasher**: Native programmer for [ADX CORE-A](https://github.com/Masafuro/ADX) industrial controllers.

---

## Relationship with ADX Project

RPR4 Smart Probe was originally conceived as the flagship field programmer for the [ADX (Advanced Devices eXtended)](https://github.com/Masafuro/ADX) ecosystem.  
While it acts as the primary OTW flasher for ADX CORE-A, it is completely independent and designed to be a universal utility for all RS-485 applications worldwide.

---

## License

- **Hardware**: [CERN-OHL-P-v2](LICENSE.md)
- **Firmware & Software**: [MIT](LICENSE.md)
- **Documentation**: [CC-BY-4.0](LICENSE.md)
