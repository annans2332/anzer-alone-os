# AnzerOS Beta 1.0

**The first custom UEFI OS created by Alone Gamerz.**

AnzerOS is a lightweight, experimental operating system built from scratch with UEFI support. This is a raw ISO image that can be run in virtual machines like QEMU or VirtualBox.

---

## Features

- Bootable UEFI ISO  
- Custom kernel and bootloader  
- Minimalist, experimental OS environment  

---

## Getting Started

These instructions will help you run AnzerOS safely in a virtual machine.

### Requirements

- [QEMU](https://www.qemu.org/) (Windows/Linux/Mac) or [VirtualBox](https://www.virtualbox.org/)  
- 4GB RAM recommended for QEMU

### Running in QEMU

```bash
qemu-system-x86_64 -m 4096 \
-drive if=pflash,format=raw,readonly=on,file="OVMF_CODE.fd" \
-drive if=pflash,format=raw,file="OVMF_VARS.fd" \
-cdrom "anzeros_beta1.0.iso" \
-boot d
