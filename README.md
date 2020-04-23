# HP-Zhan-66-Pro-G1-macOS
1、dw1560 10.15蓝牙失效将BrcmBluetoothInjector.kext、BrcmFirmwareData.kext、BrcmPatchRAM3.kext放入/System/Libary/Extensions下
进入终端输入命令sudo kextcache -i /重建缓存（触控板失效）
驱动来源：https://github.com/acidanthera/BrcmPatchRAM/releases
2、跑完代码重启进BIOS设置进入内置设备选项将显存大小设置为128M和Graphics设置为混合交火
3、出现开机自检错误，BIOS版本是01.09.01及以下的，使用Docs里面的SSDT-RTC0.aml
zhan66机型交流群：814700280