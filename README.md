# 零刻gtr5 黑苹果安装


|   规格   |                           详细信息                           |
| :------: | :----------------------------------------------------------: |
| 电脑型号 |                beelink GTR5 miniPC                 |
| 操作系统 |                Ventura              |
|  处理器  |       AMD 锐龙 R9-5900HX 8核16线程       |
|   内存   |            32 GB DDR4 3200MHz            |
| 硬盘1/2  |               1个 NVMe + 1个 m.2 SATA3                 |
|   显卡   |                 AMD Radeon Vega 8                 |
| 显示接口 |   DP +  HDMI （黑苹果不支持Type-c）    |
| USB   |   3个 USB3.0 + 2个 USB2.0 + 1个Type-c    |
|   声卡   |                       ALC 269                       |
| 无线网卡 | m.2 NGFF插槽，默认出厂为 `Mediatek mk7621k` 已更换为BCM94360Z4 |
| 有线网卡 |               realtek gaming 2.5gbe family controller (rtl8125)               |

 
 --------------
 
 
 # 完善程度 
 
 cpu：基本正常，cinebench r23分数 单核1369，多核10117，高于 i7-7700k\i7-9880H,对比本人m1 max 分数，单核1507，多核12172
 
 显卡：集成显卡，已驱动，大多数情景正常，`需要GPU加速的app会导致卡住退出`，chrome浏览可以在设置中禁用GPU加速，其他有问题的app可以使用以下方式打开：
 
 `open -a Google\ Chrome --args --disable-gpu`
 
 USB：目前所有USB均能正常使用，type-c接口也正常，只是不能作为显示输出
 
 有线网卡：已驱动，~~但是有时候显示已连接却无法上网，需要手动设置ip地址~~,目前已正常使用，自动获取ip。
 
 声卡：正常驱动,目前插耳机正常
 
 无线网卡+蓝牙： 默认出厂为 `Mediatek mk7621k` ~~已更换为BCM94360Z4免驱`，BCM94360Z4是比普通无线网卡宽一点的，gtr5耳机孔那里会挡住，最好换一款😂`~~，换后发现蓝牙正常，但是Wi-Fi无法打开，可能购买的版本有问题，已更换为94360cs2+转换卡（还在路上，未测试）
 
 
 # 安装步骤
 
 阿里云盘不限速下载Ventura13.5.1
 
`https://www.aliyundrive.com/s/QAbUj4bjuAQ` 提取码: 59yn,（由于阿里云盘不能分享 .dmg 格式的镜像文件，所以通过阿里云下载的镜像，需要自行更改文件名称改成 .dmg 结尾）  

  下载后用 balenaEtcher 写入到 16G 以上 U 盘，再自行挂载 U 盘的 EFI（自行搜索如何挂载EFI分区或使用`diskgenius格式化EFI分区并分配盘符`），在 EFI   引导分区替换对应的EFI文件夹即可，bios启动选择u盘,关闭安全引导（secure boot）,其他bios设置基本上不用动。
  
 1、安装请使用EFI-install.zip里面的EFI  
 2、安装完毕后用EFI.zip里面的EFI   
 3、理论上所有5800H\5900hx cup都能用此EFI 
 
# 加装SSD注意事项
 gtr5第二个m.2硬盘位仅支持sata3协议， 不支持nvme协议，本人加载了一个sata3 500G的SSD，安装了Windows11，目前是windows11 + macOS 13.5双系统。第一启动硬盘为MacOS所在SSD，开机会有windows11 和 MacOS选项。
 
 
 
 # 建议
 
 amd核显的黑苹果都使用了[NootedRed](https://github.com/ChefKissInc/NootedRed)，因此都是通病，就是上述显卡的问题，因此最好购买有免驱独显的机型。像铭凡HX80G/HX90G/HX99G,[相关链接](https://github.com/daliansky/minisforum-HX90G-Hackintosh),不过价格就上去了，基本上翻倍，gtr5大概2200左右，带独显的要4400左右。
 
 可以继续等待NootedRed项目完善，不久应该会有解决
 
 
 # 鸣谢
 本项目修改自[黑果小兵](https://github.com/daliansky/Beelink-SER5-Hackintosh)
 




