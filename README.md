# Operating Systems Capstone 2021

## Author

| Student ID | GitHub Account | Name | Email                      |
| -----------| -------------- | ---- | -------------------------- |
| 0856167    | Yunyung        | 許振揚| yungyung7654321@gmail.com  |

## Files
| File          | Content      | 
| --------------| ------------ | 
| linker.ld     | linker script|
| a.S           | source code  |

## Prerequisite
Follow [here](https://grasslab.github.io/NYCU_Operating_System_Capstone/labs/lab0.html) to install required target toolchain, and use them to buuld bootable image for rpi3.

## How to build From Source Code to Kernel Image

### From Source Code to Object Files
```
aarch64-linux-gnu-gcc -c a.S
```

### From Object Files to ELF
```
aarch64-linux-gnu-ld -T linker.ld -o kernel8.elf a.o
```

### From ELF to Kernel Image
```
aarch64-linux-gnu-objcopy -O binary kernel8.elf kernel8.img
```

## Run on QEMU
```
qemu-system-aarch64 -M raspi3 -kernel kernel8.img -display none -d in_asm
```