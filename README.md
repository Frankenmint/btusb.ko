[https://askubuntu.com/a/606941](https://askubuntu.com/a/1371453) The point is, I own a TPlink UB500 dongle and it didn't work on ARM ubuntu that I have compiled for the Orange pi 5.  To make it work, I found this topic on askubuntu and indeed it has worked to generate th btusb.ko file so I can use this bluetooth dongle on the orange pi 5!

Directions:

Copy this linked file to the firmware location for your given linux installation and run modprobe -v and modprobe -r to use verbose mode and reload the patched module.


```
sudo cp btusb.ko /lib/modules/$(uname -r)/kernel/drivers/bluetooth
sudo modprobe -r btusb
sudo modprobe -v btusb
```
