# cfadisk

The Hitachi Microdrive Filter Driver is a useful tool that allows you to **make your USB flash drive or SD card a fixed disk** in Windows.

It's implemented by filtering Removable Media Bit.

This repository is already imported as a Visual studio 2022 project for Windows 10. 

What you need to know about the usage:
1. Compile as kernel driver (cfadisk.sys)
2. Find the hardware ID of the device you want to install and fill in the inf file (cfadisk.inf)
3. Generate catalog file from inf file (cfadisk.cat)
4. Digital sign kernel driver and catalog file with a code signing certificate issued in 2015 or earlier
5. Timestamp sign kernel driver and catalog file via fake timestamp server
6. Install driver manually
