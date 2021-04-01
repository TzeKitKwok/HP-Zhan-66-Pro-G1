# One-Key-UnlockTDP

### 安装方法

- 首次安装时运行 `install.command` 安装必要文件
- 每次唤醒后运行 `unlockTDP.command` 解锁 `TDP`
- 性能释放效果取决于机器散热情况

### 预设参数

- Junction Temperature：92 ℃
- Power Limt 2：35 W
- Power Limt 1；25 W

### 设置开机自启动
- 打开`com.voltageshift.unlocktdp.plist`的`Program`处填写`unlockTDP.command`所在路径，例 `/Users/noctis/unlockTDP/unlockTDP.command`
- 将`com.voltageshift.unlocktdp.plist`放到` /Library/LaunchDaemons`目录下
- 修改文件权限 `sudo chown root:wheel /Library/LaunchDaemons/com.voltageshift.unlocktdp.plist` `sudo chmod 644 /Library/LaunchDaemons/com.voltageshift.unlocktdp.plist`
- 启动服务并载入plist文件`sudo launchctl load /Library/LaunchDaemons/com.voltageshift.unlocktdp.plist` 或者重启
- 检查服务的运行状态 `sudo launchctl list`
### Credits

- `One-Key-UnlockTDP` made by [@stopyan](https://github.com/stopyan)
- `FED15900` Report by [@unclewebb](http://forum.notebookreview.com/threads/the-throttlestop-guide.531329/page-317)
- `rwmem` made by [@osresearch](https://github.com/osresearch/rwmem)
- `ModifiedDirecthwMakefile` made by [@CloverHackyColor](https://github.com/CloverHackyColor/directhw)
- `VoltageShift` made by [@sicreative](https://github.com/sicreative/VoltageShift)
- DirectHW is Copyright © 2008-2010 coresystems GmbH <info@coresystems.de>
