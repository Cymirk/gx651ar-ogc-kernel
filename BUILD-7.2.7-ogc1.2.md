# GX651AR OGC Kernel Build — 7.2.7-ogc1.2

## Base

- Upstream Linux: 7.2.7
- OGC base: v7.2.7-ogc1
- Fedora package environment: Fedora 44 container
- dwarves/pahole: 1.31

## GX651AR changes

This build adds three GX651AR-specific kernel changes on top of the OGC base:

1. `platform/x86: asus-armoury: add support for GX651AR`
   Commit: `7be2bf50c967`

2. `HID: asus: add ROG Zephyrus Duo GX651AR keyboard`
   Commit: `6d3af033dce5`

3. `soundwire: dmi-quirks: disable ghost Realtek on GX651AR`
   Commit: `91924178fb2a`

## Build

Package version:

`7.2.7-ogc1.2.fc44`

The RPM was built with OGC's Fedora 44 container workflow.

## Testing

The resulting kernel was installed and booted successfully:

`7.2.7-ogc1.2.fc44.x86_64`

The GX651AR SoundWire audio path was tested after boot and audio was confirmed working.

The Armoury and keyboard changes were verified in the preceding `7.2.7-ogc1.1.fc44` build and are included unchanged in this `ogc1.2` build.

## Note

This is a community/custom GX651AR build based on OGC's kernel package, not an official OGC release.
