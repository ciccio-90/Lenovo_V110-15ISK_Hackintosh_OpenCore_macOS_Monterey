 
# Lenovo V110-15ISK Hackintosh OpenCore 0.7.2 macOS Big Sur 11.5.2

EFI folder to run macOS Big Sur 11.5.2 on Lenovo V110-15ISK Laptop using OpenCore 0.7.2 as bootloader.

## Dortania's OpenCore Install Guide

https://dortania.github.io/OpenCore-Install-Guide

## About this Laptop

### Original Hardware Info 💻

Type | Spec | Status
:---------|:---------|:----------
Computer		| Lenovo V110-15ISK   | Working
BIOS Version	| 1KCN51WW | Working
CPU				| Intel(R) Core(TM) i3-6006U CPU @ 2.00GHz | Working
Chipset			| Intel Skylake | Working
Graphics		| Intel Skylake GT2 [HD Graphics 520] | Working
Audio			| Realtek ALC236, Codec ID:10EC0236 / 17AA3814 | Working
Ethernet		| Realtek RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller | Working
WiFi			| Intel(R) Dual Band Wireless-AC 3165 | Working
Bluetooth		| Intel(R) Wireless Bluetooth(R) | Working
Touchpad & Keyboard		| Synaptics 19.4.18.37 Elan 11.4.108.3 | Working
Webcam		    | BISON 10.0.15063.11299 AVC 10.0.15063.11299 Chicony 10.0.15063.11299 AWA 10.0.15063.11299 | Working

### Modifications 🔨

Type | Spec | Status
:--------- |:---------|:----------
Samsung SSD 850 EVO 250GB Media | - | Working
RAM 12.00 GB | - | Working

### Software Status 👨‍💻

Type | Spec | Status
:---------|:---------|:----------
Battery Status | - | Working
Brightness with keys (F11 - F12) | - | Working
Sleep | - |  Working

### Used Kexts 
 
Kext | Info 
:---------|:---------
[Lilu.kext](https://github.com/acidanthera/Lilu) | Arbitrary kext and process patching on macOS.
[AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm) | Intel Wi-Fi Drivers for macOS.
[IntelBluetoothFirmware.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) | Intel Bluetooth Drivers for macOS.
[IntelBluetoothInjector.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) | Intel Bluetooth Drivers for macOS.
[AppleALC.kext](https://github.com/acidanthera/AppleALC) | For Audio.
[RealtekRTL8111.kext](https://github.com/Mieze/RTL8111_driver_for_OS_X) | RTL8111/8168/8411 PCI Express Gigabit Ethernet (V2.2.2).
[VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC) | SMC Emulator Layer.
[SMCBatteryManager.kext](https://github.com/acidanthera/VirtualSMC) | Battery Status Monitoring.
[SMCProcessor.kext](https://github.com/acidanthera/VirtualSMC) | Processor Temp Monitoring.
[SMCSuperIO.kext](https://github.com/acidanthera/VirtualSMC) | Fan Reading.
[USBInjectAll.kext](https://github.com/Sniki/OS-X-USB-Inject-All) | For USB Port mapping.
[VoodooPS2Controller.kext](https://github.com/RehabMan/OS-X-Voodoo-PS2-Controller) | Contains updated Voodoo PS/2 Controller, improved Keyboard & Synaptics TouchPad.
[WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen) | Various patches necessary for certain ATI/AMD/Intel/Nvidia GPUs. This is needed for Intel HD 520.

### Used SSDT 

Kext | Info | Refrence Link 
:---------|:--------- |:---------
SSDT-EC-USBX-LAPTOP.aml | Fix Embedded Controllers. For Skylake laptops and newer. | [Link](https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-fix.html#fixing-embedded-controller-ssdt-ecusbx)
SSDT-PLUG-DRTNIA.aml | Fixing Power Management. | [Link](https://dortania.github.io/Getting-Started-With-ACPI/Universal/plug.html)
SSDT-PNLF.aml | Fix Backlight. For most users. | [Link](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/backlight.html)
SSDT-XOSI.aml | This SSDT can be used instead of an OS Check Fix patch to simulate a version of Windows for Darwin. | [Link](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-prebuilt.html#trackpad)

### Troubles
 - Micro SD Card Reader - Not working.
 - HDMI (Audio & Built-in Display) - Not working.
