---
layout: post
title: On the Banality of Attacks and on Mindful Engineering
categories: blog
---
Over the years of my experience assisting journalists and dissidents with matters of computer security, and researching the nature of the threats they face, I learned that those who don’t have access to security solutions and do not operate in a managed environment, are often not best served by the consumer technology they are normally provided with.

There is a recognizable difference between the design of certain consumer technology and some other. Mobile phones, for example, are increasingly provided with operating systems that are designed — for the most part, at least — around the interests of end-users. Other technology, like personal computer’s operating systems, seem to be often designed around the interests of the Enterprise sector instead. It really depends on what appears to be the primary target market for the producer.

To me, this is signified by the fact that among the many — and I mean, really a lot of — attacks that I have observed targeting members of civil society, the use of exploits is a rare sight. Mind, not just zero-day exploits, but even just exploits at all. The large majority of attacks that I observe leverage tricks as infection vectors that are very simply (ab)using features that are exposed by the operating system or mainstream consumer software, and that seem to be mostly intended for enterprise users. Rather than a lack of sophistication on the part of the state-sponsored actors orchestrating these attacks, I believe this rather indicates a dire state of overall security controls.

There are definitely tactical advantages in using tricks rather than exploitation. For example, abusing features exposed by operating systems like Microsoft Windows or by primary consumer applications like Microsoft Office, or Adobe Reader, requires way less situational awareness. Attackers do not need to know which architecture, build, or version of the particular software targets use, and as such there is no need to spend resources and time crafting attacks that must be reliable. This is particularly true when the target of an attacker is a diverse demographic that does not operate within an uniformed technology stack as it generally is in corporate and government environments. Additionally, while attackers often look for that one weak entry point to exploit in the operations of corporations or government institutions, the targeting of activist and dissident groups is often opportunistic — except, of course, of some individuals who are of particular interest — and attackers seek instead to just compromise as many people as possible. As a matter of fact, it is common to see the same spearphishing email being sent in carbon copy to dozen of individuals, even working for different organizations.

For these reasons, targeting activists, journalists, and dissidents using tricks is very likely way less expensive than using exploits, and might in fact result in a higher success rate. Consequently, this is driving up the numbers of attacks we witness.

The most common vectors for spearphishing attacks that I’ve observed in the last year involved the abuse either of Microsoft Office Macros and Packager Shell Objects, or the abuse of PowerShell or Windows Script Host. With perhaps the exception of Macros for Excel, all the remaining tricks are powered by features that are generally useless to regular users, and are rather thought for the Enterprise sector.

For some of them, I can’t even think of any reasonable legitimate use. For example: why should one be able to embed Windows executables inside a PowerPoint title slide and automatically launch them through a custom animation? *(Insert here a dozen more implicit question and exclamation marks.)*

I understand. A lot has to do with enabling system administrators and software developers to automate some of their tasks. Yes, I am sure that PowerShell is great at that. I am also sure it is great for facilitating incident response in corporate environments. However, please don’t make those default options (or in the case of PowerShell, for example, no option at all). Organizations can provision the configuration they prefer, end users instead have to stick with what they’re given. I am all for rich features and plenty of possibilities, but I am also for security by default, not by choice.

Let me now demystify some of the most common responses I get when similarly ranting about these particular issues.

1. **“There is Antivirus software, they detect all that”**

    Firstly, no. Secondly, any security design that relies on the efficacy of third party products that your user must discover and acquire is a ridiculous one.

2. **“Users should learn not to click on unsolicited links and attachments”**

    Links and attachments are supposed to be clicked. It’s the whole point. If you expect users to be able to discriminate naturally between a legitimate email and a malicious one, you are detached from the reality of real world attacks. Attackers commonly befriend victims, impersonate their relatives and co-workers, and create all the pre-conditions to make the attack as credible as possible.

3. **“Users are warned when they are about to execute something dangerous”**

    <div style="float: left;padding-right: 20px;padding-bottom: 5px;"><img src="/assets/blog/20170111/warning.png" /></div>

    That’s not always the case, but it is for some applications. However, it is also clear that vague, undescriptive warnings — like the one displayed on the side — are not enough. For example, in the case of some targeted attacks against dissidents in Iran my co-conspirator Collin and I have documented last year, the malware was delivered through malicious PowerPoint presentations that embedded multiple copies of the same executable in the title slide and launched it in the same way I described earlier. Why multiple copies? Because while at the first, or second, or third security warning dialog from Microsoft Office the victim might not allow the payload to execute, they most likely will at the fourth or fifth. We formalized this technique as Security Bypass by Annoyance.

4. **“Even if you disable one feature or another, there’s so many ways to compromise someone”**

    True. It still doesn’t mean however that we should leave all doors open. Reducing the number of possible attack points allows us to deal and watch for the fewer remaining ones more efficiently.

To this effect, my dear friend emdel and I at Security Without Borders have started aggregating tips & tricks to disable some of these most problematic features in a little experimental utility that is being assembled here.

In conclusion, I invite software producers — especially those who provide highly popular consumer applications — to stay informed on how some of their choices are being regularly abused, to stop blaming users, and to start practicing more mindful engineering.
