# PlayStation Vita

## Concepts
* There's no good or bad reason to be on 3.60 vs 3.65. However, 3.60 has a far larger userbase and is more tested.
* `tai/config.txt`: Plugin loader config. Can live in `ux0:` or `ur0:`, `ux0` takes priority, it *should* live in `ur0`.


## The Vita's Many Drives
* `ur0:`: Internal storage, user resources, LiveArea cache. Some homebrew stuff lives here, like your plugins and config.txt.
  **This is NOT the internal "memory card" on the 2000/PSTV.**
* `ux0:`: Active memory card. This might be the internal memory card on 2000/PSTV, a Sony memory card, or remapped SD2Vita/PSVSD/USB storage.
* `uma0:`: USB mass storage
* `imc0:`: "Internal" memory card of the 2000/PSTV, when not at `ux0:`
* `xmc0:`: External memory card, when not at `ux0`


## Plugins to have
* [iTLS-Enso](https://github.com/SKGleba/iTLS-Enso): Backport newer TLS CAs and TLSv1.2 support to pre-3.68
* [reAuth](https://forum.devchroma.nl/index.php/topic,362.0.html): Fix signing into the PSN on 3.60/3.65
* [0syscall6](https://github.com/SKGleba/0syscall6): Run software designed for any firmware version
* [kubridge](https://github.com/TheOfficialFloW/kubridge): Kernel-user bridge for the Vita, needed for some other stuff
* [DownloadEnabler](https://github.com/TheOfficialFloW/VitaTweaks/releases/tag/DownloadEnabler): Download anything within the web browser
* [shellbat](https://github.com/nowrep/vita-shellbat): Show battery percentage in the status bar
* [pngshot](https://github.com/xyzz/pngshot): Take screenshots as full quality pngs, with no watermark, in any app anywhere
* [NoNpDrm](https://github.com/TheOfficialFloW/NoNpDrm): Complete DRM bypass/disable
* [PSVshell](https://github.com/Electry/PSVshell/): Easy and reliable "overclocking" plugin
* [NoPowerLimitsVita](https://github.com/Electry/NoPowerLimitsVita): Bypass disabling cameras/wireless at higher power levels
* [CapUnlocker](https://github.com/GrapheneCt/CapUnlocker): Bypass some artificial limitations to increase functionality/performance of homebrew
* [VitaGrafix](https://github.com/Electry/VitaGrafix/): Change rendering resolution and max framerate for most popular games
  * You'll also want [VitaGrafixPatchlist](https://github.com/Electry/VitaGrafixPatchlist) and [VitaGrafix Configurator](https://github.com/Kirezar/VitaGrafixConfigurator)
* [vita-udcd-uvc](https://github.com/xerpi/vita-udcd-uvc): Output your Vita display to a connected computer as a webcam. Great for streaming/recording.
* [rePatch-reDux0](https://github.com/dots-tb/rePatch-reDux0): Patch Vita games with community made patches
* [DolcePolce](https://github.com/KuromeSan/DolcePolce): Bypass PSTV blacklist (only useful on the PSTV)
* [reVita](https://github.com/MERLev/reVita): Rebind buttons to other buttons, including touch screen events

## Other things to have
* [Adrenaline](https://github.com/TheOfficialFloW/Adrenaline/): It's like a PSP inside your PSV!
* [SimpleAccountSwitcher](https://bitbucket.org/SilicaAndPina/simpleaccountswitcher): Switch PSN accounts with far less pain than normal
* [StorageMgr](https://github.com/CelesteBlue-dev/PSVita-StorageMgr) or [YAMT](https://github.com/SKGleba/yamt-vita): Drivers and drive remapping for SD2Vita and/or PSVSD. Follow the guides on https://vita.hacks.guide for them. Use YAMT for just a SD2Vita, StorageMgr for PSVSD or USB storage.

## Things to avoid
* AutoPlugin (2): Great way to break your config.txt and have to do recovery on your Vita
* Enso\_ex: Can be used to replace the Team Molecule logo on bootup, but also the #1 source of bricked Vitas.
* reF00D: Less reliable than 0syscall6, causes some games to crash.

## Thing-specific notes
### NoNpDrm
To copy content off the original Vita to use elsewhere, follow [the instructions in the NoNpDrm](https://github.com/TheOfficialFloW/NoNpDrm#sharing-digital-applications) repo.

### PSVshell
What do those different clock speeds mean?

* `CPU`: Clock speed of the quadcore ARM Cortex A9
* `ES4`: Clock speed of the PowerVR SGX543MP4+ GPU
* `BUS`: Clock speed of the CPU's system bus
* `XBR`: Clock speed of the GPU's crossbar


## FAQ
### My Vita has been off for 1+ years, I just dug it out, and now it's behaving weird / everything is gone!
Very cheap/small flash storage, including (but not limited to) SD cards, **microSD** cards, Memory Sticks, and **Vita proprietary memory cards** only have a shelf life of around a year. Beyond that, and the data can become silently corrupted.

If your memory card becomes corrupted, unless you have a backup, you'll just have to start over from scratch. Sorry.
