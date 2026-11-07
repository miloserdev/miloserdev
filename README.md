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
*Aug 2026 – present · ARM server platforms, virtualization, server firmware*

- Building out an ARM (aarch64) server platform and datacenter: porting system software, building custom Linux kernels.
- Ported Proxmox to ARM on Debian 13. Custom KVM-enabled kernel plus dependency shims to install it without Proxmox's own kernel.
- Kasm running on ARM under ALT Linux Server 11.1. Kernels built with Mellanox OFED support; Harbor registry built for aarch64.
- Maintain OpenBMC on in-house boards (Aspeed, mickledore/styhead): isolate downstream patches against each board's upstream base and rebase them onto the target upstream. Rebranded webui-vue.
- Architecting an ARM hosting/cloud with billing: KVM/LXC, per-tenant virtual networks, self-service vCPU/RAM/disk configurator (Vite + shadcn/ui).
- GPU-offload R&D comparing aarch64 against x86 on cost and energy. SIMD compute kernels (AVX on x86, NEON on ARM), Ampere Altra Max 128-core vs EPYC 7742.

### Ideco — Software Engineer
*Sep 2025 – Jul 2026 · high-load network stack, real-time traffic moderation*

- Developed VPP plugins for L2/L3 traffic: forwarding, VLAN tagging, packet classification.
- Integrated Suricata IPS into the VPP pipeline (process nodes, session timeouts, flush mechanisms).
- Multithreading: worker threads, barrier sync, atomics.
- Added UU-encoding to the smtp.rs MIME parser (Suricata 8, Rust).
- TLS/SSL inspection: TCP proxy, connection contexts, TLS profiles.
- Patched Linux netfilter components (libnetfilter_conntrack, libnetfilter_queue).
- Hot-path optimization: zero-copy, queue splitting.
- GDB debugging, code review, and mentoring the team on multithreading and memory.

### SmartEcoSystem — Software Engineer
*Jun 2024 – Aug 2025 · part-time (0.5 FTE), subsidiary of NII Mashtab · Linux smartphones and tablets*

- Built RootFS and the Linux kernel for the AYYA TrustPhone (Rockchip RK3588, MediaTek MT6771V).
- R&D at Elvees: ALT Linux (Simply) via Buildroot, Device Tree, and drivers for display, touchpad, fingerprint sensor and charge controller.

### NII Mashtab — Software Engineer
*Oct 2023 – Aug 2025 · virtualization platform*

- Ported the VeiL virtualization product to ARM and RISC-V; adapted it for Elbrus E2K.
- Modified OpenBMC (Aspeed AST2500) and BIOS firmware.
- Built an eBPF/XDP traffic filter with a userspace perceptron in C (AVX-accelerated inference), sharing BPF maps between kernel and userspace.
- Qt5 thin client for Kaspersky OS with hardware-token support (eToken, JaCarta, Rutoken). Passed Kaspersky Lab testing.
- FastAPI clustering microservice (Pacemaker, Corosync, LVM, iSCSI, Multipath, systemd), shipped in the product release.
- CI/CD pipelines and deployment automation with Ansible.

### SimbirSoft — Software Engineer
*May 2024 – May 2025 · contract · Scanfactor, hardware processing and computer vision*

- Developed NVIDIA Tegra drivers for the Jetson Nano (PCIe subsystem, Device Tree changes).
- Team code review (C, Python).

### RUDN University — Software Engineer
*Jun 2020 – Aug 2022 · system administration*

- REST API and backend for a class-schedule monitoring web app (Python).
- Administered Linux servers for the university learning portal; wrote automation scripts.
- Prototyped a smart-home system on ESP32/ESP8266 (firmware in C).

## Education

- **RUDN University**, Applied Informatics in Economics (software engineer, expected 2028)
- **RUDN University**, Programming in Computer Systems (programmer technician, 2021)

## Projects

- **[net_neural_filter](https://github.com/miloserdev/net_neural_filter)**: eBPF/XDP packet filter with a neural-network (perceptron) classifier for adaptive DDoS and anomaly detection. XDP runs in the kernel data path; events reach userspace over a BPF ring buffer, BPF maps inspected with `bpftool`. C, libbpf, Clang/LLVM.
- **[xec](https://github.com/miloserdev/xec)**: Embedded Controller (EC) utility in C for ST and Nuvoton ECs. Controls LEDs, fan speed, charging and the Wi-Fi/Bluetooth power switch, and watches EC memory for changes.
- **[mpu6050_userspace](https://github.com/miloserdev/mpu6050_userspace)**: userspace I2C driver for the MPU-6050 IMU on Linux (MilkV Duo), through the Linux i2c subsystem. Written in C.
- **[sunxi_licheerv](https://github.com/miloserdev/sunxi_licheerv)**: Linux kernel and U-Boot bring-up for the LicheeRV D1 board (Allwinner D1, RISC-V). Kernel/U-Boot forks, an Arch Linux RISC-V SD-card image, display and LED bring-up (ST7789V, WS2812).
- **[arch_khadas](https://github.com/miloserdev/arch_khadas)**: Arch Linux ARM port for the Khadas VIM4 SBC (aarch64). Bootable BOOT/ROOTFS images over U-Boot.
- **[copydisk](https://github.com/miloserdev/copydisk)**: command-line tool in C that turns a whole `/dev/diskX` block device into a small sparse image.

**Also:** full-stack tooling: [xcale](https://github.com/miloserdev/xcale) (load-testing panel + agent), [newspaper](https://github.com/miloserdev/newspaper) (Markdown-based news engine), [xross](https://github.com/miloserdev/xross) (Node.js HTTP router).

## Contact

GitHub: [miloserdev](https://github.com/miloserdev) · Telegram: [@miloserdev](https://t.me/miloserdev)
