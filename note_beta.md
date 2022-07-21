## Magisk v25.2-delta by HuskyDG

> Synchronized with Magisk v25.2

### Diff from official

- [General] MagiskHide is restored and enabled by default
- [General] The package name is `io.github.huskydg.magisk`
- [MagiskHide] Hide Google SafetyNet process by default
- [General] Implement Core-only mode
- [General] Support installing Magisk into system partition
- [General] Add button to temporarily disable Magisk
- [General] Add button to download and install Riru core
- [General] Fix Magisk survival script `addon.d` when FBE cannot be decrypted: Change modules directory from `/data/adb/magisk` to `/data/unencrypted/MAGISKBIN` and symlink back
- [MagiskHide] Only reset sensitive props after boot completed
- [General] Change magisk directory from `/data/adb/modules` to `/data/unencrypted/magisk_modules` and symlink back on FBE so you can manage module from Recovery.
- [MagiskInit] Inject Magisk services through `exec` option
- [MagiskHide] Introduce MagiskHide Dualspace mode to hide Magisk from all apps on dual space
- [MagiskHide] Introduce MagiskHide WhiteList mode to hide Magisk from all apps except apps that have been previously granted root access from Magisk
- [Manager] Show all supported languages in Language settings for Chinese ROM
- [Modules] Support systemless deleting files or folders for modules. [Learn more about it...](https://huskydg.github.io/blog/delete-file-and-folder-by-magisk-module)
- [General] Introduce Anti Zygote loop feature to automatically boot into Core-only mode if zygote fails to start for many times (aka. bootloop)

### About MagiskHide WhiteList

After WhiteList is enabled, Magisk will be hidden from all apps by default and only previously apps have been granted root access from Magisk can continue to access Magisk.

Temporarily turn off MagiskHide WhiteList if you want to grant root access to new apps

MagiskHide WhiteList has significant performance and memory consumption issue and might break some modules that require app to read (overlay module, systemize app, ...). Only use WhiteList if necessary

### About Zygisk 💀

Zygisk is detectable and does not have hiding itself method like RiruHide. In additional, there are no hiding module that actually work, please don't enable Zygisk if unnecessary. [Read here to learn more about Zygisk...](https://huskydg.github.io/blog/zygisk-can-be-detected-very-easily)

## 2022.7.20 Magisk v25.2

Maintenance release fixing various issues.

- [MagiskInit] Fix a potential issue when stub cpio is used
- [MagiskInit] Fix reboot to recovery when stub cpio is used
- [MagiskInit] Fix sepolicy.rules symlink for rootfs devices
- [General] Better data encryption detection
- [General] Move the whole logging infrastructure into Rust

### Full Changelog: [here](https://topjohnwu.github.io/Magisk/changes.html)