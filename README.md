Droidian for the Samsung Galaxy Note10 Lite (`r7`)
====================================================

This repository builds the flashable Droidian image for the Samsung
Galaxy Note10 Lite (SM-N770F, codename `r7`). It is a community port,
not an official Droidian device.

Do not follow generic Droidian fastboot/`adb sideload` instructions for
this device — they do not apply here. This device is flashed with
`heimdall` (Linux) and TWRP; there is no fastboot-flashable image and no
`flash_all.sh`.

## Install

See **[INSTALL.md](https://github.com/note10lite-droidian/docs/blob/main/docs/INSTALL.md)**
in the docs repository. It covers the full procedure: unlocking the
bootloader, the Knox Guard wait, flashing with `heimdall`, putting TWRP
on the recovery partition, and writing the rootfs over `adb`.

Also read **[KNOWN-ISSUES.md](https://github.com/note10lite-droidian/docs/blob/main/docs/KNOWN-ISSUES.md)**
and the full **[STATUS.md](https://github.com/note10lite-droidian/docs/blob/main/docs/STATUS.md)**
feature table before you flash.

## Releases

Built images are published on this repository's
[Releases](https://github.com/note10lite-droidian/droidian-samsung-r7/releases)
page.

## Building

See **[BUILDING.md](https://github.com/note10lite-droidian/docs/blob/main/docs/BUILDING.md)**
in the docs repository.

## Repository layout

- `apt/` — this port's own patched-package overlay, consumed during the
  image build and by the port's own apt source on the device
  (`community-samsung-r7.list`, shipped by `adaptation-samsung-r7-configs`)
- `community_devices.yml` — the device recipe (packages, edition, variant)
- `.github/workflows/release.yml` — builds images on GitHub Actions,
  manually triggered only (`workflow_dispatch`)
