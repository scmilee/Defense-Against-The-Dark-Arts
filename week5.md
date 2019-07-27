
# Week 5- Windows Interals & Kernal Debugging

## Ideas

This week focused on the inner working of windows from boot processes to 32 bit virtual memory layout. When discussing this topic, it's almost impossible not to bring up rootkits and bootkits, so that's what our guest speaker Aditya Kapoor did. Additonally there was a lot of review regarding Kernal/User memory, process scheduling and Hooking that will be covered briefly. 

### Malicious Kits:
**RootKits**- Rootkits are pieces of malware that have the over-arching goal of conealing themselves from the users and system of the device, while also having root permissions in a system. They are most commonly found on Windows-32 Bit devices due to complications when trying to infect 64 bit systems. A rootkit infects usually through one of these three ways :
- exploits in the kernel.
- bypassing or stealing valid driver signature checks.
- adding itself to the bootpath.
 
**BootKits**- Bootkits are nearly identical in terms of functionality when compared to a rootkit, but their main difference is the fact that they add themselves to the master boot record so it can survive reboots. Once a device is infected with a bootkit it can be incredibly difficult to remove, since a bootkit has access to the kernel and boot process.

#### Review:
- **User/Kernel Memory**- 
- **Hooking**- 
- **Processes/Threads**-

#### Rootkit Types

There's a general and fairly simple two step process for a hacker to have successfully "hacked" your device. The first is simple, it's to trigger a vulnerability which could be overflowing a buffer, tampering with uniitialized memory, abusing faulty authentication, etc. Once the hacker has triggered the vulnerability and the process is in a state of freefall and or panic, the goal of the hacker is to try and control that freefall and introduce a payload(shell code primarily) at the same time.

#### Tools

- **Process Hacker**- this is a opensource website running a vulnerable instance of ActiveX Control, and is a learning aid for exploiting Windows primarily in the web browser environment. This was the primary focus of our labs and was created by Brad Antoniewicz himself.

![Yara Ouput](images/phack.png)

- **WinDBG/WinBAG**- Windows debugger is software developed by microsoft for the debugging of programs on their platform. It's main features include the ability to halt programs and take register dumps, providing assembly code for program instructions, allowing users to place breakpoints at instruction addresses and even look at modules being loaded into the program on start. The only downside to the program is the horrendous UI, but what can I say, it's from Microsoft.

![cheat sheet](images/winbdg.png)

WinDBG is the obvious winner in terms of tools this week -regardless of my love for Metasploit- it's proved to be almost too useful in the labs to not be given the recognition it deserves. The ability to spill a programs guts outs, sift through them quickly, translate between hex and decimals in 2 words of code, it's simply awesome. 

## Fun Facts Learned
- Windows virtual memory on 32 bit systems is 4GB.
- HackerDefender is the father of all modern day user-mode rootkits because it's the first one.
- 10% of all current malware use rootkits 
