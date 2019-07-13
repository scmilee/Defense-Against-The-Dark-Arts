# Week 3- Malware Defense

## Ideas

This week was centered around Malware, Attack vectors for infection and how to defend against those vectors. We got to use Yara more in depth and were introduced to a new tool Cuckoo in the labs this week. For both defense and attack vectors, they can be broken down into four main events:
 - First Contact
 - Local Execution
 - Establish Presence
 - Malicious Activity/ Establish persistence

#### Attack Vectors:
 - **First Contact**- 
 - **Local Execution**-
 - **Establish Presence**-
 - **Malicious Activity/ Establish persistence**-

#### Defense Against Previous Vectors:
 - **First Contact**- 
 - **Local Execution**- 
 - **Establish Presence**-
 - **Malicious Activity/ Establish persistence**- 

#### Anti-Malware Characteristics
Expanding on the procedures element above is the volatility grade of the information, and the order of which it should be collected. This order is from RFC-3227 which is a guideline for evidence collection:
`system memory -> temp files -> process table -> routing information -> disc aquisition -> remote logging data -> physical configurations -> backups`

The first four steps of evidence collection should/ can only be done during a live-investigation, while the other 4 steps can be done post mortem. 

#### Tools

- **Cuckoo**- is an open source automated malware analyses tool that oulines file behavior and charateristics. It executes files in a realistic environment/sandbox and records everything that happens including API calls and network traffic. 

![cheat sheet](images/kol.jpg)

- **Yara**- a Regex matcher on steroids. It is primarily used for the identification and classification of malware samples using rules created by a forensic investigator.Below is an image showing what is displayed when Yara finds a file that matches a rule set / signature.

![Yara Ouput](images/yarasig.png)

Cuckoo was definitely the star of the show this week in my opinion, so much so that I went out of my way to play with it a little bit more on my own free time. It integrates perfectly with both Yara and Volatility, which makes things like memory analyses a breeze. And in a similar fashion to Linux, it's super modular and a bit like Lego, you can make your own custom analyses sandbox with parts available on github/sourceforge etc.

## Fun Facts Learned
- Yara can take fairly complex logic and use things called wildcards to get around random byte/string fillers.
- Most of the time when developing Anti-Malware systems you have to be looking for patterns across malware, because by the time you finish writing a tool for current malicious software, there's already 5 more programs to take its place. So you need to be able to anticipate what the bad actors are going to create next.
- Windows autorun/startup program runner is absolutely massive and is a great hiding place to put some maleware to keep it persistent. 
