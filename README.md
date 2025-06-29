<div align="center">

# 💻 Simple 32-bit Operating System

## Bootable OS written in C and x86 Assembly — built to learn the fundamentals of low-level systems and how real kernels work.

![](https://img.shields.io/badge/C-007ACC?style=for-the-badge&logo=c&logoColor=white)
![](https://img.shields.io/badge/x86_Assembly-4CAF50?style=for-the-badge&logo=assemblyscript&logoColor=white)
![](https://img.shields.io/badge/NASM-000000?style=for-the-badge&logo=gnubash&logoColor=white)
![](https://img.shields.io/badge/QEMU-FF5722?style=for-the-badge&logo=qemu&logoColor=white)
![](https://img.shields.io/badge/Makefile-FFD700?style=for-the-badge&logo=gnubash&logoColor=black)

</div>

---

<div align="center">
  <!-- Replace with your actual paths if adding screenshots -->
  <img src="images/img1.png" width="49%" />
  <img src="images/img2.png" width="49%" /> 
</div>

---

## 📘 About

This project is a graphical 32-bit operating system built completely from scratch using NASM and C. It features a 16-bit bootloader, a C-based kernel, basic memory management, hardware-level keyboard/mouse input, double-buffered graphics, and cooperative multitasking. The OS runs entirely on bare-metal and is tested with QEMU.

---

## 🛠What’s Inside

- ✅ 16-bit bootloader written in Assembly that switches to protected mode
- ✅ C-based kernel loaded and executed with memory management setup
- ✅ Direct VGA memory access to display text and graphics
- ✅ Real-time hardware I/O handling (keyboard + mouse) using interrupts
- ✅ Double-buffered graphics for smooth animation rendering
- ✅ Cooperative multitasking (bouncing ball demo, etc.)
- ✅ Fully bootable `.img` file tested via QEMU

---

## 💡 What I Learned

- How x86 CPU boots and switches modes (real → protected)
- How bootloaders are written in NASM and assembled into raw binaries
- How a kernel is compiled with `gcc` and linked properly with a linker script
- How interrupts and hardware I/O are handled at the OS level
- How to build multitasking systems and basic window elements from scratch

---

## 🚀 Getting Started

### 🔧 Prerequisites

- [NASM](https://www.nasm.us/)
- [GCC](https://gcc.gnu.org/)
- [QEMU](https://www.qemu.org/)
- `make`

**_1. Build the OS_**

```bash
make
```

**_2. Run using QEMU_**

```bash
qemu-system-i386 -fda os.img
```

**_3. Clean Build_**

```bash
make clean
```

> Removes all object files and the generated image.

---

## 📦 Final Output

- The final output is a bootable floppy image os.img that can be run in any x86 emulator like QEMU or Bochs.

## Project Structure

```bash
/os
├── os.img
├── os.img.lock
├── boot/
│   ├── bin/
│   ├── images/
│   ├── utilities/
│   ├── boot.asm
│   ├── final.c
│   ├── font.c
│   ├── graphics.c
│   ├── graphics_elements.c
│   ├── graphics.h
│   ├── input.c
│   ├── kernel_entry.asm
│   ├── main.c
│   ├── makefile
│   ├── README.md
│   ├── task.c
│   └── vbe-modex.txt

```
