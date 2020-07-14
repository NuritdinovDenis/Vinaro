# Vinaro
Operation system

## Getting Started
These instructions will get you a copy of the project up and running on your pc

### Prerequisites
* Yasm
* dd

### Create a disk image
Step 1: Go to Clone or download

Step 2: Unzip the file

Step 3: Open the unpacked archive in the terminal

Step 4: Enter the following command to compile the boot.asm file
```yasm -f bin -o hello.bin hello.asm```

Step 5: Enter the following commands to create a bootable disk image

```
dd if=/dev/zero of=disk.img bs=1024 count=1440
dd if=hello.bin of=disk.img conv=notrunc
```

Step 6: Now you can start the system from a floppy disk image
