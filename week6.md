
# Week 6- Network Security

## Ideas

This week we had the pleasure of having two guest speakers from Intel to talk to us about internet security, their names were Ram Venugopalan and Geoffry Cooper. A lot was covered this week from principles to types of threats and protection strategies to defend against them. First we'll discuss the attacks then how to defend against them, and then go over a firewall policy example.

### Threats:
Threats on the internet are everywhere, but we can split them into two main catagories. The first are threats that are on the internet, these threats include worms, botnets, resource theft and recon/espionage. The second catagory is threats that are from the internet, and this includes things like DDOS attacks, MitM attacks, Morris worms, Stack Overflow etc. Given the sheer magnitude of threats on/from the internet I'll be going my two favorite from each sector.

**DDOS**- a process is a running piece of software, and a thread is the smallest piece of execution for a process. Threads from the same parent process all share the same virtual address parents, but processes do not. Processes are shceduled to run by the cpu through a variety of different methods from round-robin scheduling to lottery-scheduling.

**MitM**- User memory is available to processes running in user space, and in turn is very restricted in what it can do in terms of execution, reading other memory etc. On the other hand kernel memory has access to all of the devices memory and hardware, making it quite a big deal if it's every compromised.

**Arp Cache Poisoning**- is at its very core, just intercepting or "hooking" into function calls, module loading,sys-calls, hardware events(keystrokes, mouse movements) etc.


### Defenses:
**RootKits**- Rootkits are pieces of malware that have the over-arching goal of conealing themselves from the users and system of the device, while also having root permissions in a system. They are most commonly found on Windows-32 Bit devices due to complications when trying to infect 64 bit systems. A rootkit infects usually through one of these three ways:
- exploits in the kernel.
- bypassing or stealing valid driver signature checks.
- adding itself to the bootpath.
 
**BootKits**- Bootkits are nearly identical in terms of functionality when compared to a rootkit, but their main difference is the fact that they add themselves to the master boot record so it can survive reboots. Once a device is infected with a bootkit it can be incredibly difficult to remove, since a bootkit has access to the kernel and boot process.

#### Rootkit Types
- **User-mode rootkit**: The easiest to detect of all the rootkits, but still menacing. A usermode rootkit has admin privileges granting it the ability to hide processes, files, ports etc. But since it does not have kernel access it is much more likely to be detected by a hypervisor layer of security.
- **Kernel-mode rootkit**: Kernel mode rootkits are exactly like their user mode counterparts, except they have access to the kernel and in turn are far more difficult to detect. 
- **Hybrid rootkit**: A hybrid rootkit, is simply a blend between a kernel rootkit and a user rootkit and is the most common type of rootkit for malicious activity.
- **Firmware rootkit**: As with the other three, the name really gives away what the rootkit does/ where it lives. A firmware rootkit plants itself inside of firmware, so that on system restart it will always be there. And like the kernel mode rootkit, its very difficult to detect unless using secure boot.

## Robustness Analysis

![cheat sheet](images/robust.PNG)

## FireWall policy document

![Yara Ouput](images/firewall.PNG)

## Fun Facts Learned
- Companies serve out/ compute reputation for various actors, IE: files, IP's, URLs.
- Firewalls are the largest single segment of Network Security companies income becuase they can a lot in a tiny package.
- Big data is where the magnitude of the data becomes so big that it affects the value of the data itself. 
