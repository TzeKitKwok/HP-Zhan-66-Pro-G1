# HP-Zhan-66-Pro-G1-macOS
惠普Zhan 66 Pro G1 安装 macOS Catalina & Mojave & High Sierra
## 电脑配置
|规格 | 详细信息|
|:-: | :-:|
|电脑型号|惠普 战 66 Pro G1|
|主板|惠普 83FD ( 英特尔 Xeon E3 - 1200 v6/7th Gen Intel Core)|
|处理器|英特尔 酷睿 i5 - 8250U|
|内存|~~镁光 8GB 2666Mhz DDR4~~ 镁光 16GB 2666MHz DDR4|
|硬盘|~~intel 600P 256G~~ 三星 SM961 256G|
|显卡|英特尔 UHD Graphics 620 ( 128 MB / 惠普 )|
|声卡| Conexant ISST Audio CX8200|
|网卡| ~~Intel 8265NGW~~ ~~博通BCM94352z(DW1560)~~ 博通934602CS 蓝牙4.2|

- ### 硬件部分
- 网卡：本机自带intel无线网卡还在不稳定阶段，建议更换博通网卡BCM94352z(DW1560)、博通934602CS2+延长转接卡、博通934602CS+延长转接卡 见下图

- [博通934602CS2点我](https://github.com/RenAmamiya/GitPic/blob/master/Zhan%2066%20Pro%20G1/BCM94360CS2.png)[DW1560点我](https://github.com/RenAmamiya/GitPic/blob/master/Zhan%2066%20Pro%20G1/DW1560.png)

- 硬盘：NVMe固态硬盘推荐SM961、PM961等等

-  ## 正常工作
- 显卡 声卡 电源 睡眠唤醒 WI-FI 蓝牙 触控板 HDMI VGA USB已内建 USBType-C SD读卡器

- ## 不正常工作 
- 独立显卡MX150（已屏蔽）

## 安装

- ### 安装前注意事项

- 按`F10`进入`BIOS`，设置语言为`简体中文`
- 按`➡️`选择`先进`，按`⬇️`选择`内置设备选项`，将`显存大小`设置`128MB`
- 按`➡️`选择`先进`，按`⬇️`选择`安全引导配置`，将`配置传统支持和安全引导`设置`禁用传统支持和禁用安全引导`

- ### 开始安装

- 准备一个16G的U盘、TransMac软件、DiskGenius、一个闲置的分区（80G以上）、BOOTICEX64、 [macOS镜像文件点我下载](https://blog.daliansky.net)

- 插入准备好的U盘，打开TransMac，右键U盘`Restore with Disk Image`,选择下载好的macOS下载文件，点击确定，开始执行macOS安装U盘制作，等待完成即可。

- 打开DiskGenius,左侧选择U盘的`ESP分区`，在右侧面板选择顶部`浏览文件`选项,点击EFI进去，替换掉旧的CLOVER右键强制删除，快捷键Ctrl+V复制下载好的CLOVER或者OpenCore引导（二选一）

- 重启电脑按F9`开机设置启动项`，按`⬇️`选择`选择文件引导`，找到刚才U盘ESP分区复制进去的引导文件`/U盘/EFI/CLOVER/CLOVERX64.efi`或`/U盘/EFI/OC/OpenCore.efi` CLOVER选择`macOS Install`,OpenCore按键盘上的数字选择`macOS install`

- 等待跑码进入`实用工具`，进入`磁盘工具`，选择刚才在Windows格式化好的分区，在上方点击`抹掉`，名称自定，格式化为`APFS`

- 点击左上角 退出`磁盘工具`，回到第一步安装界面，选择第二项`安装macOS`

- ### 安装后注意事项

- 终端输入`diskutil list`挂载磁盘EFI分区`sudo diskutil mount disk0s1`还有挂载U盘EFI分区`sudo diskutil mount disk1s1`将U盘引导目录复制到磁盘的EFI分区即可（注意双系统备份好其他系统的引导）

- 回到Windows 打开`BOOTICEX64`，选择`物理磁盘`，目标硬盘选择你的硬盘，点击`分区管理`给ESP分配盘符，点击BOOTICEX64上面的`UEFI`选项，点`修改启动序列`，点击`添加`，会出现刚才分配盘符的分区路径`/EFI/CLOVER/CLOVER.efi` `/EFI/OC/OpenCore.efi`直到弹出窗口算成功，不成功的多试几次。

- 使用DW1560的将文件`BrcmBluetoothInjector.kext``BicmFirmwareData.kext``BrcmPatchRAM3.kext`复制到`/Library/Extensions`目录下

- 打开`Kext Utility`输入密码重建缓存（触控板失效）

## 最后
- 出现自检错误实时时钟丢失（005）BIOS版本是`01.09.01`及以下的，使用`Docs`里面的`SSDT-RTC0.aml` BIOS版本查看方法：按`F10`进入`BIOS`,按`⬇️`选择`系统信息`就能看到BIOS版本

- 开启 [HIDPI](https://github.com/xzhih/one-key-hidpi)

- 如有其他问题，请加QQ群：814700280

## 参考及引用
- [黑果小兵](https://blog.daliansky.net)
- [远景论坛](http://www.pcbeta.com/)
- [Acidanthera](https://github.com/acidanthera)
- [RehabMan](https://bitbucket.org/RehabMan/)
- [HIDPI](https://github.com/xzhih/one-key-hidpi)
- [Hackintool](https://github.com/headkaze/Hackintool)
- [宪武整理的OC-little](https://github.com/daliansky/OC-little)
- [HP-Zhan-66-Pro-G2-macOS](https://github.com/chiccheung/HP-Zhan66-Pro14-G2-macOS)
- [unlockTDP](https://github.com/chiccheung/HP-Zhan66-Pro14-G2-macOS/tree/master/unlockTDP)
- [one-key-cpufriend](https://github.com/stevezhengshiqi/one-key-cpufriend)

## 感谢
- limurphy
- aa10786*****
- Duck
- LEE
- daliansky
- Cloverkits
- 宪武
- ChicCheung