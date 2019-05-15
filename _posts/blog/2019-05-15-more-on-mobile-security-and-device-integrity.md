---
layout: post
title: More on Mobile Security and Device Integrity
newsletter: True
categories: blog
---
In my previous newsletter<sup id="a1">[1](#f1)</sup> I comment on the recent news regarding the WhatsApp exploits discovered used by NSO Group and I marginally touch on the difficulties we encounter in confirming infections of mobile devices, particularly because of the tight security mitigations implemented by manufacturers such as Google and Apple.

Some additional debate and commentary appeared on social media, particularly after an article published by Motherboard<sup id="a1">[1](#f1)</sup> expanding on this particular issue, and quoting various security researchers as well as my newsletter. Because it is an interesting and contentious topic, I figured I could expand on my point. Forgive the higher frequency of my writing, but it's dicated by timeliness.

In my previous newsletter, I wrote:

> "... these security controls have made mobile devices extremely difficult to inspect, especially remotely, and particularly for those of us working in human rights organizations lacking access to adequate forensics technology."

And continued:

> "Quite frankly, we are on the losing side of a disheartening asymmetry of capabilities that favors attackers over us, defenders."

What do I mean by that?

What perhaps many don't realize is how resourceless we are, as technologists, when asked to respond to a suspected attack or to inspect a mobile device of an individual at risk who might have been targeted. For example, if a human rights defender suspects they are being surveilled and they bring their iPhone for inspection, all we can mostly do is search for suspicious messages and perhaps monitor the outgoing network traffic for the amount of time available to us (generally not a lot) hoping to get lucky enough to spot some suspicious traces at the right time. Obviously, when there is a significant distance or travel restrictions, our ability to intervene reduces drastically.

Under some circumstances there are exceptions and we might be able to do more. More commonly, however, technical, logistical and time constraints do not allow for a meaningful analysis.

Although the tight security controls baked into modern mobile devices are a net positive and significantly raise the costs for attackers, when the threat model of an individual at risk includes a nation state or even a law enforcement agency among their adversaries, these limitations play into the losing asymmetry of capabilities I mentioned in my previous newsletter.

Why? Because various companies out there are resourceful enough to acquire the necessary talent and the necessary technology (sometimes illegally<sup id="a3">[3](#f3)</sup>) and research and develop bypasses to smartphones' security mitigations. Companies such as NSO Group, or even Cellebrite<sup id="a4">[4](#f4)</sup> and GrayShift<sup id="a5">[5](#f5)</sup>, provide expensive products and services to States, which can essentially exercise an hegemonic power over the subversion of modern mobile devices for offensive purposes. In other words, there are tools available to law enforcement and intelligence agencies to break into an iPhone unknowingly to its owner, while there is very little available to us to inspect a smartphone even when the owner is willing to unlock it in front of us. I am sure it is superflous to explain why exclusively relying on law enforcement agencies or manufacturers is often not scalable or simply not possible.

Regardless of the legitimacy or illegitimacy of this imbalance, I believe it is an objective reality.

The resulting question then is: what can be done to enable people (especially individuals at risk and their support networks) to obtain more agency over their own mobile devices? Modern smartphones are very closed system, and perhaps for the owners' own good. Balancing a product's default security hardening with more access for its owner is not trivial. Some on social media rightfully argued<sup id="a6">[6](#f6)</sup> that opening up access for third-party security vendors to more closely inspect mobile devices will most likely result in that same access abused by malicious actors for offensive purposes. I agree. However, I also believe that more needs to be done (or at least explored) to provide at least some ability for consumers to independently verify the integrity of their devices. Even only within boundaries and with tools designed by the manufacturers.

Other than the obvious technical value of being able to determine whether a device is being tampered with (at any time, and under the owner's own security and personal safety requirements) and adapt one's secure communications strategy, enabling individuals at risk to learn whether their smartphones are being used to surveil them can also be an extremely important canary in the coalmine to alert them, and to contextualize their current exposure to personal risk.

What I'm left to wonder is whether some of these changes would be technically and economically justifiable for manufacturers, in contrast to the needs of a larger consumer base and the interests of shareholders. I don't know. I suppose that is the unfortunate result of the largely monolithic technological ecosystem in which we live.

<span id="f1"></span>1: [On the WhatsApp 0day and legal action against NSO Group - Nex](https://nex.sx/blog/2019/05/14/on-whatsapp-0day-legal-action-nso.html)  
<span id="f2"></span>2: [It’s Almost Impossible to Tell if Your iPhone Has Been Hacked - VICE](https://www.vice.com/en_us/article/pajkkz/its-almost-impossible-to-tell-if-iphone-has-been-hacked)  
<span id="f3"></span>3: [The Prototype iPhones That Hackers Use to Research Apple’s Most Sensitive Code - VICE](https://motherboard.vice.com/en_us/article/gyakgw/the-prototype-dev-fused-iphones-that-hackers-use-to-research-apple-zero-days)  
<span id="f4"></span>4: [Security-tech companies once flocked to Myanmar. One firm’s tools were used against two journalists](https://www.washingtonpost.com/world/asia_pacific/security-tech-companies-once-flocked-to-myanmar-one-firms-tools-were-used-against-two-journalists-/2019/05/04/d4e9f7f0-5b5d-11e9-b8e3-b03311fbbbfe_story.html)  
<span id="f5"></span>5: [Mysterious $15,000 'GrayKey' Promises To Unlock iPhone X For The Feds](https://www.forbes.com/sites/thomasbrewster/2018/03/05/apple-iphone-x-graykey-hack/)  
<span id="f6"></span>6: [Twitter](https://twitter.com/DidymaWorks/status/1128314170057748491)
