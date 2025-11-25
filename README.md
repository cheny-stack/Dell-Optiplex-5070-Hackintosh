# Dell Optiplex 5070 Micro Hackintosh

OpenCore EFI configuration for Dell Optiplex 5070 Micro.

## Hardware Specifications

| Component | Specification |
| --- | --- |
| **Model** | Dell Optiplex 5070 Micro |
| **CPU** | Intel Core i5-9500T / i7-9700T (Coffee Lake) |
| **GPU** | Intel UHD Graphics 630 |
| **Chipset** | Intel Q370 |
| **Audio** | Realtek ALC3204 (ALC255) |
| **Ethernet** | Intel I219-LM |
| **WiFi/BT** | Intel Wireless-AC 9560 / AX200 (Requires replacement or AirportItlwm) |

## BIOS Settings

*   **General**
    *   Boot Sequence: UEFI
    *   Advanced Boot Options: Uncheck "Enable Legacy Option ROMs"
    *   UEFI Boot Path Security: Always, Except Internal HDD
*   **System Configuration**
    *   SATA Operation: AHCI
    *   Drives: Check all
    *   SMART Reporting: Enable
    *   USB Configuration: Enable all
*   **Video**
    *   Primary Display: Auto
*   **Security**
    *   PTT Security: Enabled
*   **Secure Boot**
    *   Secure Boot Enable: Disabled
*   **Intel Software Guard Extensions**
    *   Intel SGX Enable: Disabled
*   **Performance**
    *   Multi Core Support: All
    *   Intel SpeedStep: Enabled
    *   C-States Control: Enabled
    *   Intel TurboBoost: Enabled
*   **Power Management**
    *   AC Recovery: Power Off
    *   Deep Sleep Control: Disabled
    *   USB Wake Support: Disabled
    *   Wake on LAN/WLAN: Disabled
*   **Virtualization Support**
    *   Virtualization: Enabled
    *   VT-d: Disabled (or Enabled if `DisableIoMapper` is True in config.plist)

## Kexts

*   **Lilu**: Arbitrary kext, library, and program patching for macOS
*   **VirtualSMC**: SMC emulator
*   **WhateverGreen**: Graphics patching
*   **AppleALC**: Audio patching
*   **IntelMausi**: Intel Ethernet LAN driver
*   **NVMeFix**: NVMe power management and compatibility
*   **SMCProcessor**: CPU temperature monitoring
*   **SMCSuperIO**: Fan speed monitoring
*   **USBInjectAll**: Injects all USB ports (Map your USB ports for stability!)
*   **VoodooPS2Controller**: PS2 keyboard/mouse driver

## ACPI

*   **SSDT-PLUG**: CPU Power Management
*   **SSDT-EC-USBX**: Embedded Controller and USB Power
*   **SSDT-AWAC**: RTC/AWAC fix
*   **SSDT-PMC**: NVRAM support for 300-series chipsets

## Credits

*   [Acidanthera](https://github.com/acidanthera) for OpenCore and Kexts
*   [Dortania](https://dortania.github.io/OpenCore-Install-Guide/) for the OpenCore Install Guide
