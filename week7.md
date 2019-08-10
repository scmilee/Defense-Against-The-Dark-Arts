

# Week 7 Web Security

## Ideas

This week we guest speaker Cedric Cochin give us a talk about the inner workings of web security. Cedric is a former white-hat hacker, penetration tester and currently work at Mcafee as a vulnerability automation engineer. Given the massive field that is web-security there was a lot that was covered, but it can mainly be broken down into two categories, User level attacks and Browser level attacks.

### User Level Attacks:
User level attacks are attacks that focus not on network vulnerabilities, not on software vulnerabilities, but instead focus on the end users themselves as a means of exploitation. User level attacks use users laziness, impatience and clickability against them to launch a variety of attacks that usually all end up as a horrible experience for the user. Below is a very short list of the possible attacks a user could expect during their time on the web. 

**Phishing**- Phishing attacks, much like normal fishing, use bait to lure in potential targets, then trap them in a unfavorable scenario. Phishing uses websites and links that look like the real-deal but instead scrape user information or provide malicious downloads. 

**SEO Poisoning**- SEO poisoning is heavily focused around Google Trends and aims to serve up malicious content for the newest trends on the web. Google is likely the safest place to browse but the occasional poisoning can still turn up.
**Social Media**- Social media profiles can be incredibly dangerous due to the fact that you can't really know who you're talking to unless you've met them in person. And if you do end up adding random people from the internet, they could potentially be skimming data from your profile. Data like: 
- projects you're working on at work
- co-workers 
- whiteboards
- your schedule
- your interests 
- important dates to you

**Fake AV**- Fake AV or fake anti-virus are programs that mimic real  AV programs but either perform malicious activities or exploit their users by producing fake infection results leading users to paying for no real service.

**Malvertising**- Malvertising as complex as it is, can be boiled down into a simple concept. Find a target -> tailor ads to fit that target -> serve those ads on their favorite sites -> perform malicous activity on the redirection. 

### Defenses
Users are most commonly referred to as the weakest link in any security set-up, so as a result your system is only as secure as your actions. There have been improvements to the user side of security but the human firewall is far from perfect and will likely always be a step behind the bad guys. 

### Browser Level Attacks:
Defenses for network security come in all shapes and sizes and require varying amounts of configuration. This configuration requirement is often the greatest barrier for a company to use a piece of software. 

**MitM**- A whitelist is a list of activities and actions you expect a system to produce. This gives the defender a massive advantage because you can be incredibly granular with the traffic you let through a policy, which as a result limits the attack surface available to an attacker. A positive policy is usually implemented in one of these three systems:
- firewalls
- internet/web gateways
- email gateways
The only real downside to a whitelist is that it might detect bad actors but it cannot identify them.
 
**MiB**- HoneyNets are very similar to the popularized term of honey-pots. They are bait that's left out for an attacker to fall into and be trapped.The system can often use delayed response times and a maze-like network structure to try and absorb as much of the attackers time as possible. During this wasted time, other systems and sys-admins can evaluate the threat and act accordingly. Unfortunately, this system is very config-heavy and as a result, not many companies implement honeynets. 

**DNS Hijacking**: Intrusion prevention/detection systems are a lot like anti-virus systems in terms of evaluating threats because they use signature matching and hashes. IPS's are incredibly fast and provide information about an attack unlike a firewall. The only downside is that they can not help with zero-day attacks and that they can provide false positives. 

**SQL injection**: Quarantines are remarkably similar to honeypots, except they are even more restrictive in the activities of a host. Quarantines are exceptionally useful for analyzing behavior and analyzing traffic before letting it in to your internal network. A quaratine can cause issues on a network if a good actor gets blacklisted , causing them to retry through various methods resulting in a lockout on many entry-points. 


## Alexa
This is my take on the Robustness Principle and how it manages to keep up with modern day practices and teachings.
![cheat sheet](images/alexa.PNG)

## IPVoid
This is an example firewall policy document.
![Yara Ouput](images/ipvoid.PNG)

## PhantomJS
This is my take on the Robustness Principle and how it manages to keep up with modern day practices and teachings.
![cheat sheet](images/phatomjs.png)

## Burp-Suite
This is an example firewall policy document.
![Yara Ouput](images/burp.png)

## Fun Facts Learned
- Browser based  exploits and malware do not need to be web-centric, using the browser is just a means to an end.
- Malware authors are starting to target developers more often due to their increased exposure to end-users.
- At the time of making our lectures, Jimmy Kimmels searches were the most dangerous (result wise).
