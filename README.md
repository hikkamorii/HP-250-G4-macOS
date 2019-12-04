So I've decided to install macOS Mojave on my laptop. I wasn't hoping for much success, but I've managed to create somewhat working config. There is still room for improvement, but for now I'm happy, and I'm glad to share my success story with you. 

I also want to point out that many people who've tried hackintoshing this laptop had Broadwell (5th gen) CPUs. Mine also had dedicated GPU (see *specs*)

&nbsp;

Specs
======
**CPU:** Intel Core i3 4005U
**iGPU:** Intel HD4400
**dGPU:** AMD Radeon R5 330M
**Network:** Realtek RTL8106E *(10/100😔)*
&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Broadcom BCM43xx series (Don't really care, see *problems*)
**RAM:** 4GB DDR3L *(Hopefully I'm gonna upgrade it soon)*
**Audio:** Realtek ALC286
**BIOS:** Insyde UEFI, vF.24
**Board:** HP 80C4
**HDD:** Toshiba MQ01ABF050 *(Note: Don't install macOS on 5400rpm drive, bad idea.)*

&nbsp;

What's working
============
* Wake by opening lid.
* Brightness control.
* CPU Power Management.
* Metal.
* SD Card reader.

&nbsp;

Problems
=======
* Laptop goes to sleep only when on battery. Instant wake when on AC. Can be put to sleep on battery and then plugged on to charge.
* Wi-Fi (and Bluetooth) obviously.
* No HDMI audio. I use AirPlay most of the times so I don't really care.
* No sleep by closing lid.

&nbsp;

Untested
=======
* VGA. Probably not working.
* Long-term sleep. Tested for about 30 hours.

&nbsp;

List of Patches and kexts
==================
* RehabMan's Clover Config for HD4400
* Descrete GPU Disabler Hotpath (SSDT-DDGPU)
* GPRW Hotpatch (SSDT-GPRW)
* Brightness Hotpath (SSDT-PNLF)(Note comments*(See PNLF.png)* and don't forget kexts)
* [Mieze's RTL8100 Kext](https://www.insanelymac.com/forum/files/file/259-realtekrtl8100-binary/)
* ACPIBatteryManager
* AppleBacklightFixup
* EnableLidWake
* FakeSMC
* Lilu
* VodooHDA
* VoodooPS2Controller
* WhateverGreen

[All of the stuff listed above can be found there.](https://github.com/RehabMan/OS-X-Clover-Laptop-Config)

&nbsp;

Thoughts
=========
Overall, I'm pretty happy I did that, and I'm glad this experience was more successfull then my previous attempts. I'm still a noob when it comes to ACPI patching, but I got some experience from that.

If you have same laptop as me, feel free to download Clover files *(Clover.zip)*

&nbsp;

Happy hackintoshing! 💙

&nbps;