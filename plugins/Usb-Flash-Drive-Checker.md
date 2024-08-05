
 
Issues often arise with cheap flash drives made with lower quality controls, as is the usual case with products made in China. With that said, **USB Flash Drive Tester** is a useful software utility which can reduce the headache of faulty devices.As the name suggests, Flash Drive Tester is a utility which will run through some tests on connected USB flash devices such as SD Cards, Memory Cards and USB Flash Drives. It will perform **read and write tests** on connected media.Running Flash Drive Tester is simple. Users are presented with a drop-down list of detected USB devices and from there, you can select the test type and commence the test.The text panel of this utility provides a log of actions taken while the bottom of the interface provides graphical outputs such as current operation, last error, error count thus far and a device map which displays status of the device with color coding.Overall, if you want to test some of your storage media for errors that can be recovered or not, try **Flash Drive Tester** to see whether any of your storage media requires replacement.Compatibility and LicenseFlash Drive Tester is provided under a freeware license on Windows from disk management with no restrictions on usage. Download and installation of this PC software is free and 1.14.0.1 is the latest version last time we checked.
 
**DOWNLOAD ··· [https://eromdesre.blogspot.com/?d=2A0SDQ](https://eromdesre.blogspot.com/?d=2A0SDQ)**


 
**USB Flash Drive Tester** (**Download**v1.14)****- Flash card/drive tester allows testing of any removable media including SD, CF, USB flash drives for bad or unstable sectors. Especially useful for testing for fake sizes often seen on low quality USB flash drives.
 
**Netflow Traffic Generator**(**Download**v1.1) - Allows to generate large amount of NetFlow packets for protocol versions: 5, 6, 7, 8, 9 as if they were coming from real routers or switches. Windows GUI provides control for every single parameter of the NetFlow packets. Randomizaton of flow data. Support for multiple collectors. Simulation for up to 5000 routers.
 
**Packet Ge** **nerator. Bandwidth, Delay and Jitter Tester**(**Download**v1.0) - This application allows network engineers to measure real network throughtput, measure delays and jitter for traffic between two IPs. Application consists of Sender and Receiver. Sender sends UDP packets to IP address where Receiver is running. Receiver calculates traffic statistics such actual throughput, average delays, mean jitter and absolute mean jitter, lost and out of order packets. Nice tool to stress test a router, server or find out if there are any bottlenecks in your network.
 
**Flash Drive Image Creator**(**Download**v1.0) - This product helps to create image file of any removable flash drive such as USB flash drive or SD/CF flash card. Image file created by this tool can be used with any of the duplicators manufactured by Virtual Console as source of duplicated data.
 
**Flash Drive Image Writer**(**Download**v1.0) - This application is essentially a software based (PC based) USB duplication tool that takes previously created image file and writes it to multiple USB flash drives.

IMO best option is to look behind info that is easily faked (like the printing on the casing). Goal of the faker is to make (quick) money and often one way to do this is by keeping production costs down. Second way to quick money is pretend you're an A brand and thirdly lie about things like capacity: claim more than there's actually in there, higher capacity = higher price.
 
Saving on production costs may result in visually detectable anomalies, sloppy printing for example. Problem is this is easy to tell when you can compare against a genuine drive but harder when you have nothing to compare against.
 
It's relatively easy to have a USB flash drive with say 8GB NAND installed report as a 64GB or 128 GB drive. You can even use such a drive to a degree until you start saving files at LBA addresses > 8 GB, but even then you will not be alarmed until you actually try to open these files!
 
Carefully examine the looks of the USB flash drive. Even if you can not compare to a genuine Sandisk USB flash drive you might be able to spot a fake. In general Sandisk's are nicely finished products, looks for signs of sloppiness.
 
An alternative tool to determine this information is 'ChipGenius' but many copies you can find on the internet are suspicious according to many virus scanners. IOW it's risky to rely on this tool and I'd avoid it.
 
I recently read a lot about fake MicroSD card and USB thumb drives that claim to have a lot of space (even if you ask your computer), while physically offering way less. I recently bought a SanDisk USB drive (128 GB claimed) and want to test its size. It's not bought via ebay or something, but I really want to test the real size before using it productively.
 
I could just copy stuff on it, copy it back and look if the files are okay. I could also automate it with Hashes and stuff. But I hoped there is a more accurate solution. I read that for Windows, H2testw does the trick. Is there an easy way to test this on Ubuntu/Linux? A specialized, well working tool maybe?
 
Update: Just to be clear, the idea is to verify that the size the linux system gets told by the controller is correct (**so no data will be lost**). It's not like I want to see if I get 128 GB instead of 127.3 GB. **I want to test if all data I write will be readable again.** Unfortunately I can only find a few information about this on English tech sites. There are good German sources, though. I'm actually searching for an application like those, but for Ubuntu/Linux: -and-detect-fake-or-counterfeit-usb-flash-drives-bought-from-ebay-with-h2testw/
 
The capacity of usb devices your operating system or unix tools give you, can be wrong. This is fatal, since your OS regulates how much data you can send it to. Send more data than it can really hold, you'll get a data loss. This is a problem. So, why can this happen?
 
You do not need to know the USB-Protocol well to unterstand the problem. Serial Interfaces have the common property, that the client device (the usb drive) will need to tell its own capacity via this serial interface. This means that the client device needs it's own controller with some knowledge about the devices purpose and, in this case, it's capacity. It also decides what is done, when it receives the command to store something. If the controller is programmed that way, it can just ignore the command or overwrite something with the data.
 
What does this mean? Whatever your unix tools tell you about the capacity of the drive: It's what the tools asked the drive, nothing more. This is what h2testw was invented for: It tests the real size with a method explained later on, and compares it to what the drive says. If this is not the same, you may have a data loss, because all your common operations to store data, rely on the information of your operating system, which just asks the controller. Why just ask? Testing needs time and overwrites all data on the drive. So it's natural that an Operating System needs to rely on this information.
 
To check the real capacity like h2testw, you indeed can use dd to write data on the drive, read it again, and see if it's the same you wrote. Totally legit. The nature of hardware and the drive make it more complicated. Consider write-caches for example. You need to ensure that you do not read from the cache. This is just one example of why it is not as easy as it looks. Also think that just writing zeros means a low entropy of information, which can be reconstructed when reading. It's just not that easy in detail. You can still do it manually, of course.
 
But why, when you can automate things? Why to the work? f3 as proposed in my answer below, implements tons of thoughts of many contributors (consider that it kind of extended h2testw) and it also implements several methods with different trade-offs. The developer figured out the tricks of different fake drives (aka counterfeit drives) they had at hand. So, while I understand the theory and the problem (seemingly since the problems are well explained in german tech media, but not in english speaking media), I do not pretend to understand everything, which is why I mentioned it above. It's just the theory I understand, and I'm more of a software guy. But as a student of informatics I understand it well enough to see the problem.
 
Is it possible that he buys stuff he doesn't know is fake? Totally, look at the recent ryzen fakes: -of-fake-ryzen-processors-selling-on-amazon/ , -von-Amazon-Faelschungen-von-AMDs-Ryzen-Prozessoren-im-Umlauf-3772757.html
 
If I loose my presentation in the drive and screw up the presentation, will my trusted supplier go back in time and rescue me? It will probably replace the drive, since the last time-travelling DeLorean was destroyed in 1885.
 
This is ridiculous. I was searching specifically for a similar tool to h2testw that also runs on linux. And yes, that's what I'd "like", helpful answer, so sorry. I had no idea that the english speaking press is not that aware of such issues and was lucky to find something like that later on. This is not a promo, but actually it seems you could use one.
 
There is only one alternative I found, but I think this is even a better one than the original h2testw tool for MS Windows. Fortunately, it is really easy to use, even from command line. There are GUIs available, though. There is also a lot of information about the implementation and the problem with fake drives on the tools website.
 
f3probe is one way to test the drives, not as accurate but faster since it does not write on the whole drive. You can read more about it on the tools website. If you want to be 100% sure, better use the h2testw method. As the developer describes on the website:
 
Finally, thanks to f3probe be