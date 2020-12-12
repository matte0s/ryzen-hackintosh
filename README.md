
# OpenCore EFI for AMD Ryzen Hackintosh (macOS 10.15.1 - 10.16)

## Specification
| **Component** | **Model** |
| ------------- | --------- |
| CPU | AMD Ryzen 5 1600 AF @ 3.7GHz |
| Motherboard | Gigabyte Aorus B450 PRO |
| RAM | 16GB (2 x 8GB) GSkill Ripjaws @ 3000MHz |
| Audio Chipset | Realtek ALC 1220|
| GPU | SAPPHIRE RX 5500 XT 8GB Nitro+ |
| OS Disk (SATA) | Samsung 860 Evo 500GB |

**macOS version**: 11.0.1 (20B50)
**OpenCore version**: 0.6.3  

## Credits
 - [[Bootloader] OpenCore](https://github.com/acidanthera/OpenCorePkg)
 - [[Resources] Picker GUI](https://github.com/acidanthera/OcBinaryData/tree/master/Resources)
 - [[Patch] AMD_Vanilla](https://github.com/AMD-OSX/AMD_Vanilla)
 - [[SSDT] EC-USBX-DESKTOP](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-EC-USBX-DESKTOP.aml)
 - [[SSDT] SLEEP-PTXH](./OC/ACPI/SSDT-SLEEP-PTXH.aml)
 - [[Driver] OpenRuntime](https://github.com/acidanthera/OpenCorePkg)
 - [[Driver] OpenCanopy](https://github.com/acidanthera/OpenCorePkg)
 - [[Driver] HFSPlus](https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi)
 - [[Kext] Lilu](https://github.com/acidanthera/Lilu)
 - [[Kext] VirtualSMC](https://github.com/acidanthera/VirtualSMC)
 - [[Kext] WhateverGreen](https://github.com/acidanthera/WhateverGreen)
 - [[Kext] AppleALC](https://github.com/acidanthera/AppleALC)
 - [[Kext] RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X)
 - [[Kext] AMDRyzenCPUPowerManagement](https://github.com/trulyspinach/SMCAMDProcessor)
 - [[Kext] SMCAMDProcessor](https://github.com/trulyspinach/SMCAMDProcessor)
 - [[Kext] AppleMCEReporterDisabler](https://github.com/AMD-OSX/AMD_Vanilla/blob/experimental-opencore/Extra/AppleMCEReporterDisabler.kext.zip)

## Compatible macOS versions
 - Catalina (10.15.x)
 - Big Sur (10.16/11.0)

## Issues
 - Partially-working virtualization (only VirtualBox & Parallels Dekstop 13.1.0 or below)
 - Not working 3.5mm Jack microphone (only USB/Bluetooth microphones)

## How to use
  1. Make your USB installer with [**this guide**](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
  2. Clone the repository and paste "BOOT" and "OC" directories into your's pendrive "EFI" folder
  3. Download [**GenSMBIOS**](https://github.com/corpnewt/GenSMBIOS) to generate unique SMBIOS information. Run it and select **Generate SMBIOS**, as the model select **iMacPro1,1**.
  4. Open config.plist with [**ProperTree**](https://github.com/corpnewt/ProperTree) and go to PlatformInfo > Generic. Set MLB (Board Serial), SystemSerialNumber (Serial) and SystemUUID (SmUUID) to generated values. Change ROM to your network card's MAC address without the `:` character. [**How to get MAC Address?**](https://www.wikihow.com/Find-the-MAC-Address-of-Your-Computer)
  5. Boot it!  

**You CAN NOT use SMBIOS from this repository, it MUST be unique for every macOS installation**

## Adobe applications fix
Adobe applications crash on AMD Hackintoshes due to missing intel_fast_memset instructions.  Follow [guide](https://gist.github.com/naveenkrdy/26760ac5135deed6d0bb8902f6ceb6bd) made by XLNC to get it working!  
If Photoshop still crashes when selecting font, you have to delete `/Applications/Adobe\ Photoshop\ 2020/Adobe\ Photoshop\ 2020.app/Contents/Required/Deep_Font`

## Other guides
**If you have any problems with installation or booting your macOS, kernel panics or another system related issue check OC configuration guide**  
**If something else isn't working properly (for example USB ports, iServices, DRM/Netflix) check Post-Install guide**
 - [Creating USB Installer](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
 - [Opencore cofiguration](https://dortania.github.io/OpenCore-Install-Guide/AMD/zen.html)
 - [Post-Install](https://dortania.github.io/OpenCore-Post-Install/)
 - [Troubleshooting](https://dortania.github.io/OpenCore-Post-Install/)
 - [ACPI Patching](https://dortania.github.io/Getting-Started-With-ACPI/)
 - [USB mapping](https://dortania.github.io/OpenCore-Post-Install/usb/)
 - [Change about this mac (CPUName)](https://amd-osx.com/forum/viewtopic.php?t=9516)
 - [Change about this mac (Logo)](https://github.com/jogerj/Mac-Ryzen-Logo)

If you have any other questions or issues, feel free to ask on [**AMD-OSX Discord**](https://discord.gg/EfCYAJW) or [**Forum**](https://forum.amd-osx.com)  

## Credits
 - [Apple](https://apple.com) for macOS
 - [Mikigal](https://github.com/mikigal/ryzen-hackintosh) for Readme.md
 - [AMD-OSX Developers](https://github.com/AMD-OSX) for kernel patches for AMD CPUs
 - [Acidanthera](https://github.com/acidanthera) for OpenCore and most of used kexts
 - [Trulyspinach](https://github.com/trulyspinach) for Ryzen power management and monitoring kexts
 - [Mieze](https://github.com/Mieze) for RealtekRTL8111 kext
 - [Dortania](https://github.com/dortania) for OpenCore configuration guides
 - [XLNC](https://github.com/naveenkrdy) for Adobe patches for AMD CPUs
 - [AMD-OSX Community](https://amd-osx.com) for support while making my Hackintosh
<br>

![Screenshot](/screenshot.png?raw=true)
