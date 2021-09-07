### How to install GSI Android 11 DotOs on Moto G8 Power (sofiar)

In this article I show you how to install GSI Android 11 on your Moto G8 Power

#### Requirements
- [Motorola Unlock Bootloader](https://motorola-global-portal.custhelp.com/app/standalone/bootloader/unlock-your-device-a) 
- [Installation of the latest stock firmware](https://mirrors.lolinet.com/firmware/motorola/sofiar/official/)
- [Download SDK Platform Tools](https://developer.android.com/studio/releases/platform-tools)
- [Download Android Verified Boot 2.0](https://dl.google.com/developers/android/qt/images/gsi/vbmeta.img?hl=tr)
- [Download GSI Android 11 DotOs with GApps](https://www.droidontime.com/)

### How to install GSI Android 11 DotOs

´´´
Folder structure
--> Root
-----> platform-tools
-----> GSI
   ----> dotOS-R-v5.1.3-arm64-GAPPS-OFFICIAL.img
   ----> vbmeta.img


# Commands 
../platform-tools/fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img
../platform-tools/fastboot reboot fastboot
../platform-tools/fastboot erase system
../platform-tools/fastboot erase system_a
../platform-tools/fastboot erase system_b
../platform-tools/fastboot delete-logical-partition product_a
../platform-tools/fastboot delete-logical-partition product_b
../platform-tools/fastboot flash system system-gapps.img 
../platform-tools/fastboot reboot recovery

# Note: In recovery you will have to do "Data Factory Reset"

´´´
