# Lenovo-m710q-Hackintosh-EFI
 Hackintosh EFI for Lenovo Thinkcenter m710q.
![Model](https://fardincompteq.com/wp-content/uploads/2018/03/M700-Tiny-600x600.png)

How it works:
![working](/Pics/1.JPG)
![1](img/os.jpg)

## System Specifications

- **Model:** Lenovo M710Q  
- **Processor:** Intel QTJ2(i7-10750H ES) 6c12t
- **Memory:** 8GB DDR4 2666 MHz  
- **Storage:** 512GB WD SN580 NVMe SSD  
- **Graphics:** Intel UHD630 Integrated Graphics 
- **Wifi Card** Not Installed 
## Features
- Working: USB Ports, Ethernet, Dual DP output, Built-in Audio, DP Audio, Graphics
- Won't Work at All: iPhone Mirroring(T2 Chip required), DRM-related stuff
- Do it Yourself If You Need it: Wifi, Bluetooth, AirDrop, Sidecar, etc

## BIOS Configuration

Before installing macOS, adjust your BIOS settings as follows:

1. **Disable CSM Support**  
   This ensures compatibility with macOS's UEFI booting requirements.
2. **Set VRAM to 64MB**  
   Configuring VRAM ensures proper functioning of Intel UHD630 graphics.
3. **Enable VT-d**  
   Required for macOS virtualization compatibility.
4. **Set SATA Mode to AHCI**  
   This is necessary for macOS to recognize SATA storage devices.

Save your changes and reboot to apply these settings.

## Known Issue: QTJ2 CPU Batch Problem
![2](img/bad-display.jpg)
[Watch How it Happened](https://youtu.be/CKHQxTijZmY)

If, after booting into macOS, the display output suddenly changes to a solid color (e.g., green, blue, or another uniform hue) within a few minutes, and the system logs do not report any errors, this issue is likely caused by a specific batch defect in the QTJ2 CPU. 

### Solution

- **Temporary Workarounds:** None.
- **Permanent Solution:** Replace the QTJ2 CPU with a compatible and unaffected model.

Unfortunately, due to the nature of the issue, no software configuration or patch can resolve this problem.

## Important! Important! Important!

**YOU MUST modify SN/UUID/MLB/ROM values in config.plist file. ROM value is the MAC address of your motherboard built-in network card, check it on BIOS settings.(I don't have network card so no need for me.))**
![SN/UUID/MLB](https://github.com/revunix/GIGABYTE-X399-Designare-EX/blob/main/images/MLBUUIDSN.png?raw=true)

## Special Thanks To:

[revunix](https://github.com/revunix/ThinkCentre-M710Q) for inspiration

[Apple](https://apple.com) for everything

[OpenCore](https://github.com/acidanthera/OpenCorePkg/releases/latest)

[Lilu](https://github.com/acidanthera/Lilu/releases/latest) 

[AppleALC](https://github.com/acidanthera/AppleALC/releases/latest)

[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases/latest) 

[WhateverGreen](https://github.com/acidanthera/whatevergreen/releases/latest) 

