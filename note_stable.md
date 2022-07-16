## Magisk v25.1-delta-2 by HuskyDG

> Synchronized with Magisk d81ccb77-delta

- [General] MagiskHide is restored, replace DenyList
- [Zygisk] Allow MagiskHide to handle isolated process
- [Zygisk] Clean up preload when hiding with MagiskHide
- [General] The package name is `io.github.huskydg.magisk`
- [MagiskHide] Use seperate `hidelist` instead of `denylist`
- [MagiskHide] MagiskHide is enabled by default
- [MagiskHide] Hide Google SafetyNet process by default
- [General] Add option to boot into Core-only mode
- [General] Support Magisk installation in system partition
- [General] Add Disable Magisk button
- [General] Add Riru core button
- [General] Fix Magisk survival script `addon.d` when FBE cannot be decrypted: Change modules directory from `/data/adb/magisk` to `/data/unencrypted/MAGISKBIN` and symlink back
- [MagiskHide] Only reset sensitive props after boot completed
- [General] Support system Magisk installation for devices with disabled SeLinux
- [General] Change modules directory from `/data/adb/modules` to `/data/unencrypted/magisk_modules` and symlink back on FBE so you can manage module from Recovery.

### About Zygisk

[Read here to learn more about Zygisk...](https://huskydg.github.io/blog/zygisk-can-be-detected-very-easily)

## Magisk v25.1 Official changes

- [MagiskBoot] Fix ramdisk backup being incorrectly skipped
- [MagiskBoot] Add new feature to detect unsupported dtb and abort during installation
- [Zygisk] Change binary hijack paths
- [App] Fix incorrect recovery mode detection and installation
- [MagiskInit] Fix config not properly exported in legacy SAR devices
- [General] Enforce the Magisk app to always match or be newer than magiskd
