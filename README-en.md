# Acer-v3-371-547H-OC-EFI
English | [简体中文](./README.md)<br>
## Hardware configuration
For detailed configuration, please check the official website database: https://www.acer.com/datasheets/2014/4876/V3-371/NX.MPFCN.015.html<br>
Hard disk: Samsung 870evo 250GB <br>
Wireless network card (Bluetooth and WIFI): BCM943224PCIET2 (`NGFF` transfer card) (replace by yourself), I have set the kernel version number to adapt to Monterey and the old MacOS Bluetooth<br>
## Driver situation
The driver is basically perfect (there is also a little defect and precautions during the installation process, which I tried and made mistakes step by step, and there is a model toss around together)
### Driven hardware
CPU (9-speed variable frequency or turbo frequency)<br>
GPU (Intel HD Graphics 5500) <br>
Trackpad and keyboard (intermittently unavailable on the OC boot page) <br>
The sound card `ALC283' layout 11 can be driven, and there is noise in the 3.5mm headphone jack. Speakers and microphones are available. Let's see if 3.5mm noise can be solved in the future. ( Flag +) <br>
USB can use <br>
Available under the network card MacOS12, AirTransmission, Handoff, Shared Clipboard. ( Changing the system model may be able to achieve on-board) Air transmission speed of about 20m/s. <br>
Battery: number of battery cycles, plug-in status, power availability can use.(There may be problems with plug-in power detection, which has no impact.)<br>
Camera available through Facetime test<br>
Card reader: it has added  drivers , but there isn't card to test.
Attachment: Fn key operation is available.(Adjust the volume · brightness)<br>
### Imperfect hardware
There is noise in the 3.5mm headphone jack, but the sound card layout of the V3-371 is 11.
### Known problems
There is something wrong with hibernation (screen saver is available, I put it for 3 hours)
## Considerations
These solutions are only suitable for identical models.
### Pre-installation considerations
1. Update the logic board Bios<br>
https://www.acer.com/ac/en/US/content/support-product/5487?b=1 <br>
Download the latest version of Bios and update it.<br>
2. Modify logic board settings<br>
Change Boot-Boot Mode to `UEFI` (necessary)
Change Boot-Secure Boot to `Diskabled` (set the Bios password if you can't modify it first) (necessary)
Change Main-F12 Boot menu to `Enabled` to facilitate the temporary modification of boot items. (Unnecessary)
### The page keyboard and mouse are unavailable when booting OC
You can hold down the down button and plug and unplug a responsive USB device (U disk, mouse, iPhone) while booting the interface
### Black screen after running the code
In fact, MacOS has been started at this point, you need to close the screen and open it again (don't close it for too long or the system will sleep and restart). If the backlight is dark, click the keyboard (any key). <br>
I have found the solution (squatting right), which is to turn on hidpi and inject eeid (when I turned on the external display, I pressed the wrong result and solved the problem). <br>
The following items are available:<br>
https://github.com/xzhih/one-key-hidpi
### Entering the system prompts abnormal shutdown
There is no solution to this problem at the moment, it does not affect the system, just click Cancel. <br>
## Changelog
### 2022.1.22
Custom USB.
Chinese document changed to README.md (main document)
### 2022.1.18
OpenCore version upgraded to 0.7.7 (stable channel)
### 2022.1.17
Added card reader driver, system information panel information can be read, but no CD card for me to test.

## Appreciate
![Wechat](https://user-images.githubusercontent.com/84220224/149635235-3f295841-d2cf-4579-b2a7-00b5345ff77e.jpg)
![Alipay](https://user-images.githubusercontent.com/84220224/149635237-1d548a3f-12c8-4c4b-81a8-08b455b9801f.jpg)
