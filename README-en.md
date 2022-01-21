# Acer-v3-371-547H
English | [简体中文](./README.md)<br>
## Hardware configuration
CPU: Intel I5 5200U 2.2Ghz 2 cores<br>
GPU: Intel HD Graphics 5500 <br>
Memory: Original 4GB Samsung 1.35v 1600MHz plus a dual channel with the same memory group, total 8GB<br>
Hard disk: HDD 500G SSD is recommended, otherwise the black apple will be very slow to boot<br>
Sound Card ID: ALC283 Layout ID is `11`<br>
USB: USB`3.0` x 1; USB`2.0` x1 <br>
Wireless network card (Bluetooth and WIFI): BCM943224PCIET2 (`NGFF` transfer card) (replace by yourself), I have set the kernel version number to adapt to Monterey and the old MacOS Bluetooth<br>
## Driver situation
The driver is basically perfect (there is also a little defect and precautions during the installation process, which I tried and made mistakes step by step, and there is a model toss around together)
### Driven hardware
CPU (9-speed variable frequency or turbo frequency)<br>
GPU (HD5500)<br>
Trackpad and keyboard (there are intermittent unavailable on the OC boot page, which has little impact. If you need to operate, I will give the last solution)<br>
The sound card ALC283 layout 11 can be driven, and there is noise in the 3.5mm headphone jack. Speakers and microphones are available. Let's see if 3.5mm noise can be solved in the future. ( Flag +)<br>
USB 3.0 is available (USB2.0 is also available)<br>
Available under the network card MacOS12, AirDrop, Handoff, Shared. ( Unable to test without an iPad) Airtransmission speed is about 20m/s.<br>
Battery: number of battery cycles, plug-in status, power availability can use.(There may be problems with plug-in power detection, which has no impact.)<br>
Camera available through Facetime test<br>
Card reader: it has added  drivers , but there isn't card to test.
Attachment: Fn key operation is available<br>
### Driveable but defective hardware
There is noise in the 3.5mm headphone jack, but the sound card layout of the V3-371 is 11.
### Undrive hardware
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
You can go to https://blog.gatesx.cn/macos-hidpi.html to learn about Hidpi and inject EEID to start hidpi.

### Enter the system prompts abnormal shutdown

At this time, MacOS has actually started. You need to close<br>

## Update logs
### 2022.1.22
Added USB map.
English documents become documents in other languages.
### 2022.1.18
OpenCore version upgraded to 0.7.7
### 2022.1.17
Add a card reader drivers , and the system information is already recognizavle , but there isn't card to test.

---
![Wechat](https://user-images.githubusercontent.com/84220224/149635235-3f295841-d2cf-4579-b2a7-00b5345ff77e.jpg)
![Alipay](https://user-images.githubusercontent.com/84220224/149635237-1d548a3f-12c8-4c4b-81a8-08b455b9801f.jpg)
