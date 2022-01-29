# Acer-v3-371-547H-OC-EFI
简体中文 | [English](./README-en.md)<br>
##  硬件配置
详细配置请查看官网数据库：https://www.acer.com/datasheets/2014/4876/V3-371/NX.MPFCN.015.html<br>
硬盘 ： 三星870evo 250GB <br>
无线网卡（蓝牙及WIFI）：BCM943224PCIET2（`NGFF`转卡）（自行更换），我已经设置内核版本号来适配Monterey与旧的MacOS的蓝牙<br>
## 驱动情况
已基本完美驱动（还有一点瑕疵和安装过程的注意事项，这可是我自己一步步试错出来的，有一样机型的一起折腾）
### 已驱动硬件
CPU（可进行9档变频或睿频）<br>
GPU（Intel HD Graphics 5500）<br>
触控板及键盘（在OC引导页面有间歇性不可用）<br>
声卡 `ALC283`布局11可驱动，3.5mm耳机孔存在杂音，扬声器及麦克风可用，未来看看能否解决3.5mm杂音。（Flag +）<br>
USB均可用<br>
网卡 MacOS12下可用，隔空传送，接力，共享剪贴板可用。（改系统机型可能可以实现随航） 隔空传送速度20m/s左右。<br>
电池 循环次数，插电状态，电量均可用（插电功率检测可能存在问题，没啥影响）<br>
摄像头 通过Facetime测试可用<br>
读卡器 已添加驱动，但我没有CD卡来测试<br>
附：Fn键操作可用。（调节音量·亮度）
### 不完美硬件
3.5mm耳机孔存在杂音，但是V3-371的声卡布局为11。（已查看AppleAlc更新日志）
### 已知问题
休眠存在问题（屏幕保护程序可用，我放了3h）
## 注意事项
这些解决方法都只适用于一模一样的机型。
### 安装前注意事项
1.更新主板Bios。<br>
https://www.acer.com.cn/support.html?type=1 <br>
下载最新版Bios并更新。<br>
2.修改主板设置。<br>
Boot-Boot Mode 改为 `UEFI` （必要）
Boot-Secure Boot 改为 `Diskabled` （如果无法修改请先设置Bios密码） （必要）
Main-F12 Boot menu 改为`Enabled`，便于临时修改引导项。 （非必要）
### 引导OC时页面键鼠不可用
可以在引导界面时，按住下键并插拔有响应的USB设备（u盘·鼠标·iPhone）
### 跑完代码后黑屏
此时其实MacOS已经启动了，你需要闭合屏幕再打开（不要闭合太久否则系统会睡眠重启），如果背光暗着就点下键盘（任意键）。<br>
解决方法我已经找到了（歪打正着），就是开启hidpi和注入eeid（我开启外置显示器时按错了结果解决了这个问题）。<br>
可以使用下面的项目：<br>
https://github.com/xzhih/one-key-hidpi
### 进入系统提示异常关机
这个问题暂时没有解决方案，不影响系统，点击取消就行。<br>
## 更新日志
### 2022.1.22
定制USB。
中文文档改为README.md（主要文档）
### 2022.1.18
OpenCore版本升级至 0.7.7 （稳定通道）
### 2022.1.17
添加了读卡器驱动，系统信息面板信息可以读取，但没有CD卡来让我测试。

## 赞赏

![Wechat](https://user-images.githubusercontent.com/84220224/149635235-3f295841-d2cf-4579-b2a7-00b5345ff77e.jpg)
![Alipay](https://user-images.githubusercontent.com/84220224/149635237-1d548a3f-12c8-4c4b-81a8-08b455b9801f.jpg)
