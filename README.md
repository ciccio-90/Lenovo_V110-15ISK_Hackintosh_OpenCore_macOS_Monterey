 
# Lenovo V110-15ISK Hackintosh OpenCore 0.7.2 macOS Big Sur 11.5.2

EFI folder to run macOS Big Sur 11.5.2 on Lenovo V110-15ISK Laptop using OpenCore 0.7.2 as bootloader.

## Dortania's OpenCore Install Guide

https://dortania.github.io/OpenCore-Install-Guide

## About this Laptop

### Original Hardware

Type | Spec | Status
:---------|:---------|:----------
Computer		| Lenovo V110-15ISK   | Working
BIOS Version	| 1KCN51WW | Working
CPU				| Intel(R) Core(TM) i3-6006U CPU @ 2.00GHz | Working
Chipset			| Intel Skylake | Working
Graphics		| Intel Skylake GT2 [HD Graphics 520] | Working
Audio			| Realtek ALC236, Codec ID:10EC0236 / 17AA3814 | Working
Ethernet		| Realtek RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller | Working
Wi-Fi			| Intel(R) Dual Band Wireless-AC 3165 | Working
Bluetooth		| Intel(R) Wireless Bluetooth(R) | Working
Touchpad & Keyboard		| Synaptics 19.4.18.37 Elan 11.4.108.3 | Working
Webcam		    | BISON 10.0.15063.11299 AVC 10.0.15063.11299 Chicony 10.0.15063.11299 AWA 10.0.15063.11299 | Working
HDMI | Intel 21.20.16.4821 | Partially working (Built-in Display works only after comes back from sleep mode)
Micro SD Card Reader | Realtek 10.0.15063.31235 | Not working

### Modifications

Type | Status
:--------- |:---------
Samsung SSD 850 EVO 250GB Media | Working
RAM 12.00 GB | Working

### Software

Type | Status
:---------|:---------
Battery Status | Working
Brightness with keys (F11 - F12) | Working
Sleep | Working
iMessage & iServices | Not working

### Used Kexts 
 
Kext | Info 
:---------|:---------
[Lilu.kext](https://github.com/acidanthera/Lilu/releases) | Arbitrary kext and process patching on macOS.
[AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases) | Intel Wi-Fi Drivers for macOS.
[IntelBluetoothFirmware.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | Intel Bluetooth Drivers for macOS.
[IntelBluetoothInjector.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | Intel Bluetooth Drivers for macOS.
[AppleALC.kext](https://github.com/acidanthera/AppleALC/releases) | Native macOS HD audio for not officially supported codecs.
[RealtekRTL8111.kext](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases) | OS X open source driver for the Realtek RTL8111/8168 family (V2.2.2).
[VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases) | SMC emulator layer.
[SMCBatteryManager.kext](https://github.com/acidanthera/VirtualSMC/releases) | Used for measuring battery readouts on laptops.
[SMCProcessor.kext](https://github.com/acidanthera/VirtualSMC/releases) | Used for monitoring CPU temperature.
[SMCSuperIO.kext](https://github.com/acidanthera/VirtualSMC/releases) | Used for monitoring fan speed.
[USBInjectAll.kext](https://github.com/Sniki/OS-X-USB-Inject-All/releases) | Kext to inject all USB ports for the installed Intel EHCI/XHCI chipset automatically.
[VoodooPS2Controller.kext](https://github.com/acidanthera/VoodooPS2/releases) | For systems with PS2 keyboards, mice, and trackpads.
[WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen/releases) | Various patches necessary for certain ATI/AMD/Intel/Nvidia GPUs.

### Used SSDT 

Kext | Info | Refrence Link 
:---------|:--------- |:---------
SSDT-PLUG-DRTNIA.aml | Used for enabling Apple's XCPM in macOS, allowing for far better CPU power management. | [Link](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PLUG-DRTNIA.aml)
SSDT-EC-USBX-LAPTOP.aml | Used for disabling your real Embedded controller and creating a fake one for macOS to play with. USBX portion is used for injection USB power properties missing on Skylake and newer. | [Link](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-EC-USBX-LAPTOP.aml)
SSDT-PNLF.aml | Used for controlling the backlight on internal displays such as AIOs and laptops. | [Link](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PNLF.aml)
SSDT-XOSI.aml | Enables many Windows-only functionality in macOS. Requires XOSI patch. | [Link](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-XOSI.aml)
