# OpenCore 1.0.3 Stable - macOS Sequoia 15.4 - Lenovo ideapad 330S-15IKB (81F5)

![Captura de pantalla 2025-04-07 a la(s) 11 25 40 p m](https://github.com/user-attachments/assets/71b8d1fe-0eb7-4d68-8de7-e96f7e4cfdfe)

![Captura de pantalla 2025-04-07 a la(s) 11 37 28 p m](https://github.com/user-attachments/assets/10132e7b-7916-461c-90c1-6edbfd4add6d)

![Captura de pantalla 2025-04-07 a la(s) 11 39 13 p m](https://github.com/user-attachments/assets/3d423b32-6c96-4226-9d1c-7c602a943072)


This EFI is based on the JuicerV3 EFI: https://github.com/JuicerV3/Hackintosh_OpenCore_Lenovo-ideapad-330s-15ikb

Not use `AirportItlwm` and `IntelBluetoothFirmware` kext. Upgrading to Broadcom wireless card is recommended for better stability and features for current and future macOS versions. If you have intel wifi, I used this video for Intel Dual Band Wireless-AC 7265 AC Internal: https://www.youtube.com/watch?v=0lHxrMqT0WA&t=361s.

```
* I am not responsible for any damage done to your device. Use at your own risk.
* Please do some research if you concerns about features included in this EFI.
* Before continuing, you are choosing to make these modifications yourself
* if any thing goes wrong, it is your responsible for the damage that happen next.
```

## Important note

#### ***Every laptop are difference, even those with the same model number. So use this EFI as a reference and edit accordingly to your own hardware.***

### You need to generate your own SMBIOS to signin with Apple ID
Use CorpNewt's [GENSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate platforminfo using `MacBookPro15,2` (i5-8259U) as an SMBIOS

### What works
* Native OTA Updates
* Full Metal GPU Acceleration
* WiFi & Bluetooth connection stable with Heliport.
* Onboard Audio & Microphone
* Keyboard & Trackpad
* Webcam
* USB 3.0
* USB C
* SD Card reader
* HDMI Video/Audio output
* Battery read-out
* Display Brightness Control & BrightnessKeys
* Volume control keys
* Jack 3.5 Audio output.
* Sleep & Wake
* lid Sleep & Wake
* Hibernation

### What not works
* Airdrop & Continuity Features (Need native wificard)
*The Windows boot entry from the OpenCore bootloader didn't work, so I used the F12 key to change the operating system.

## Intel Wlan/Bluetooth Video Tutorial for Configuration
*https://www.youtube.com/watch?v=0lHxrMqT0WA&t=361s

from `EFI/OC/Kexts` folder and `config.plist` then replace with one that work for your card. otherwise Wifi&Bluetooth will not work properly or will not boot at all.

## Bios/UEFI Settings
**Configuration**
* Configuration
  * Storage > Controller Mode: `AHCI mode`
* Security
  * Intel Platform Trust Technology: `Enabled`, disable this for any issue to boot mac os
  * Secure Boot: `Disable`
* Boot
  * Boot Mode: `UEFI`
  * USB Boot: `Enabled`

## Laptop Specs/Details
* Model: `Lenovo ideapad 330S-15IKB (81F5)`
* Processor: `8th gen Core i5-8250U (Kaby Lake R)`
* CPUID: `Intel(R) Core(TM) i5-8250U CPU @ 1.60GHz`
* iGPU: `intel UHD Graphic 620`
* Ram: `12gb 4+8 @ 2400 MHz`
* DRIVE1 SSD: `Samsung EVO 870 500GB (SATA) (Windows)`
* DRIVE2 SSD: `Kingston NV1 (KINGSTON SNVS500G) (NVMe) (Mac OS Sequoia)`
* Keyboard connection type: `PS/2`
* Trackpad connection type: `I2C`
* Audio: `Realtek ALC236`
* Audio HDMI: `Intel Kaby Lake HDMI`
* Ethernet: `Not tested`
* WLAN: `Intel Dual Band Wireless-AC 7265 AC Internal`

##Windows Dual Boot Configuration
*Fast Start-up: `Disabled`, if the state is enabled, mac os reboot many times, check tutorial https://www.youtube.com/watch?v=L049J2yxY_w.

*Note: Sorry for my english, I speak spanish.

## Links/Guides
* https://github.com/acidanthera/OpenCorePkg (OpenCore Bootloader)
* https://dortania.github.io/OpenCore-Install-Guide/ (OpenCore Setup,Installation,Troubleshooting)
* https://github.com/corpnewt/GenSMBIOS (mac Serial)
* https://www.youtube.com/watch?v=0lHxrMqT0WA&t=361s (Wifi/Bluetooth Config)
* https://www.youtube.com/watch?v=L049J2yxY_w (Disable Windows start-up)
