<p align="center">
  <img src="./assets/pcb-header.svg" width="100%" alt="SINA YEGANEH — SY-2026, an animated PCB with a chip carrying my name">
</p>

<p align="center">
  <b>SY-2026</b> · Embedded &amp; IoT-Security Engineer · <b>Rev E</b><br>
  <sub>PRELIMINARY DATASHEET — specifications subject to change without notice (this device is still learning)</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/STATUS-ACTIVE-64c93e?style=flat-square&labelColor=0b152c" alt="Status: active">
  <img src="https://img.shields.io/badge/PACKAGE-HUMAN-64c93e?style=flat-square&labelColor=0b152c" alt="Package: human">
  <img src="https://img.shields.io/badge/FAB-ISFAHAN,_IR-64c93e?style=flat-square&labelColor=0b152c" alt="Fab: Isfahan, Iran">
  <img src="https://img.shields.io/github/last-commit/sina-yeganeh/sina-yeganeh?style=flat-square&label=LAST%20FIRMWARE&color=64c93e&labelColor=0b152c" alt="Last update">
</p>

<p align="center"><i><b>Free Palestine! 🇵🇸</b></i></p>

<p align="center">
  <sub>
    <a href="#1-features">1 Features</a> ·
    <a href="#2-description">2 Description</a> ·
    <a href="#3-pin-configuration">3 Pins</a> ·
    <a href="#4-specifications">4 Specs</a> ·
    <a href="#5-applications">5 Applications</a> ·
    <a href="#6-device-support">6 Toolchain</a> ·
    <a href="#7-revision-history">7 Revisions</a> ·
    <a href="#8-ordering-information">8 Contact</a>
  </sub>
</p>

---

## 1 Features

- **Embedded systems** — microcontrollers, ESP32, firmware in C and MicroPython
- **PCB design** — from schematic capture to a routed board (Altium)
- **IoT security** — breaking and hardening connected devices, heading for bug bounty
- **Low-level programming** — registers over abstractions, close to the metal
- **Web toolchain** — Python, Flask, JavaScript and React for dashboards and tools
- **Linux native** — Debian, Kali, Parrot, Ubuntu
- Co-founder of **Madarafzar Hooshmand Isfahan** — IoT · embedded · PCB
- Member of the **IEEE Student Branch** at Isfahan University of Technology

## 2 Description

The **SY-2026** is an electrical engineering student at **Isfahan University of Technology (IUT)**
who designs boards, writes the firmware that runs on them, and then tries to break both.

It shipped as a web developer and has been migrating down the stack ever since: from browsers
to Linux, from Linux to microcontrollers, and from microcontrollers to the question every
hardware person eventually asks — *"okay, but how would I attack this?"*

Target spec by graduation: seriously good at **embedded security, IoT security and PCB design**.

## 3 Pin Configuration

<p align="center">
  <img src="./assets/pinout.svg" width="92%" alt="SY-2026 pinout, top view: inputs on the left, outputs on the right">
  <br><sub><i>Figure 3-1. SY-2026 pin configuration (top view)</i></sub>
</p>

<sub><i>Table 3-1. Pin functions</i></sub>

| Pin | Name | Type | Description |
|:---:|:---|:---:|:---|
| 1 | `VCC` | P | Caffeine supply |
| 2 | `CLK` | I | Curiosity, free-running |
| 3 | `RX` | I | Docs, datasheets, courses, CTF write-ups |
| 4 | `I2C` | I/O | Team bus — IEEE Student Branch @ IUT |
| 5 | `RST` | I | Sleep. Active low, rarely asserted |
| 6 | `GND` | P | Isfahan, Iran |
| 7 | `NC` | — | Reserved for rev F |
| 8 | `SEC_OUT` | O | IoT security research |
| 9 | `PCB_OUT` | O | Schematics → layouts → boards |
| 10 | `FW_OUT` | O | Firmware in C / MicroPython |
| 11 | `MAIL` | I/O | [sinayeganeh.dev@gmail.com](mailto:sinayeganeh.dev@gmail.com) |
| 12 | `GH` | I/O | [github.com/sina-yeganeh](https://github.com/sina-yeganeh) |

## 4 Specifications

### 4.1 Absolute Maximum Ratings

> Stresses beyond those listed may cause permanent damage to the device.

| Parameter | Min | Max | Unit |
|:---|:---:|:---:|:---:|
| Sleep | 4 | — | h / night |
| Concurrent side projects | — | 8 | projects |
| Open browser tabs | — | 147 | tabs |
| Deadline proximity before panic mode | 6 | — | h |
| Ambient temperature (Isfahan summer) | — | 42 | °C |

### 4.2 Recommended Operating Conditions

| Parameter | Typ |
|:---|:---|
| OS | Linux (Debian-based) |
| Editor | VS Code |
| Interface languages | Persian · English |
| Timezone | UTC+03:30 (Asia/Tehran) |

### 4.3 Electrical Characteristics

<sub><code>PRODUCTION</code> = shipped and stable · <code>ACTIVE</code> = in heavy use · <code>SAMPLING</code> = under evaluation in the lab · <code>PREVIEW</code> = on the roadmap</sub>

| Block | Parameters | Status |
|:---|:---|:---:|
| Embedded | C · MicroPython · ESP32 · sensors (I²C/SPI) | ![ACTIVE](https://img.shields.io/badge/-ACTIVE-64c93e?style=flat-square) |
| Hardware | PCB design · Altium · analog &amp; digital electronics | ![ACTIVE](https://img.shields.io/badge/-ACTIVE-64c93e?style=flat-square) |
| Security | IoT security · Linux pentesting · OSINT | ![SAMPLING](https://img.shields.io/badge/-SAMPLING-f2a541?style=flat-square) |
| Security | Bug bounty | ![PREVIEW](https://img.shields.io/badge/-PREVIEW-8b95ab?style=flat-square) |
| Web | Python · Flask · JavaScript · React · HTML/CSS | ![PRODUCTION](https://img.shields.io/badge/-PRODUCTION-4fa3ff?style=flat-square) |
| Systems | Bash · Linux · MySQL · Git | ![PRODUCTION](https://img.shields.io/badge/-PRODUCTION-4fa3ff?style=flat-square) |

### 4.4 Typical Characteristics

<p align="center">
  <img src="./assets/characteristics.svg" width="92%" alt="Chart: web skills plateau early, embedded/PCB and IoT security rise steeply in recent revisions">
  <br><sub><i>Figure 4-1. Proficiency vs. revision</i></sub>
</p>

## 5 Applications

### 5.1 Typical Application — VitalBand

A wearable vital-signs monitor for crisis and field environments: heart rate, SpO₂ and temperature.

```text
 ┌──────────┐   I²C   ┌───────────┐  Wi-Fi / BLE  ┌────────────┐
 │ MAX30102 │ ──────▶ │   ESP32   │ ────────────▶ │ dashboard  │
 │ PPG/SpO₂ │         │ DSP + FW  │               │  + alerts  │
 └──────────┘         └───────────┘               └────────────┘
```

<sub>The trace on the scope at the bottom of this page is its PPG channel.</sub>

### 5.2 Other Applications

| Application | Description | Status |
|:---|:---|:---:|
| **Madarafzar Hooshmand** | Co-founded company in Isfahan — IoT, embedded systems, microcontrollers and PCB design | ![ACTIVE](https://img.shields.io/badge/-ACTIVE-64c93e?style=flat-square) |
| **Rezerv-Yar** | Browser extension that auto-reserves next week's meals on the IUT dining system | ![SAMPLING](https://img.shields.io/badge/-SAMPLING-f2a541?style=flat-square) |
| **MediCase** | AI clinical-simulation web app for medical students (team project) | ![ACTIVE](https://img.shields.io/badge/-ACTIVE-64c93e?style=flat-square) |

## 6 Device Support

<p align="center">
  <img src="https://skillicons.dev/icons?i=c,py,js,react,flask,html,css,mysql,bash,linux,debian,ubuntu,git,vscode&perline=14" alt="Toolchain: C, Python, JavaScript, React, Flask, HTML, CSS, MySQL, Bash, Linux, Debian, Ubuntu, Git, VS Code">
</p>

## 7 Revision History

| Rev | Changes |
|:---:|:---|
| **E** | *Current.* Focus moved to embedded security, IoT security and PCB design. VitalBand in development |
| D | Co-founded Madarafzar Hooshmand Isfahan |
| C | Started Electrical Engineering at IUT, joined the IEEE Student Branch |
| B | Moved to Linux full-time, started hacking on TryHackMe |
| A | Initial release: web development with Python, Flask, JavaScript and React |

## 8 Ordering Information

To order, collaborate, or report a bug in this device:

<p align="center">
  <a href="mailto:sinayeganeh.dev@gmail.com"><img src="https://img.shields.io/badge/MAIL-sinayeganeh.dev@gmail.com-64c93e?style=for-the-badge&labelColor=0b152c" alt="Email"></a>
  <a href="https://github.com/sina-yeganeh"><img src="https://img.shields.io/badge/GH-sina--yeganeh-64c93e?style=for-the-badge&logo=github&logoColor=white&labelColor=0b152c" alt="GitHub"></a>
</p>

---

<p align="center">
  <img src="./assets/scope.svg" width="100%" alt="Oscilloscope showing a PPG heartbeat waveform: signal, always learning">
</p>

<p align="center">
  <sub><b>IMPORTANT NOTICE</b> — This device is provided "as is". No warranty, express or implied.</sub>
</p>
<p align="center">
  <sub>May run hot near deadlines and occasionally reboot into a new side project. © 2026 Sina Yeganeh</sub>
</p>
