# Defcon-23-presentation
USB Attack to Decrypt Wi-Fi Communications

I gave a presentation 8/7/15 on two variants of rubber ducky payloads that decrypt wireless ssl traffic. 
The first variant uses the ducky firmware (keyboard only)
The second variant uses the twin duck firmware (keyboard and mass storage)

****Payload 1 using Keyboard only “trusted-root.txt”******
Before the attack will work, you will need to setup your MITM listener. I’ve included the files I used for reference and there are lots of walkthroughs online. The payload will need to be adjusted to reflect what SSID your AP will be using. 
After the MITM AP and proxy are setup, you will need to export the signing certificate and convert to base64 encoding. I’ve listed commands to do that in the attached presentation slides. 
If you are using the “trusted-root” variant, you will need to update the syntax to use your exported certificate instead of the one I used. 
That should be all you need to make the keyboard only payload work. 
*Note you may need to adjust timers or acknowledge pops differently than what my test machine needed. This version will work on IE and Chrome but not Firefox.

****Payload 2 using Keyboard and USB Mass Storage “Twin-trust-root.txt”*****
Like the previous payload, you will need to setup a MITM listener and export a certificate. 
For this payload you will need to add the certificate to your own copy of Firefox. Then you will need to copy your Firefox key3 and cert8 files. I’ve included slides in the presentation to show you where they files are located. I’ve also included a slide in the presentation shows what the file hierarchy looks like in the ca directory of the DUCKY drive. 
*Note you may need to adjust timers or acknowledge pop ups differently than what my test machine needed. This version will work on IE, Chrome and Firefox.

I’ve tried to acknowledge other people’s code I used, but if I missed someone, let me know. Give it a shot and I’ll try to help get it working if you have any questions.
