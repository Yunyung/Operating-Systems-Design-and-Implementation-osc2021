<div align="center">
   <h3> Operating Systems Design and Implementation </h3>
   <p>64-bit unix-like kernel for Raspberry Pi 3B+ (CPU: Arm Cortex A53)</p>
   <a href="https://grasslab.github.io/NYCU_Operating_System_Capstone/index.html">NYCU, Operating System Capstone, Spring 2021</a>
</div>

<br>

## Author

| Student ID | GitHub Account | Name | Email                      |
| -----------| -------------- | ---- | -------------------------- |
| 0856167    | Yunyung        | 許振揚| yungyung7654321@gmail.com  |

## About this Repository
* This is the repository for the labs in NCTU CS Operating Systems Capstone(OSC, or OSDI) Spring 2021 class.
* We are going to design some important part in the OS implementation.
* The hardware we use is **Raspberry Pi 3 Model B+**.

## How to Use This Repository
* Lab instruction is in [here](https://grasslab.github.io/NYCU_Operating_System_Capstone/index.html).
* You can download different labs in branch and release.
* [Here](https://hackmd.io/VD1WElEAQNGVpZx4mI9KXQ?both) are some references we use in each lab.

## Labs
* **Lab 0: Environment Setup**
    * [Branch](https://github.com/Yunyung/osc2021/tree/LAB-00)
* **Lab 1: Hello World**
    * [Branch](https://github.com/Yunyung/osc2021/tree/LAB-01)
* **Lab 2: Bootloader**
    * [Branch](https://github.com/Yunyung/osc2021/tree/LAB-02)
* **Lab 3: Allocator**
    * [Branch](https://github.com/Yunyung/osc2021/tree/LAB-03)
* **Lab 4: Exception and Interrupt**
    * [Branch](https://github.com/Yunyung/osc2021/tree/LAB-04)
* **Lab 5: Thread and User Process**
    * [Branch](https://github.com/Yunyung/osc2021/tree/LAB-05)
* **Lab 6: Virtual File System**
    * [Branch](https://github.com/Yunyung/osc2021/tree/LAB-06)
* **Lab 7: File System Meets Hardware**
    * [Branch](https://github.com/Yunyung/osc2021/tree/LAB-07)
* **Lab 8: Virtual Memory**
    * [Branch](https://github.com/Yunyung/osc2021/tree/LAB-08)

## Progress Overview
- [x] Lab0: Environment Setup
- [x] Lab1: Hello World
- [x] Lab2: Booting
- [x] Lab3: Allocator
- [x] Lab4: Exception and Interrupt Handling
- [x] Lab5: Multitasking
- [x] Lab6: Virtual Filesystem
- [x] Lab7: Filesystem Meets Hardware
- [x] Lab8: Virtual Memory

## Kernel Features
- [x] Initialize rpi3 (Clear bss segment, set stack pointer...)
- [x] Set up mini UART
- [x] Kernel shell
#### Booting
- [x] UART bootloader
- [x] Loading cpio archive 
- [x] Bootloader Self Relocation 
- [ ] Parsing Devicetree 
#### Exception & Interrupt
- [x] Synchronous exception handling 
- [x] Asynchronous interrupts (i.e. Hardware interrupt) handling. (Including core timer, mini uart I/O)
- [x] MiniUART I/O - supports sync/async I/O 
- [x] Timer Multiplexing
- [ ] Concurrent I/O Devices Handling 
#### Multitasking
- [x] Create kernel/user thread
- [x] Context switch
- [x] Task Scheduler
- [x] System call. (fork / exec / wait / exit...)
- [x] User / Kernel threads
- [x] Wait queues
- [x] User preeption 
- [x] Kernel preemption - protect critical sections 
- [ ] POSIX Signals - kill(), signal(), sigreturn()
#### Memory allocator
- [x] Buddy Memory Allocator
- [x] Slab Allocator
- [ ] Startup Allocator
#### Vitual Memory
- [x] Kernel/User virtual address space
- [x] Page fault handler
- [x] mmap
- [x] Demand paging
- [ ] ELF Loader 
- [ ] Copy on Write
#### Virtual File System 
- [x] Virtual filesystem (VFS) 
- [x] VFS APIs and interfaces - open / read / write / close / mount ...
- [x] VFS System calls
- [x] Multi-levels VFS 
- [x] Memory-based file system, tmpfs. And mount the tmpfs as the root file system.
- [x] Component name cache mechanism for faster pathname lookup 
- [x] Read a directory 
- [x] System-wide opened file table, Per-process file descriptor tables 
- [x] Populate the root file system with initramfs
- [x] Mount Another File System 
- [ ] /proc file system
#### File System & Interact with sdcard
- [x] Fat32 file system - read / write / open / close ...
- [x] Read/write data from an SD card hardware
- [x] Access hardware devices by the VFS
- [x] Mount the FAT32 File System 
- [x] Parse MBR (Master Boot Record)
- [ ] FAT32 with LFN (Long File Name) support 
- [ ] Device File
- [ ] Memory as cache for external storage
