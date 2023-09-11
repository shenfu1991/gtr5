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

 
 
 #完善程度
 cpu：基本正常，cinebench r23分数 单核1369，多核10117，高于 i7-7700k\i7-9880H,对比本人m1 max 分数，单核1507，多核12172
 
 显卡：集成显卡，已驱动，大多数情景正常，需要GPU加速的app会导致卡住退出，chrome浏览可以在设置中禁用GPU加速，其他有问题的app可以使用以下方式打开：
 
 `open -a Google\ Chrome --args --disable-gpu`
 
 USB：目前所有USB均能正常使用，type-c接口也正常，只是不能作为显示输出
 
 有线网卡：已驱动，但是有时候显示已连接却无法上网，需要手动设置ip地址
 
 声卡：正常驱动,目前插耳机正常
 
 无线网卡+蓝牙： 默认出厂为 `Mediatek mk7621k` 已更换为BCM94360Z4免驱
 
 
 #安装步骤
 
 1、安装请使用EFI-install.zip里面的EFI 
 2、安装完毕后用EFI.zip里面的EFI 
 
 




