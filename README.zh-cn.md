# Acer-v3-371-547H
简体中文 | [English](./README.md)<br>
英语文档使用Apple translate 翻译而成。<br>
这份文档和EFI真的花了很多时间，我之所以花这么多时间去做一件几乎不可能有收益（当然最后我可能会放赞赏码，其实也不会有人给的），但是我真的对科技有很大的兴趣，我觉得能让更多的人共同感受到这种快乐，那其实就值得了。
##  硬件配置
CPU ： Intel I5 5200U 2.2Ghz 2核<br>
GPU ： Intel HD Graphics 5500 核显<br>
内存 ： 原机4GB 三星 1.35v 1600MHz 后加 一条同内存组双通道 合计8GB<br>
硬盘 ： HDD 500G 推荐使用SSD，不然黑苹果开机挺慢的<br>
声卡ID ： ALC283 布局ID为11<br>
USB ： USB3.0 x 1 ；USB2.0 x1 主板内有一条通道提供给蓝牙<br>
无线网卡（蓝牙及WIFI）：BCM943224PCIET2（NGFF转卡）（自行更换）此卡在新的几个MacOS中Wifi需要添加驱动（本EFI已添加），在MacOS 12（Menterey）蓝牙需要更换驱动（本EFI已更换，如果需要使用MacOS Big Sur需要更换原驱动，本来可以通过设置内核版本实现，但是我喜欢新系统而且还懒，所以就另写教程了，见结尾）<br>
## 驱动情况
已基本完美驱动（还有一点瑕疵和安装过程的注意事项，这可是我自己一步步试错出来的，有一样机型的一起折腾）
### 已驱动硬件
CPU（可进行9档变频或睿频）<br>
GPU（HD5500）<br>
触控板及键盘（在OC引导页面有间歇次不可用，影响不大，如需操作我最后给出办法）<br>
声卡 ALC283 布局11可驱动，3.5mm耳机孔存在杂音，扬声器及麦克风可用，未来看看能否解决3.5mm杂音。（Flag +）<br>
USB 3.0 可用（USB2.0也可用）<br>
网卡 MacOS12下可用，隔空传送，接力，共享剪贴板可用。（随航没有Ipad无法测试） 隔空传送速度20m/s左右。<br>
电池 循环次数，插电状态，电量均可用（插电功率检测可能存在问题，没啥影响）<br>
摄像头 通过Facetime测试可用<br>
读卡器 已添加驱动，但我没有CD卡来测试<br>
附：Fn键操作可用。
### 未驱动硬件
休眠存在问题（屏幕保护程序可用，我放了3h）

## 注意事项
这些解决方法都只适用于一模一样的机型。
### 安装前注意事项
1.更新主板Bios。<br>
https://www.acer.com.cn/support.html?type=1 <br>
下载最新版Bios并更新。<br>
2.修改主板设置。<br>
Boot-Boot Mode 改为 `UEFI`
Boot-Secure Boot 改为 `Diskabled` （如果无法修改请先设置Bios密码）
Main-F12 Boot menu 推荐改为`Enabled`，便于修改引导项。
### 引导OC时页面键鼠不可用
详细方法可以去我的博客，博客目前没有广告。<br>
https://blog.gatesx.cn/oc-ps2.html
### 跑完代码后黑屏
此时其实MacOS已经启动了，你需要闭合屏幕再打开（不要闭合太久不然睡眠了），如果背光暗着就点下键盘。<br>
解决方法我已经找到了（歪打正着），就是开启hidpi和注入eeid（我开启外置显示器时按错了结果解决了这个问题）。<br>
可以前往https://blog.gatesx.cn/macos-hidpi.html 了解Hidpi和注入EEID开启hidpi的方法。
### 进入系统提示异常关机

这个问题暂时没有解决方案，没有影响系统，点击取消就行。<br>

## 更新记录
### 2022.1.17
添加了读卡器驱动，系统信息面板信息可以读取，但没有CD卡来让我测试。
---
![Wechat](https://user-images.githubusercontent.com/84220224/149635235-3f295841-d2cf-4579-b2a7-00b5345ff77e.jpg)
![Alipay](https://user-images.githubusercontent.com/84220224/149635237-1d548a3f-12c8-4c4b-81a8-08b455b9801f.jpg)