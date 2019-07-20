
# Week 4- Software Vulnerabilities & Common Exploits

## Ideas

This week focuses on the topic of Software Vulnerabilities and common exploits for them on  modern computers, this is almost the exact opposite of last weeks defense strategies. The specific exploits covered are for windows systems, although there are similar exploits for other operating systems. Our speaker Brad Antoniewicz works as a White hat hacker at Mcafee and really helped dispel a lot of the myths I had let myself believe about hacking. 

#### Primary Hacking Paths:
 - **Software Vulnerability**- This is where both of our Labs this week live. It's exploiting a programmers logic for your own good and it can happen in a variety of ways from not sanitizing your inputs from a client to something more complex like memory corruption. Either way this is caused by human error and lack of consideration for exploitation. 
 - **Exploiting Misconfigurations**- Hacks under this category often occur because honestly life is usually a lot easier with relaxed security protocols. Things like 2 factor authentication, firewalls, encryption at rest, etc. all cause your life to move slower and from a business perspective that means less money. So more often than not you have folks skipping this type of stuff in favor of nothing, or they just simply don't configure it right so the benefit is lost anyways. 

### General Process



#### Memory Corruption:
The biggest issue with defending the general public against known malware attack vectors is knowledge and understanding. If everyone were to have an IPS, awesome Firewall, 2-factor auth, HIPS etc then there would be a drastic drop in infections. But that's not the case, so instead we're stuck with Malware being a big deal.

 - **Buffer Overflow**- A big way to reduce exposure to malware is to only visit reputable sites for content (ignoring the watering hole vector). But beyond just staying safe on the internet and epoxying your USB ports, you can get an anti-spam systema, educate yourself on the attack vectors and filter out any scripts from sites.
 - **Use After Free**- First and foremost, get a anti-virus/anti-malware scanner or IPS on your computer! Another good defense for local execution is 2 factor authentication. 

#### Tools

- **WinDBG/WinBAG**- is an open source automated malware analyses tool that oulines file behavior and charateristics. It executes files in a realistic environment/sandbox and records everything that happens including API calls and network traffic. 

![cheat sheet](images/winbdg.png)

- **FS exploit me**- a Regex matcher on steroids. It is primarily used for the identification and classification of malware samples using rules created by a forensic investigator.Below is an image showing what is displayed when Yara finds a file that matches a rule set / signature.

![Yara Ouput](images/fseploit.png)

- **Metasploit**- a Regex matcher on steroids. It is primarily used for the identification and classification of malware samples using rules created by a forensic investigator.Below is an image showing what is displayed when Yara finds a file that matches a rule set / signature.

![Yara Ouput](images/metasploit.png)

Cuckoo was definitely the star of the show this week in my opinion, so much so that I went out of my way to play with it a little bit more on my own free time. It integrates perfectly with both Yara and Volatility, which makes things like memory analysis a breeze. And in a similar fashion to Linux, it's super modular and a bit like Lego, you can make your own custom analyses sandbox with parts available on github/sourceforge etc.

## Fun Facts Learned
- Most major vulnerabilities in today's world are triggered by Javascript and as a result is primarily performed through a web-browser.
- The vulnerability/exploits of today are vastly different(yet strikingly similar) from those years ago. Where in the past perimeter attacks were more common, nowadays companies have their perimeters guarded quite strongly, so bad actors are forced to resort to a honey-pot type strategy.
- EAX register in windows operating systems hold the return values of a function call. 
