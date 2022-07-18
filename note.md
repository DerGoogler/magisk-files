## Magisk f74eddef-delta by HuskyDG

### What is new?

- Update script for Magisk installation to system partition
- Canary or Debug build now will tell you to update if version name is mismatched


### Diff from official

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
- [General] Change magisk directory from `/data/adb/modules` to `/data/unencrypted/magisk_modules` and symlink back on FBE so you can manage module from Recovery.
- [MagiskInit] Inject Magisk services through `exec` option
- [MagiskHide] Introduce MagiskHide Dualspace mode to hide Magisk from all apps on dual space
- [MagiskHide] Introduce MagiskHide WhiteList mode to hide Magisk from all apps except apps that have been previously granted root access from Magisk
- [Manager] Show all supported languages in Language settings for Chinese ROM
- [Modules] Support systemless deleting files or folders for modules. [Learn more about it...](https://huskydg.github.io/blog/delete-file-and-folder-by-magisk-module)
- [General] Introduce Anti Zygote loop feature to automatically boot into Core-only mode if zygote fails to start for many times (bootloop)

### About MagiskHide WhiteList

After WhiteList is enabled, Magisk will be hidden from all apps by default and only previously apps have been granted root access from Magisk can continue to access Magisk.

Temporarily turn off MagiskHide WhiteList if you want to grant root access to new apps

MagiskHide WhiteList has significant performance and memory consumption issue and might break some modules that require app to read (overlay module, systemize app, ...). Only use WhiteList if necessary

### About Zygisk

[Read here to learn more about Zygisk...](https://huskydg.github.io/blog/zygisk-can-be-detected-very-easily)

## Magisk (9183a0a6) (25101)

- Sync to public release

## Diffs to v25.1

- None