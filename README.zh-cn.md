# Acer-v3-371-547H
##  硬件配置
CPU ： Intel I5 5200U 2.2Ghz 2核
GPU ： Intel HD Graphics 5500 核显
内存 ： 原机4GB 三星 1.35v 1600MHz 后加 一条同内存组双通道 合计8GB
硬盘 ： HDD 500G 推荐使用SSD，不然黑苹果开机挺慢的
声卡ID ： ALC283 布局ID为11
USB ： USB3.0 x 1 ；USB2.0 x1 主板内有一条通道提供给蓝牙
无线网卡（蓝牙及WIFI）：BCM943224PCIET2（NGFF转卡）（自行更换）此卡在新的几个MacOS中Wifi需要添加驱动（本EFI已添加），在MacOS 12（Menterey）蓝牙需要更换驱动（本EFI已更换，如果需要使用MacOS Big Sur需要更换原驱动，本来可以通过设置内核版本实现，但是我喜欢新系统而且还懒，所以就另写教程了，见结尾）
## 驱动情况
已基本完美驱动（还有一点瑕疵和安装过程的注意事项，这可是我自己一步步试错出来的，有一样机型的一起折腾）
### 已驱动硬件
CPU（可变频）
GPU（1536M）
触控板及键盘（在OC引导页面有间歇次不可用，影响不大，如需操作我最后给出办法）
声卡 ALC283 布局11可驱动，3.5mm耳机孔存在杂音，扬声器及麦克风可用，未来看看能否解决3.5mm杂音。（Flag +）
USB 3.0 可用（USB2.0也可用）
网卡 MacOS12下可用，隔空传送，接力，共享剪贴板可用。（随航没有Ipad无法测试） 隔空传送速度20m/s左右。
电池 循环次数，插电状态，电量均可用（插电功率检测可能存在问题，没啥影响）
摄像头 通过Facetime测试可用
附：Fn键操作可用
### 未驱动硬件
读卡器待测试 （暂时没需求，没折腾，速度估计也不咋滴）
休眠存在问题（屏幕保护程序可用，我放了3h）

## 注意事项
这些解决方法都只适用于一模一样的机型
### 安装前注意事项
1.更新主板Bios
(https://www.acer.com.cn/support.html?type=1)[https://www.acer.com.cn/support.html?type=1]下载最新版Bios并更新。
2.修改主板设置
...等待补充
### 引导OC时页面键鼠不可用
方法正在编写，将发布于博客（既有流量【没有广告】又可以交流）
### 跑完代码后黑屏
此时其实MacOS已经启动了，你需要闭合屏幕再打开（不要闭合太久不然睡眠了），如果背光暗着就点下键盘。
解决方法我已经找到了（歪打正着），就是开启hidpi和注入eeid（我开启外置显示器时按错了结果解决了这个问题）
### 进入系统提示异常关机
这个问题暂时没有解决方案，没有影响系统，点击取消就行。