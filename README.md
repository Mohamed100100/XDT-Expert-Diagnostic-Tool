# XDT — eXpert Diagnostic Tool

> **Unified Diagnostic Services (UDS) Tester Tool**  
> *A Professional-Grade Automotive Diagnostic Platform*

<p align="center">
  <img src="images/logo-xdt.png" alt="XDT Logo" width="200"/>
</p>


<p align="center">
  <img src="images/logo-cairo-university.png" alt="Cairo University" width="150"/>
  &nbsp;&nbsp;&nbsp;
  <img src="images/logo-faculty-of-engineering.png" alt="Faculty of Engineering" width="150"/>
  <img src="images/Simenslogo.png" alt="Simenslogo.png" width="150"/>

</p>


---

## 📋 Project Overview

**XDT (eXpert Diagnostic Tool)** is a comprehensive desktop application designed for **off-board automotive diagnostics** using the **Unified Diagnostic Services (UDS)** protocol over **Diagnostic Communication over CAN (DoCAN)**. Developed as a graduation project at **Cairo University, Faculty of Engineering, Electronics and Electrical Communications Department**, and sponsored by **Siemens Digital Industries Software (DISW)**.

This repository contains the **complete technical documentation** for the XDT project. The source code is **closed-source** and proprietary.

---

## 🎯 Project Goals

- **Universal ECU Communication**: Speak the standardized diagnostic language of modern vehicles
- **Modular & Scalable Architecture**: Built on OSI model layers for maintainability and extensibility
- **OEM Adaptability**: One tool configurable for any vehicle brand or ECU configuration
- **Professional-Grade GUI**: Modern, intuitive interface with real-time feedback and simplified workflows
- **Full-Duplex Multi-ECU Support**: Handle simultaneous communication with multiple ECUs
- **Intelligent Assistance**: AI-powered copilot for diagnostic guidance and troubleshooting

---

## 🏗️ System Architecture

XDT follows a **layered architecture based on the OSI model**, ensuring clear separation of concerns and modular development:

```
┌─────────────────────────────────────┐
│  Front End: GUI (JavaFX)            │  ← Chapter 8
│  - Modern, responsive interface       │
│  - Real-time visual feedback          │
│  - Multi-scene navigation             │
├─────────────────────────────────────┤
│  Back End:                            │
│  ┌───────────────────────────────┐  │
│  │ Application Layer (ISO 14229-1)│  │  ← Chapter 3
│  │ - UDS Services Implementation   │  │
│  │ - Service ID (SID) management   │  │
│  │ - Request/Response handling     │  │
│  ├───────────────────────────────┤  │
│  │ Session Layer (ISO 14229-2)     │  │  ← Chapter 4
│  │ - Timing parameter management   │  │
│  │ - P2/P2*/P3/S3 timer handling   │  │
│  │ - Session keep-alive mechanisms │  │
│  ├───────────────────────────────┤  │
│  │ Network/Transport Layer         │  │  ← Chapter 5
│  │ (ISO 15765-2 - DoCAN)           │  │
│  │ - Segmentation & Reassembly     │  │
│  │ - Flow Control (FC) management  │  │
│  │ - Single/Multi-frame handling   │  │
│  ├───────────────────────────────┤  │
│  │ Data Link Layer (CAN)           │  │  ← Chapter 6
│  │ - USB-to-CAN bridge integration │  │
│  │ - Py4J Java-Python gateway      │  │
│  │ - Frame transmission/reception  │  │
│  └───────────────────────────────┘  │
└─────────────────────────────────────┘
              │
              ▼
        ┌──────────┐
        │   ECU    │
        │  (CAN)   │
        └──────────┘
```

---

## 📂 Repository Structure

```
XDT-Documentation/
├── README.md                          ← You are here (Main Overview)
├── images/                            ← All figures, diagrams, screenshots, and logos
│   ├── logo-xdt.png                   ← XDT project logo
│   ├── logo-cairo-university.png      ← Cairo University logo
│   ├── logo-faculty-of-engineering.png← Faculty of Engineering logo
│   ├── figure-01-vehicle-architecture.png
│   ├── figure-02-tool-setup.png
│   ├── figure-03-target-audience.png
│   └── ... (all project figures)
│
├── 01-Introduction/                   ← Chapter 1: Project Introduction
│   └── README.md
│
├── 02-Project-Overview/              ← Chapter 2: High-Level Architecture
│   └── README.md
│
├── 03-Application-Layer/             ← Chapter 3: UDS Services (ISO 14229-1)
│   └── README.md
│
├── 04-Session-Layer/                ← Chapter 4: Timing & Session Management (ISO 14229-2)
│   └── README.md
│
├── 05-Network-Transport-Layer-DoCAN/  ← Chapter 5: DoCAN Protocol (ISO 15765-2)
│   └── README.md
│
├── 06-Data-Link-Layer/              ← Chapter 6: CAN Integration & Hardware Bridge
│   └── README.md
│
├── 07-File-Parsing/                 ← Chapter 7: Firmware File Formats (S19, VBF)
│   └── README.md
│
├── 08-Graphical-User-Interface/     ← Chapter 8: GUI Design & Implementation
│   └── README.md
│
├── 09-Main-Features/                ← Chapter 9: Core Tool Features
│   └── README.md
│
├── 10-Challenges-and-Solutions/     ← Chapter 10: Development Challenges
│   └── README.md
│
├── 11-Future-Work/                  ← Chapter 11: Roadmap & Enhancements
│   └── README.md
│
└── 12-Appendix/                     ← Appendix: References, Acronyms, Standards
    └── README.md
```

---

## 🎓 Academic Information

| Field            | Details                                    |
| ---------------- | ------------------------------------------ |
| **University**   | Cairo University                           |
| **Faculty**      | Faculty of Engineering                     |
| **Department**   | Electronics and Electrical Communications  |
| **Project Type** | Graduation Project (June 2025)             |
| **Sponsor**      | Siemens Digital Industries Software (DISW) |
| **Supervisor**   | Prof. Neamat Abdel Kader                   |
| **Mentor**       | Eng. Islam Gamal                           |

### Team Members

- Karim Ayman Refaat
- Gomaa Mohamed Gamal
- Mohamed Ahmed Mohamed Ahmed
- Mohamed Shawky
- Janna Wael Ali Ali
- Sohaila Mohamed Nasr
- Reem Mohy Eldin Abdelrahman

---

## 📜 Standards & Compliance

XDT is built in strict compliance with international automotive standards:

| Standard        | Description                                           | Layer             |
| --------------- | ----------------------------------------------------- | ----------------- |
| **ISO 14229-1** | Unified Diagnostic Services (UDS) — Application Layer | Application       |
| **ISO 14229-2** | UDS — Session Layer Services                          | Session           |
| **ISO 15765-2** | Diagnostic Communication over CAN (DoCAN)             | Transport/Network |
| **ISO 11898-1** | CAN Data Link Layer and Physical Signaling            | Data Link         |
| **ISO 11898-2** | CAN High-Speed Medium Access Unit                     | Physical          |

---

## 🖼️ Visual Documentation

All diagrams, figures, screenshots, and architectural illustrations referenced throughout this documentation are located in the **`images/`** directory. Each section's README references the relevant figures by filename.

### Logos

| Logo                                                         | Filename                          | Description                                   |
| ------------------------------------------------------------ | --------------------------------- | --------------------------------------------- |
| <img src="images/logo-xdt.png" width="100"/>                 | `logo-xdt.png`                    | XDT — eXpert Diagnostic Tool project logo     |
| <img src="images/logo-cairo-university.png" width="100"/>    | `logo-cairo-university.png`       | Cairo University official logo                |
| <img src="images/logo-faculty-of-engineering.png" width="100"/> | `logo-faculty-of-engineering.png` | Faculty of Engineering, Cairo University logo |

> **Note**: Place all image files in the `images/` directory and update the references in each section's README accordingly.

---

## 🔧 Technology Stack

| Component                | Technology                     |
| ------------------------ | ------------------------------ |
| **Programming Language** | Java                           |
| **GUI Framework**        | JavaFX                         |
| **UI Markup**            | FXML                           |
| **UI Design Tool**       | SceneBuilder                   |
| **Styling**              | CSS                            |
| **IDE**                  | Eclipse                        |
| **CAN Bridge**           | Python (Py4J Gateway)          |
| **CAN Library**          | Open-source Python CAN library |
| **Project Management**   | Jira, Bitbucket, Git           |
| **Build Tool**           | Maven/Gradle                   |

---

## 🚀 Key Capabilities

### Diagnostic Services

- ✅ **Diagnostic Session Control** (0x10) — Default, Programming, Extended, Safety sessions
- ✅ **ECU Reset** (0x11) — Hard, Soft, Key-Off-On, Rapid Power Shutdown
- ✅ **Security Access** (0x27) — Seed-Key challenge-response with multiple levels
- ✅ **Tester Present** (0x3E) — Session keep-alive with configurable timing
- ✅ **Read Data By Identifier** (0x22) — Read DIDs (VIN, Speed, DTCs, etc.)
- ✅ **Read Data By Periodic Identifier** (0x2A) — Continuous data monitoring
- ✅ **Dynamically Define Data Identifier** (0x2C) — Custom DID composition
- ✅ **Write Data By Identifier** (0x2E) — Write configuration and calibration data
- ✅ **Read DTC Information** (0x19) — All 27 sub-functions supported
- ✅ **Routine Control** (0x31) — Start, stop, and request routine results
- ✅ **Request Download** (0x34) — Initiate firmware flashing
- ✅ **Request Upload** (0x35) — Memory content extraction
- ✅ **Transfer Data** (0x36) — Block-based data transfer
- ✅ **Request Transfer Exit** (0x37) — Finalize transfer sessions

### Advanced Features

- 🔧 **Software Download/Upload** — S19 and VBF file parsing and flashing
- 🔧 **Sequence Automation** — Create, save, and execute multi-service sequences
- 🔧 **ECU Testing System** — Automated test cases with pass/fail reporting
- 🔧 **XML Configuration** — OEM-adaptable service definitions without code changes
- 🔧 **AI Copilot** — Intelligent diagnostic assistance and code suggestions
- 🔧 **Advanced Logging** — Multi-level logging with structured folder hierarchy
- 🔧 **Multi-ECU Support** — Simultaneous communication with multiple ECUs
- 🔧 **Full-Duplex Operation** — Concurrent send/receive with multi-threading

---

## 📊 Project Timeline

The project was executed across 5 structured phases over approximately 8 months:

| Phase       | Duration | Focus                                              |
| ----------- | -------- | -------------------------------------------------- |
| **Phase 1** | Nov–Dec  | Learning & Foundation (UDS, ISO Standards, JavaFX) |
| **Phase 2** | Dec–Jan  | Requirement Analysis & Feature Definition          |
| **Phase 3** | Jan–Feb  | Architecture Design & Layered System Planning      |
| **Phase 4** | Feb–Apr  | Core Implementation (All OSI Layers)               |
| **Phase 5** | Apr–Jun  | Integration, Testing, Optimization & Documentation |

---

## ⚠️ Important Notes

1. **Source Code Availability**: This repository contains **documentation only**. The source code is closed-source and not publicly available.
2. **Image References**: All figures are stored in `images/`. Ensure images are placed there before viewing section READMEs.
3. **Standard Compliance**: All protocol implementations strictly follow ISO 14229 and ISO 15765 standards.
4. **Hardware Requirements**: XDT requires a USB-to-CAN adapter (e.g., Vector VX1000, PCAN, Kvaser) for ECU communication.

---

## 📖 How to Navigate This Documentation

1. **Start with `01-Introduction/`** for project motivation and UDS fundamentals
2. **Proceed to `02-Project-Overview/`** for architecture and system design
3. **Explore layer-specific directories (`03` through `06`)** for technical implementation details
4. **Review `07-File-Parsing/`** for firmware format specifications
5. **Check `08-Graphical-User-Interface/`** for UI/UX design decisions
6. **See `09-Main-Features/`** for complete feature descriptions and workflows
7. **Read `10-Challenges-and-Solutions/`** for development insights
8. **Visit `11-Future-Work/`** for planned enhancements and roadmap

---

## 📧 Contact & Acknowledgments

For inquiries about this documentation or the XDT project, please contact the project team through the academic department.

### Acknowledgments

- **Prof. Neamat Abdel Kader** — For continuous support, invaluable insights, and guidance
- **Eng. Islam Gamal** — For technical expertise, mentorship, and dedication
- **Siemens DISW** — For sponsorship and industry collaboration
- **Team Members** — For dedication, collaboration, and shared success

---

<p align="center">
  <img src="images/logo-xdt.png" alt="XDT" width="100"/>
</p>


<p align="center">
  <strong>One Tool. All ECUs.</strong>
</p>


<p align="center">
  <sub>© 2025 Cairo University — Faculty of Engineering. All rights reserved.</sub>
</p>

