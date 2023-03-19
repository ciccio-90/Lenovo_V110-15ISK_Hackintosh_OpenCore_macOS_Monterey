 
# Lenovo V110-15ISK Hackintosh OpenCore macOS Ventura

EFI folder to run latest macOS Ventura version on Lenovo V110-15ISK Laptop using OpenCore as bootloader.

## [Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide)

## About this Laptop

![Screenshot 2023-03-19 at 10 25 41](https://user-images.githubusercontent.com/66642459/226165932-525c3fe2-d234-495e-ab13-8525b96e36d3.png)

### Original Hardware

Type | Specification | Status
:---------|:---------|:----------
Motherboard	| Phoenix BIOS 1KCN51WW | Working
CPU | Intel(R) Core(TM) i3-6006U CPU @ 2.00GHz | Working
Ethernet | Realtek RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller | Working
Wi-Fi & Bluetooth | Intel Dual Band Wireless-AC 3165 Plus Bluetooth | Working
GPU | Intel Skylake GT2 HD Graphics 520 | Working
Audio | Realtek ALC236 | Working
HDMI | Intel Skylake HDMI | Working
Keyboard & Touchpad | Synaptics | Working
Webcam | EasyCamera | Working
Card Reader | Realtek RTS5129 USB 2.0 Card Reader | Working
USB | Sunrise Point-LP USB 3.0 xHCI Controller | Working

### Modifications

Type | Status
:--------- |:---------
Samsung SSD 850 EVO 250GB Media SATA | Working
RAM 12.00 GB | Working
Disc Burning | Removed

### Used Kexts 
 
Kext | Info 
:---------|:---------
[Lilu.kext](https://github.com/acidanthera/Lilu/releases) | Arbitrary kext and process patching on macOS.
[AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases) | Intel Wi-Fi Drivers for macOS.
[IntelBTPatcher.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | A Lilu base patcher that fix Intel Bluetooth.
[IntelBluetoothFirmware.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases) | Intel Bluetooth Drivers for macOS.
[BlueToolFixup.kext](https://github.com/acidanthera/BrcmPatchRAM/releases) | Needed for all non-native Bluetooth devices.
[AppleALC.kext](https://github.com/acidanthera/AppleALC/releases) | Native macOS HD audio for not officially supported codecs.
[RealtekRTL8111.kext](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases) | OS X open source driver for the Realtek RTL8111/8168 family.
[VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases) | SMC emulator layer.
[SMCBatteryManager.kext](https://github.com/acidanthera/VirtualSMC/releases) | Used for measuring battery readouts on laptops.
[SMCProcessor.kext](https://github.com/acidanthera/VirtualSMC/releases) | Used for monitoring CPU temperature.
[SMCSuperIO.kext](https://github.com/acidanthera/VirtualSMC/releases) | Used for monitoring fan speed.
[VoodooPS2Controller.kext](https://github.com/acidanthera/VoodooPS2/releases) | For systems with PS2 keyboards, mice, and trackpads.
[WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen/releases) | Various patches necessary for certain ATI/AMD/Intel/Nvidia GPUs.
[RealtekCardReader.kext](https://github.com/0xFireWolf/RealtekCardReader/releases) | An unofficial Realtek PCIe/USB-based SD card reader driver for macOS.
[RealtekCardReaderFriend.kext](https://github.com/0xFireWolf/RealtekCardReaderFriend/releases) | A Lilu plugin that makes System Information recognize your Realtek card reader as a native one.

### Used SSDTs

SSDT | Info
:---------|:---------
[SSDT-PLUG-DRTNIA.aml](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PLUG-DRTNIA.aml) | Used for enabling Apple's XCPM in macOS, allowing for far better CPU power management.
[SSDT-EC-USBX-LAPTOP.aml](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-EC-USBX-LAPTOP.aml) | Used for disabling your real Embedded controller and creating a fake one for macOS to play with. USBX portion is used for injection USB power properties missing on Skylake and newer.
[SSDT-PNLF.aml](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PNLF.aml) | Used for controlling the backlight on internal displays such as AIOs and laptops.
