# Acer-v3-371-547H
English | [简体中文](./README.zh-cn.md)<br>
English documents translated by Apple Translate.<br>
This document and EFI really took a lot of time. It's almost impossible for me to spend so much time doing one (of course, I may put the appreciation code in the end, but no one will give it), but I really have a lot of interest in technology. I think it's actually worth it to let more people feel this happiness together.
## Hardware configuration
CPU: Intel I5 5200U 2.2Ghz 2-core<br>
GPU: Intel HD Graphics 5500 Core Graphics<br>
Memory: Original 4GB Samsung 1.35v 1600MHz Plus a dual-channel of the same memory group Total 8GB<br>
Hard disk: HDD 500G recommends using SSD, otherwise Hackintosh will start up slowly.<br>
Sound card ID: ALC283 Layout ID is 11<br>
Wireless card (Bluetooth and WIFI): BCM943224PCIET2 (NGFF transfer card) (self-replacement) This card needs to add a driver in the new MacOS Wifi (this EFI has been added), and in MacOS 12 (Menterey) Bluetooth needs to replace the driver (this EFI has been replaced. If you need to use MacOS Big Sur, you need to replace the original driver, it could have been achieved by setting the kernel version, but I like the new system and I am lazy, so I wrote another tutorial, you can see the end)
## Driver situation
The driver is basically perfect (there is also a little defect and precautions during the installation process, which I tried and made mistakes step by step, and there is a model toss around together)
### Driven hardware
CPU (transformable frequency)<br>
GPU (1536M)<br>
Trackpad and keyboard (there are intermittent unavailable on the OC boot page, which has little impact. If you need to operate, I will give the last solution)<br>
The sound card ALC283 layout 11 can be driven, and there is noise in the 3.5mm headphone jack. Speakers and microphones are available. Let's see if 3.5mm noise can be solved in the future. ( Flag +)<br>
USB 3.0 is available (USB2.0 is also available)<br>
Available under the network card MacOS12, AirDrop, Handoff, Shared. ( Unable to test without an iPad) Airtransmission speed is about 20m/s.<br>
Battery: number of battery cycles, plug-in status, power availability can use.(There may be problems with plug-in power detection, which has no impact.)<br>
Camera available through Facetime test<br>
Attachment: Fn key operation is available<br>
### Undrive hardware
The card reader is to be tested (there is no demand for the time being, there is no toss around, and the speed is estimated to be not very good)<br>
There is something wrong with hibernation (screen saver is available, I put it for 3 hours)
## Considerations
These solutions are only suitable for identical models.
### Pre-installation considerations
1. Update the logic board Bios<br>
https://www.acer.com/ac/en/US/content/support-product/5487?b=1 <br>
Download the latest version of Bios and update it.<br>
2. Modify logic board settings<br>
Boot-Boot Mode to `UEFI`
Change Boot-Secure Boot to `Diskabled` (if you can't modify it, please set the Bios password first)
Main-F12 Boot menu to `Enabled` 
### Page key mouse is not available when booting OC
Detailed methods can be found on my blog.There are no advertisements on blogs at present.<br>
https://blog.gatesx.cn/oc-ps2.html
### Black screen after running the code
At this time, MacOS has actually started. You need to close
![Wechat](https://user-images.githubusercontent.com/84220224/149635235-3f295841-d2cf-4579-b2a7-00b5345ff77e.jpg)
![Alipay](https://user-images.githubusercontent.com/84220224/149635237-1d548a3f-12c8-4c4b-81a8-08b455b9801f.jpg)