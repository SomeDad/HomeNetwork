# Home Network
A small piece about setting up my first home network. At the time of creating this repository I was / am very new to IT and CyberSecurity, so bear with me if some of my terminology is completely incorrect. I aim to keep my updates as they were so I can see my knowledge and understanding increase over time. 

**07/11/2021** - Initially I was going to create my home Network with a RAID 0 setup for NAS storage, with the purpose of having a safe space to securely save important files and photo's.

After a bit of research and speaking to a few people, I've decided that I will most likely set up the Network as a ZFS file system. Next step is to figure out what I will need to have / buy to set this up properly.

**19/01/2022** - I ended up buying a Synology DS920+ (4 bay NAS) and setting that up with a SHR1 setup (Raid 5) for my NAS, so that I can maximise space but have 1 disc still fail. The setup was incredibly easy to do, and the UI / phone application make it very user friendly. 

I bought and have received a J4125 NUC (8gb RAM / 128gb SSD) with Pfsense pre-installed from AliExpress. I am going to use this as a first line of defence, the first thing the internet will hit is the Pfsense NUC before anything else in the house. I have done the initial Pfsense setup on the NUC, but am yet to physically set it up in place. When I've put it in place I'll set up my LAN into different VLAN's and different WiFi channels for home / guest / IoT. 

The next step for me will then be setting up my HomeLab. I am lucky that I have a friend that I can borrow some server-grade hardware to do so, I just need to get myself a cheap server cabinet / rack. I have still yet to decide how I'd like to set up the HomeLab, whether I would set it up with a traditional OS and run some VM's for attack / defence and practicing programs, or whether I would set it up with Dockers to make it easier to run containers like Pi-Hole (Network Ad-Blocker), etc. as well as running some VM's. 

**30/01/2022** - I found some spare time between study to set up the Pfsense NUC, after some trial and error it's all working perfectly. Initially I hadn't changed my router to AP mode so it was also trying to be the DHCP server as well as the Pfsense, easy fix. I've set up 3 VLANS at this stage, home, lab and IOT; all with different rules and permissions. 

I've had a bit of a look through the Pfsense settings and the packages I could test out. I am going to set up pfBlocker (ad blocker) and WireGuard (VPN) at this stage, and when I have the HomeLab set up with dockers I am going to run a Pi-Hole and a different VPN. 
