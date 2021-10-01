# HP ProBook 450 G6 Hackintosh

Use Opencore Configurator to make changes in config.plist.

## Configuration

| Specifications      | Detail                       |
| ------------------- | ---------------------------- |
| CPU                 | Intel(R) Core(TM) i5-8265U   |
| Integrated Graphics | Intel UHD Graphics 620       |
| Sound Card          | Realtek ALC236 (layout-id:3) |
| Wireless Card       | Intel Wireless               |

## MacOS Versions Supported:

- macOS Big Sur 11.5.2

## Changelog

### 3-23-2021

#### Update

- `OpenCore` v0.7.3
- `AppleALC` v1.6.4
- `HibernationFixup` v1.4.3
- `Lilu` v1.5.6
- `VirtualSMC` v1.2.7
- `VoodooI2C` v2.6.5
- `VoodooPS2Controller` v2.2.5
- `WhateverGreen` v1.5.3

#### Add

- `AirportItlwm` v2.0.0
- OC resources(default 3 themes opencore (preorder Golden))

#### Change

- Change `alcid=11` boot-args(fix line-in mic)
- Proccessor type `1545`
- Bump opencore and kext

#### Remove

- Remove `CodecComander`
- Remove `SMCBatteryManager.kext`
- Remove `CPUFriend.kext`
- Remove `USBPorts.kext`

## What is Working?

- [x] Native CPU Power Management
- [x] Sleep/Wake
- [x] Intel Graphics
- [x] Audio
- [x] Trackpad (gestures)
- [x] Type-C USB
- [x] Type-C: video and audio
- [x] HDMI: video and audio
- [x] USB 3.0
- [x] Battery Management (thanks to [anor4k](https://www.tonymacx86.com/threads/guide-how-to-patch-dsdt-for-working-battery-status.116102/page-500#post-2021126) and [e285ne](https://www.tonymacx86.com/threads/guide-hp-probook-430-g6-whiskey-lake.282302/page-6#post-2147595))
- [x] Brightness
- [x] Built-in mic
- [x] Line-in mic
- [x] Bluetooth Intel
- [x] Intel wireless
- [x] Fn keys: play/pause, prt scr(F13), sound mute/-/+, sleep

## Not working:

- [ ] Fingerprint reader
- [ ] SD Card Reader
- [ ] Brightness fn keys (if not working, turn off the laptop and hold the power button for 30 seconds to reset EC)
- [ ] Built-in camera

## BIOS settings

- [ ] Fast Boot
- Secure Boot Configurations - Configure Legacy Support and Secure Boot = Legacy Support Disable and Secure Boot Disable
- Wake On LAN = Disabled
- Wake On WLAN = Disabled
- Video Memory size = 64 MB
- [ ] Fingerprint Device
- [ ] Media Card Reader in Port Options
- Wake on USB = optional

## For 440/450 users:

- Disable **USBPorts.kext** and remap USB with **USBInjectAll.kext** using **[Dortania guide](https://dortania.github.io/OpenCore-Post-Install/usb/intel-mapping/intel.html)** or **[Hackintool](https://www.tonymacx86.com/threads/release-hackintool-v3-x-x.254559/)**.
- Possibly need change layout-id in boot-args for **AppleALC.kext**

## IMPORTANT

Make sure to add SMBIOS of MacBook Pro 15.2 and serial number in config.plis.
