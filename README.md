# Miloserdev

Senior C engineer · low-level and high-performance network systems

[GitHub](https://github.com/miloserdev) · [Telegram](https://t.me/miloserdev)

## About

Senior C/C++ engineer with 5+ years of commercial experience. My focus is high-performance network software and low-level systems: userspace and kernel packet processing (eBPF/XDP, VPP, DPDK, Suricata-based IPS), and Linux kernel work close to the hardware. I've shipped across x86-64, ARM (aarch64), RISC-V and Elbrus E2K: bringing up and porting system software on new server platforms, writing kernel modules and device drivers, building out ARM datacenter and virtualization stacks.

## Skills

**Languages**  
`C`, `C++`, `Rust`, `Python`, `JavaScript (Node.js)`

**Networking & Dataplane**  
`VPP`, `DPDK`, `eBPF/XDP`, `Suricata IPS`, `netfilter`, `conntrack`, `nfqueue`, `TLS/OpenSSL`, `Wireshark`, `tcpdump`

**Linux Kernel & Hardware**  
`Linux Kernel`, `Kernel Modules`, `Device Drivers`, `Device Tree`, `PCIe`, `Buildroot`, `OpenBMC`, `Mellanox OFED`, `GDB / KGDB`, `Flamegraph`

**Virtualization & Clustering**  
`KVM`, `LXC`, `QEMU`, `Proxmox`, `Pacemaker/Corosync`, `LVM`, `iSCSI`, `Multipath`

**Infrastructure & Tooling**  
`CI/CD`, `Ansible`, `Docker`, `Podman`, `Kubernetes`, `Harbor`, `Git`

**Architectures**  
`x86-64`, `ARM (aarch64)`, `RISC-V`, `Elbrus E2K`

## Experience

### E-FLOPS — Software Engineer

_Aug 2026 – present · ARM server platforms, virtualization, server firmware_

- Building out an ARM (aarch64) server platform and datacenter: porting system software, building custom Linux kernels.
- Ported Proxmox to ARM on Debian 13. Custom KVM-enabled kernel plus dependency shims to install it without Proxmox's own kernel.
- Kasm running on ARM under ALT Linux Server 11.1. Kernels built with Mellanox OFED support; Harbor registry built for aarch64.
- Maintain OpenBMC on in-house boards (Aspeed, mickledore/styhead): isolate downstream patches against each board's upstream base and rebase them onto the target upstream. Rebranded webui-vue.
- Architecting an ARM hosting/cloud with billing: KVM/LXC, per-tenant virtual networks, self-service vCPU/RAM/disk configurator (Vite + shadcn/ui).
- GPU-offload R&D comparing aarch64 against x86 on cost and energy. SIMD compute kernels (AVX on x86, NEON on ARM), Ampere Altra Max 128-core vs EPYC 7742.
- LLM engineering: built a pipeline that ingests coding standards and open-source C and uses local LLMs to extract and cross-check rules into a single reviewed engineering playbook (~33k tokens);
- Swarm of local LLM agents behind hard gates (strict compilation, ASan/UBSan, coverage, mutation testing, sandbox) with a reader/judge eval harness to measure effect on process and code quality.

### Ideco — Software Engineer

_Sep 2025 – Jul 2026 · high-load network stack, real-time traffic moderation_

- Developed VPP plugins for L2/L3 traffic: forwarding, VLAN tagging, packet classification.
- Integrated Suricata IPS into the VPP pipeline (process nodes, session timeouts, flush mechanisms).
- Multithreading: worker threads, barrier sync, atomics.
- Added UU-encoding to the smtp.rs MIME parser (Suricata 8, Rust).
- TLS/SSL inspection: TCP proxy, connection contexts, TLS profiles.
- Patched Linux netfilter components (libnetfilter_conntrack, libnetfilter_queue).
- Hot-path optimization: zero-copy, queue splitting.
- GDB debugging, code review, and mentoring the team on multithreading and memory.

### SmartEcoSystem — Software Engineer

_Jun 2024 – Aug 2025 · part-time (0.5 FTE), subsidiary of NII Mashtab · Linux smartphones and tablets_

- Built RootFS and the Linux kernel for the AYYA TrustPhone (Rockchip RK3588, MediaTek MT6771V).
- R&D at Elvees: ALT Linux (Simply) via Buildroot, Device Tree, and drivers for display, touchpad, fingerprint sensor and charge controller.

### NII Mashtab — Software Engineer

_Oct 2023 – Aug 2025 · virtualization platform_

- Ported the VeiL virtualization product to ARM and RISC-V; adapted it for Elbrus E2K.
- Modified OpenBMC (Aspeed AST2500) and BIOS firmware.
- Built an eBPF/XDP traffic filter with a userspace perceptron in C (AVX-accelerated inference), sharing BPF maps between kernel and userspace.
- Qt5 thin client for Kaspersky OS with hardware-token support (eToken, JaCarta, Rutoken). Passed Kaspersky Lab testing.
- FastAPI clustering microservice (Pacemaker, Corosync, LVM, iSCSI, Multipath, systemd), shipped in the product release.
- CI/CD pipelines and deployment automation with Ansible.

### SimbirSoft — Software Engineer

_May 2024 – May 2025 · contract · Scanfactor, hardware processing and computer vision_

- Developed NVIDIA Tegra drivers for the Jetson Nano (PCIe subsystem, Device Tree changes).
- Team code review (C, Python).

### RUDN University — Software Engineer

_Jun 2020 – Aug 2022 · system administration_

- REST API and backend for a class-schedule monitoring web app (Python).
- Administered Linux servers for the university learning portal; wrote automation scripts.
- Prototyped a smart-home system on ESP32/ESP8266 (firmware in C).

## Education

- **RUDN University**, Applied Informatics in Economics (software engineer, expected 2028)
- **RUDN University**, Programming in Computer Systems (programmer technician, 2021)

## Projects
|                                                                                                      |                                                                                                                                                                               |
| ---------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="https://github.com/miloserdev/fl0w/raw/master/docs/images/screenshot.png" width="800px">   | [FL0W](https://github.com/miloserdev/fl0w) lets you build automations by dragging **blocks** onto a canvas and wiring their ports together                                    |
| <img src="https://github.com/miloserdev/newspaper/raw/master/docs/screenshot.png" width="800px">     | [Newspaper](https://github.com/miloserdev/newspaper) — **A file-based news engine.** Point it at a folder of markdown files                                                   |
| <img src="https://github.com/miloserdev/xcale/raw/master/webui/public/screenshot.png" width="800px"> | [xcale](https://github.com/miloserdev/xcale) — A panel for clustered machines testing                                                                                         |
| **[copydisk](https://github.com/miloserdev/copydisk)**                                               | A "mini slice" of a GPT disk<br>Turns a big disk (e.g. a 256 GB NVMe: EFI + root, ~2 GB used) into a small sparse image file that keeps **all identifiers**                   |
| **[net_neural_filter](https://github.com/miloserdev/net_neural_filter)**                             | eBPF/XDP packet filter with a neural-network (perceptron) classifier for adaptive DDoS and anomaly detection. XDP runs in the kernel data path; events reach userspace over a |
| **[xec](https://github.com/miloserdev/xec)**                                                         | Embedded Controller (EC) utility in C for ST and Nuvoton ECs. Controls LEDs, fan speed, charging and the Wi-Fi/Bluetooth power switch, and watches EC memory for changes.     |

## Contact

GitHub: [miloserdev](https://github.com/miloserdev) · Telegram: [@miloserdev](https://t.me/miloserdev)
