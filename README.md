# AsRock_B460M_PRO_Monterey_Hackintosh_OC
AsRock B460M Pro, i5 10600K, OC 0.8.2, Monterey 12.5, BigSur 11.6.8

## 基本信息

* OpenCore: 0.8.2 DEBUG
* MacOS
  * BigSur 11.6.8
  * Monterey 12.5

> 支持引导 BigSur 和 Monterey  

## Hackintosh + OpenCore 0.8.2

* https://dortania.github.io/OpenCore-Desktop-Guide
* https://www.sqlsec.com/tags/%E9%BB%91%E8%8B%B9%E6%9E%9C/
* https://github.com/3Alan/Hackintosh-i5-10400-B460M-MORTAR-WIFI

## TODO
- [ ] 测试黑果完美程度
- [ ] USB 定制
- [ ] 清理OC工具
- [ ] 移除部分DEBUG信息

## Work

* 图形界面EFI
* 核显硬件加速
* USB端口识别（能用，未完全测试）
* WIFI
* 集显DP输出
* 独显DP输出
* 风扇转速显示
* 独显温度显示（需额外软件

### 未测试
* 睡眠/唤醒
* 声卡输出
* 蓝牙
* 隔空投送


## 硬件

* 见：https://iitii.github.io/2021/09/10/1/
* GPU 使用 UHD630集显和蓝宝石 RX460 OC 4GB 版本，都有视频输出（因为RX460只有一个 DP 接口，不够用。。。


## BIOS 设置
* 见：https://iitii.github.io/2021/09/10/1/

## 非EFI问题及解决方案

* 为了方便拍错，默认打开DEBUG，日志输出到启动所用的 EFI 分区

* HIDPI: https://github.com/xzhih/one-key-hidpi
* 亮度调节工具（前提是显示器支持调节）: https://github.com/MonitorControl/MonitorControl

* windows和mac时间不同步问题 windows下管理员身份运行命令
```pwsh
Reg add HKLM\SYSTEM\CurrentControlSet\Control\TimeZoneInformation /v RealTimeIsUniversal /t REG_DWORD /d 1
```
* windows/mac 蓝牙设备共用需要重新配对的问题 解决方案：https://www.reddit.com/r/hackintosh/comments/mtvj5m/howto_keep_bluetooth_devices_paired_across_macos/

> 当然也有现成的脚本：https://github.com/digitalbirdo/BT-LinkkeySync  



