# Resize LUKS Partition in VMWare

I created a disk with a default size, and quickly ran out of space. Here is some documentation on how I resized the disk.

## Virtual Disk Resize

You have to remove all snapshots before resizing the partition

Shut down the machine to resize the volume

Virtual Machine -> Settings -> Hard Disk

## Boot to Recovery ISO

VMWare Settings -> CD/DVD - Use the Mint startup disk
VMWare Settings -> Startup Disk


## Open LUKS disk
sudo cryptsetup open /dev/sda3 sda3_crypt

## Resize Partition
sudo parted 
resize 3

## Resize Physical Volume
sudo pvdisplay -m
sudo pvresize /dev/mapper/sda3_crypt 


## Resize Logical Volume
sudo lvresize -L +70G /dev/vgmint/root 

## Resize Filesystem
sudo resize2fs /dev/mapper/vgmint-root

