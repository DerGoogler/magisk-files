## Magisk 7a6dd2cc-delta DEBUG by HuskyDG

> The Debug version has a more detailed log than the Canary version

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
- [MagiskInit] Inject Magisk services through `exec` option
- [MagiskHide] Add MagiskHide Dualspace mode to hide Magisk from all apps on dual space
- [MagiskHide] Add MagiskHide WhiteList mode to hide Magisk from all apps except apps that have been previously granted root access from Magisk
- [Manager] Show all supported languages in Language settings for Chinese ROM
- [Modules] Support systemless deleting files or folders for modules. [Learn more about it...](https://huskydg.github.io/blog/delete-file-and-folder-by-magisk-module)
- [General] Add bootloop protection feature

### About MagiskHide WhiteList

After WhiteList is enabled, Magisk will be hidden from all apps by default and only previously apps have been granted root access from Magisk can continue to access Magisk.

Temporarily turn off MagiskHide WhiteList if you want to grant root access to new apps

MagiskHide WhiteList has significant performance and memory consumption issue and might break some modules that require app to read (overlay module, systemize app, ...) and system performance might be dropped. Only use WhiteList if necessary

### About Zygisk

[Read here to learn more about Zygisk...](https://huskydg.github.io/blog/zygisk-can-be-detected-very-easily)

## Magisk (9183a0a6) (25101)

- Sync to public release

## Diffs to v25.1

- None