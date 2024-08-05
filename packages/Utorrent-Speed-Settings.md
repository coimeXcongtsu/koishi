It would be nice if when you paused the laser that you could change the speed/power without starting the job all over again. I realize that there is now an option to change the speed/power in the move tab but that does not reflect in the original file. Keeping track of changes made are difficult and making changes on the fly to get an idea of the settings needed for a particular material is difficult before fine tuning using a target. Unless someone has a better way that they would like to share I think this would be a good idea to include in the next version.
 
**Download File » [https://eromdesre.blogspot.com/?d=2A0SzK](https://eromdesre.blogspot.com/?d=2A0SzK)**


 
Many of the things that you can change in LightBurn, like the dither settings, DPI, etc, make very drastic changes to the content of the GCode, so they would not be at all simple to update on the fly.
 
What most people do is use a generator or a set of samples with different settings to run test swatches, and use those to get the initial starting point set before doing the fine tuning. This is a good one: Lightburn PowerScale Generators - O2 Creative
 
I recently bought a atomstack x7pro. I am currently trying to change it back as I said previously the max speed was 100. It changed to 6000 when I setup the rotary roller and and has been like that for the past 3 days however I did adjust the machine settings when setting up the rotary roller but I did not change the speed settings, I turned off Homeing cycle, soft limits and the hard limits once I was done I changed them back clicked write. Could this be what affected the speed settings?

My goal is to achieve the quality of my 0.2mm nozzle prints on my Prusa mk3 but with the new X1 carbon. My main issue is the excess blobs of filament in between the letters and at the edges of the letters and logos.
 
For Color prints increasing prime tower volume by 2x default helps. In your speed settings lower acceleration. If you use model parts for colour you can get the printer to slow down right after changing colour. Put a draft shield around your model for colour change, otherwise the prime tower mess can destroy your print, and speed for prime tower is way too fast and no speed overrides atm
 
Quality and speed is a trade-off. THIS guide gives a lot of tips on different print settings and values, and how to adjust for different issues which can affect the final quality of a model. I think nozzle temperatures are also covered briefly under the section on stringing.
 
I would suggest to start with those settings and work from there. Basically, the faster you print, the hotter the nozzle temp must be, and vice versa. You can actually print PLA very cool, around 190 C, but you would need to print very slow in order for this to work. Printing cooler can help with the quality of overhangs and reduces stringing, but you are not able to extrude as much material through the nozzle the cooler you go, so it is a trade-off.
 
Also, as far as layer height goes, anything between 60-100 microns looks "high quality" to me. Printing >60 microns usually will take much, much longer and can be difficult as very thin layers will cool down more quickly, so could actually warp (even with PLA). Unless it's very important to your purposes for some reason, printing >60 micron layer heights is not worth it in my opinion. But of course, beauty is in the eye of the beholder.
 
I have been using my UMO+ for about 2 weeks already, and from what I experienced so far, different filaments might require different settings, even from the same brand (I have used silver and black ultimaker pla).
 
I agree with @Labern, I just got some Leaf green Colorfabb filament, and its much meltier than the red i had, and also the black. Its the same brand, but i have to print much cooler than normal or else it jams or i get poor quality. And also 50mm/s is too fast to preserve small details without patterning on the sides as I call it. The faster you print the more mechanical lines you see on the outside like stepper motor patterns and vibration patterns. for what i call high quality you cant really go much above 30-35mms in my personal experience, i have always printed at 35 at 0.06 and 208, but noticed improvement at 30 205. Again there are so many factors involved, it boils down to trial and error. I used to always ask this question, but again not everyones printer is the same and temperature sensors vary. Also overhangs are best printed with manual support designs unless they are simple and flat underneath or else they'll look lame.
 
You need to match the speed (RPM) of the router to the feed (movement rate of the machine) to get a chipload suitable to your material and endmill and which your machine is rigid enough to ensure will not result in chatter.
 
I updated the Dewalt spreadsheet with the Mikita Speed settings. Again, the main takeaway is that these routers spin way faster than you need for the types of tooling we commonly use. So using the lowest speed setting is always a good place to start.
 
If Makita made a statement at all, its based on the expectation that the use is the original purpose, palm routing. The cutting forces are much smaller on a CNC router and cutting forces is what matter.
Also air cooling is less at low RPM.
 
I just got a box of Polymaker PolyMax PETG. Among usual temperature parameters, it also lists nozzle speed to be set between 30 and 50 mm/s. Not sure how important it is to follow (still experimenting with this filament), but let assume it is. PrusaSlicer only supports setting maximum volumetric speed. Fair enought, easy to convert, nozzle speed \* nozzle width \* layer height. However, I'd need to reset it when printing at different layer heights. Is there any way to tell PrusaSlicer maximum nozzle speed, and let it calculate maximum volumetric speed?
 
I would guess you are right there. As many slicers don't know the max volumetric flow setting it can make sense for filament manufacturers to go with nozzle speeds assuming typical nozzle sizes and layer heights. If you want to convert it to a max volumetric flow I would simply assume a 0.4mm nozzle and 0.2mm layer heights. From then onward you can quickly change the setting with a single change of a number.
 
In the filament settings for each filament profile you can configure a max volumetric rate. If you look at a PLA and PETG profile you will see the difference, the pla is around 11 iirc and the pet one is set to 8. There is another volumetric rate in Print Settings too and Slicer will use the lower of the 2 so setting a more realistic rate for a particular filament is respected if you remember to select it. The volumetric will act as a brake on the print speeds which is why I think some of Prusa's default profiles have very fast infill rates of 200 mms. The max volumetric will slow it down where needed.
 
I just got a box of Polymaker PolyMax PETG. Among usual temperature parameters, it also lists nozzle speed to be set between 30 and 50 mm/s. Not sure how important it is to follow (still experimenting with this filament), but let assume it is.**PrusaSlicer only supports setting maximum volumetric speed.** Fair enought, easy to convert, nozzle speed \* nozzle width \* layer height. However, I'd need to reset it when printing at different layer heights. Is there any way to tell PrusaSlicer maximum nozzle speed, and let it calculate maximum volumetric speed?
 
Said that, it would be nice if "effective speed" would be displayed as appropriate in various parts of the UI. E.g. if volumetric limit effectively also limits linear speed in some other setting, or vice versa, it would be nice it was visible in the UI.
 
Yes, that where the speeds are adjusted but if you have a filament that requires a different speed than the default print profile, you have to create a custom filament profile AND a print profile. I'm running into the same problem with the Matter Hacker Build PET filament I recently tried out. I set the temps in the filament profile and saved that in it's own profile. That makes perfect sense. However, I have discovered that I end up with blobbing and failed prints if I don't knock 10mm/s off the support and infill feed rates which is set in the print profile. I would think those speeds would be filament dependent rather than print dependent. I'll math my way to the speeds that work with the volumetric rate but that's a hack.
 
This page in Filament settings shows the gruesome details: with the setting of 15 mm3/s, infill will exceed the setting and suffer enforced slowdowns (infill requires 16.28 mm3/s as set in Print Settings).
 
But there is another issue the mfg needs to suggest: and that is the flow and cure characteristics. Some filaments will have odd surface characteristics if printed too fast; i.e., even though the material will flow at 80 mm/s, the sheen will be destroyed unless printed slower than 20 mm/s.
 
I've done calcs for PLA and PETG determining maximum speeds to maintain MVS at a given layer height and extrusion width. I think you'll have problems with a single filament profile simply because your effective volumetric rate will depend on so many factors under the **Print Settings** tab. It's the same issue all over again.
 
Raise 3D's ideaMaker slicer has an interesting approach in allowing a filament profile to over-ride any other slicer setting. I wish there was a way to de-link settings from the fixed tabs and let us define free-form profiles that can contain any valid slicer setting. You can do this from the command line (well, it's broken in current PS versions) by loading progressively more specific profiles.
 a2f82b0cb4
 
