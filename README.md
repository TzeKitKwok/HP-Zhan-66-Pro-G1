# HP-Zhan-66-Pro-G1-macOS 由于换了新笔记本 本项目停止更新 请移步 战66一代：972643797 [战66-G1  MAC交流](https://jq.qq.com/?_wv=1027&k=9p74zRj2)
惠普Zhan 66 Pro G1 安装 macOS Big Sur & Catalina & Mojave & High Sierra 

## 电脑配置
|规格 | 详细信息|
|:-: | :-:|
|电脑型号|惠普 战 66 Pro G1|
|主板|惠普 83FD ( 英特尔 Xeon E3 - 1200 v6/7th Gen Intel Core)|
|处理器|英特尔 酷睿 i5 - 8250U|
|内存|镁光 16GB 2666MHz DDR4|
|硬盘|三星 SM961 256G|
|显卡|英特尔 UHD Graphics 620 ( 128 MB / 惠普 )|
|声卡|Conexant ISST Audio CX8200|
|网卡|博通934602CS 蓝牙4.2|


-  ## 正常工作
- 核心显卡 声卡 电源 睡眠唤醒 WI-FI 蓝牙 触控板 HDMI VGA USB已内建 USBType-C SD读卡器

- ## 不正常工作 
- 独立显卡MX150（已屏蔽）指纹识别（已屏蔽）

## BIOS设置

- [ ] Fast Boot
-     配置传统支持和安全引导 = 禁用传统支持和禁用安全引导
- [x] Virtualization Technology(VTx)
- [ ] Virtualization Technology for Directed I/O(VTd)
- [x] Enable Turbo Boost on DC
- [ ] Dynamic Platform Thermal Framework(DPTF)
- [x] High Performance 
- [ ] 通过LAN唤醒 = 已禁用
-     显存大小 = 128MB
-     显卡 = UMA显卡
- [ ] 指纹识别


## 注意事项

~~- 出现自检错误实时时钟丢失（005）BIOS版本是`01.09.01`及以下的，使用`Docs`里面的`SSDT-RTC0.aml`~~

- 使用EFI前请更新BIOS，[BIOS下载链接](https://support.hp.com/cn-zh/drivers/selfservice/hp-zhan-66-pro-g1-notebook-pc/17996593) ，F10进入BIOS在线更新(记得插网线)

- 更新10.15出现屏幕字体渲染发虚，毛刺严重在终端下执行
```shell
defaults delete -g CGFontRenderingFontSmoothingDisabled
```

- 开启 [HIDPI](https://github.com/xzhih/one-key-hidpi)
- [解锁TDP](https://github.com/TzeKitKwok/HP-Zhan-66-Pro-G1/tree/master/unlockTDP)
- [CPU变频](https://github.com/corpnewt/CPUFriendFriend)

## 如有其他问题，请加QQ群 

- 战66一代：972643797 [战66-G1  MAC交流](https://jq.qq.com/?_wv=1027&k=9p74zRj2)
- 战66二代：814700280

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
- [HP ProBook 430/440/450 G6 Hackintosh](https://github.com/KirillSerogodsky/HP-ProBook-430-440-450-G6-Hackintosh)
- [HpProbook450G6-Hackintosh](https://github.com/mehmetyukcell/HpProbook450G6-Hackintosh)
- [HP-ProBook-430-G5-Hackintosh](https://github.com/kreizlie/HP-ProBook-430-G5-Hackintosh)


## 感谢
- limurphy
- aa10786*****
- Duck
- LEE
- daliansky
- Cloverkits
- 宪武
- ChicCheung
- 重启大师
- kreizlie
- stopyan
