# Week 3- Malware Defense

## Ideas

This week was centered around Malware, Attack vectors/processes for infection and how to defend against those vectors. We got to use Yara more in depth and were introduced to a new tool Cuckoo in the labs this week. For both defense and attack vectors, they can be broken down into four main events:
 - First Contact
 - Local Execution
 - Establish Presence/Persistence
 - Malicious Activity/ Establish 

#### Attack Vectors/ Infection Process:
 - **First Contact**- This is where the rubber meets the road so to speak, it's where a user is first exposed to Malware. This can be done a variety of ways from instant messaging to a watering hole poisoning. My favorite one discussed was physical access as it is usually the most overlooked of all the ways you can get infected, and popular cases like Stuxnet have shown the importance of it.
 - **Local Execution**- This is what I think would be the hardest part about making Malware. It's getting the user to run the stuff in the first place. The main two means of doing this are through exploitation of existing systems like Windows autron feature, and social engineering. 
 - **Establish Presence/Persistence**- Once the malware has infected your computer, the author of the code has two choices pretty much on what to do in terms of keeping the user non the wiser. The first is to blend in, now this can be done many ways but the most common is to use filenames that are similar to system files and change their mac times to blend in. The second is to hide in the form of a bootkit or a rootkit and just run at startup behind the OS.
 - **Malicious Activity**- This is where hackers make their money and it can be something simple like keylogging where they're just waiting for you to type in your passwords. Or it could be scanning your computer for important files like banking information/SSN/Passports etc. Then of course the malware has to get the data off your computer so it's likely to connect to another machine or e-mail out all of the data it finds.

#### Defense Against Previous Vectors:
The biggest issue with defending the general public against known malware attack vectors is knowledge and understanding. If everyone were to have an IPS, awesome Firewall, 2-factor auth, HIPS etc then there would be a drastic drop in infections. But that's not the case, so instead we're stuck with Malware being a big deal.

 - **First Contact**- A big way to reduce exposure to malware is to only visit reputable sites for content (ignoring the watering hole vector). But beyond just staying safe on the internet and epoxying your USB ports, you can get an anti-spam systema, educate yourself on the attack vectors and filter out any scripts from sites.
 - **Local Execution**- First and foremost, get a anti-virus/anti-malware scanner or IPS on your computer! Another good defense for local execution is 2 factor authentication. 
 - **Establish Presence/Persistence**- Same as above, using a good IPS/HIPS and a anti-malware scanner is your best bet.
 - **Malicious Activity**- Data loss prevention is the name of the game. Montior network traffic to try and catch the baddies exporting your data.

#### Anti-Malware Characteristics
Most anti-malware software has a combination of the following characteristics:
- OAS/ODS file scanning and MD5 hash matching/filtering system.
- Registry/Cookies scanning system.
- Cloud scan, where you can export any suspicious files to be analyzed in the cloud by the software providers computers/technicians.
- Memory scan making sure everything in your memory should be there.
- Script scanning for suspicious sites.
- Heuristics & Logging.

#### Tools

- **Cuckoo**- is an open source automated malware analyses tool that oulines file behavior and charateristics. It executes files in a realistic environment/sandbox and records everything that happens including API calls and network traffic. 

![cheat sheet](images/cuck.png)

- **Yara**- a Regex matcher on steroids. It is primarily used for the identification and classification of malware samples using rules created by a forensic investigator.Below is an image showing what is displayed when Yara finds a file that matches a rule set / signature.

![Yara Ouput](images/yara.png)

Cuckoo was definitely the star of the show this week in my opinion, so much so that I went out of my way to play with it a little bit more on my own free time. It integrates perfectly with both Yara and Volatility, which makes things like memory analyses a breeze. And in a similar fashion to Linux, it's super modular and a bit like Lego, you can make your own custom analyses sandbox with parts available on github/sourceforge etc.

## Fun Facts Learned
- Yara can take fairly complex logic and use things called wildcards to get around random byte/string fillers.
- Most of the time when developing Anti-Malware systems you have to be looking for patterns across malware, because by the time you finish writing a tool for current malicious software, there's already 5 more programs to take its place. So you need to be able to anticipate what the bad actors are going to create next.
- Windows autorun/startup program runner is absolutely massive and is a great hiding place to put some maleware to keep it persistent. 
