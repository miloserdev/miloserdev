# Miloserdev

Senior C developer · low-level network systems

[GitHub](https://github.com/miloserdev) · [Telegram](https://t.me/miloserdev)

## About

I build high-performance network software in C/C++ and Rust: userspace and kernel packet processing, eBPF/XDP, VPP, DPDK, and Suricata-based IPS. I work close to the hardware and the Linux kernel across x86, ARM, RISC-V and Elbrus E2K. I take part in developing servers based on Ampere Altra, and I have written and maintained Linux kernel modules, including peripheral drivers for mobile devices.

## Skills

**Languages**  
`C`, `C++`, `Rust`, `Python`, `JavaScript (Node.js)`

**Networking**  
`VPP`, `DPDK`, `eBPF/XDP`, `Suricata`, `netfilter`, `TLS/OpenSSL`, `Wireshark`, `tcpdump`

**Kernel and hardware**  
`Linux Kernel`, `Device Tree`, `PCIe`, `Drivers`, `Buildroot`, `OpenBMC`, `GDB / KGDB`, `Flamegraph`

**Infrastructure**  
`CI/CD`, `Ansible`, `Pacemaker/Corosync`, `Docker`, `Podman`, `Kubernetes`

**Architectures**  
`x86`, `ARM`, `RISC-V`, `Elbrus E2K`

## Experience

### Ideco — Software Engineer

*Sep 2025 – Jul 2026 · high-load network stack, real-time traffic moderation*

- VPP plugins for L2/L3 traffic processing: forwarding, VLAN tags, packet classification
- Integrated Suricata IPS into the VPP pipeline: process nodes, session timeouts, flush mechanisms
- Worker threads, barrier sync, atomic operations
- UU-encoding support in the smtp.rs MIME parser (Suricata 8, Rust)
- TLS/SSL inspection: TCP proxy, connection contexts, TLS profiles
- Patches to Linux network components (libnetfilter_conntrack, libnetfilter_queue)
- Hot-path optimization: zero-copy, queue splitting
- GDB debugging, code review and mentoring on multithreading and memory handling

### SmartEcoSystem — Software Engineer

*Jun 2024 – Aug 2025 · Linux-based smartphones and tablets*

- AYYA TrustPhone: RootFS and Linux kernel for Rockchip RK3588 and MediaTek MT6771V
- R&D Elvees: Alt Linux (Simply) via Buildroot, Device Tree and drivers (display, touchpad, fingerprint sensor, charge controller)

### NII Mashtab — Software Engineer

*Oct 2023 – Aug 2025 · virtualization platform*

- Ported the VeiL product to ARM and RISC-V; adapted software for Elbrus E2K
- OpenBMC (Aspeed AST2500) and firmware (BIOS) modifications
- eBPF/XDP traffic filter with a userspace perceptron in C with AVX-accelerated inference, BPF maps between kernel and userspace
- Qt5 thin client for Kaspersky OS with token support (eToken, JaCarta, Rutoken); passed Kaspersky Lab testing
- FastAPI clustering microservice (Pacemaker, Corosync, LVM, iSCSI, Multipath, systemd), shipped in the product release
- CI/CD pipelines and deployment automation with Ansible

### SimbirSoft — Software Engineer

*May 2024 – May 2025 · Scanfactor project, hardware processing and computer vision*

- NVIDIA Tegra drivers for Jetson Nano, PCIe subsystem, Device Tree changes
- Team code review (C, Python)

### RUDN University — Software Engineer

*Jun 2020 – Aug 2022 · system administration*

- REST API and backend for a class-schedule monitoring web app (Python)
- Linux server administration for the university learning portal, automation scripts

## Education

- RUDN University — Applied Informatics in Economics, software engineer, expected 2028
- RUDN University — Programming in Computer Systems, programmer technician, 2021

## Contact

Telegram: [@miloserdev](https://t.me/miloserdev) · GitHub: [miloserdev](https://github.com/miloserdev)
