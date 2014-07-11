Qwin OS.

What do we need to run Qwin:

QEMU

At least 1 GB of RAM

Instructions:

If you want to have a new version of the system for testing, you need to download and compile the 
source code from the repository. If you just want to look at the system, regardless of its version, or 
are experiencing problems with the assembly - you can download the completed images of the older 
version from the repository "images".

building qwin from source:

1. cd to the directory where you extracted / cloned the source code of the system.
2. start make project with your opt. flags, eg. make -j5.
3. When the building is ready, we will get two images - boot.img and system.img.
4. Copy these images in any folder.

running qwin over qemu:

1. cd to the directory where you copied two system images(built from source,or obtained from "images" 
repo)
2. Type: qemu-system-i386 -hda boot.img -hdb system.img -m 512 -smp 1 (smp = number of 
cores 
to 
emulate,m = 
RAM in MB.)
3. Good Luck! :)

