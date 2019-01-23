---
layout: post
title: Phishing, Two-Factor Authentication and False Myths
newsletter: True
categories: blog
---
Today we published a rather short report detailing a campaign of phishing attacks we monitored closely during the last year. You can find it here:

[https://www.amnesty.org/en/latest/research/2018/12/when-best-practice-is-not-good-enough/](https://www.amnesty.org/en/latest/research/2018/12/when-best-practice-is-not-good-enough/)

In this report we don't get into attribution or victimology, but we provide what I believe to be an accessible read to describe how targeted phishing attacks are actually conducted by real state-sponsored attackers, in this case originating from a country in the Persian Gulf. While there are some interesting elements in the phishing of "secure email" services such as ProtonMail and Tutanota, what I found to be more fascinating and important to discuss at length, is the ability of this particular attacker to successfully bypass some forms of two-factor authentication.

Note: although in this case two-step verification might be a more accurate term, for the sake of simplicity I am going to stick to two-factor authentication (2FA). However, if you are interested in understanding the purist differences you can find a good explanation here: 

[https://lifehacker.com/the-difference-between-two-factor-and-two-step-authenti-1787159870](https://lifehacker.com/the-difference-between-two-factor-and-two-step-authenti-1787159870)

Google offers several methods for two-factor authentication. By default it sends a verification code (normally made of 6 digits) via SMS to the registered phone number. The user would then be prompted to input the code they just received and continue with the login. Yahoo by default also provides the same login verification process. Both these services offer several other flavors of 2FA, including authenticator apps or push notifications (which consists in installing an app on the phone which will request you to manually approve a login by tapping a button, rather than copying a code).

As we detailed in this report, the attackers have built a system cleverly designed to workaround at least the SMS based verification procedure. However, I believe the technique they used can be just as easily adapted to nearly every other form of verification including authenticator apps as well as push notifications. Essentially the attackers have built an "auto-pilot" software that automatically instruments a Google Chrome browser and directs it to the login pages of the service, such as Google or Yahoo, whenever a victim visits the phishing page and begines to provide account name and password. In the meantime, the software will in the background automatically enter the credentials to the legitimate service using the instrumented Chrome browser. If it notices that the service requires some additional information for verification purposes, such as the numerical code sent via SMS, the phishing page will simply display a clone of the original prompt and wait for the user to input the valid code that the service indeed sent to their phone at the request of the instrumented Chrome. If the victim, thinking of interacting with the original Google or Yahoo, enters the code in the phishing page, the software will copy it and send it to the original service it had open and complete the login process successfully.

They do this using a popular automation framework called Selenium, normally used for quality assurance and automated testing of web applications.

While SMS code verification isn't necessarily the strongest form of 2FA (and indeed, it should be generally avoided if only because SMS is an insecure protocol), I believe that with sufficient automation it is possible to bypass other flavors as well. For example, nothing prevents an attacker to just in the same way request valid codes from an authenticator app (such as Google Authenticator) and automatically use it with the instrumented browser. Or similarly, if in the background the instrumented Chrome is being required by the service to approve the login through a push notification, an attacker should be able to lure the victim into approving the login on their phone. If the attackers managed to lure the victim to enter their password, I don't imagine an additional piece of information or action would be much harder to solicit.

Ultimately this form of attack can be successful if the attackers build a sufficiently adaptable automation system to interact with the original services, combined with a frontend offering credible phishing pages to the victim. Unless the targeted online services implement heuristics or other mitigations against automation (such as CAPTCHAs), it might be hard defeat this. Worryingly, building such a phishing framework is not actually that complicated, and as a matter of fact we have observed other low-sophisticated state-sponsored attackers employing just the same techniques as well.

I am very concerned about this. Particularly when it comes to individuals at risk and activist communities, I personally witness an alarmingly common misconception over the security promise these 2FA flavors offer. As a result, some of them have internalized a false sense of security which lead them to be significantly less cautious. For this we, as a community of technologists and security trainers, are most likely to be blamed due to the inadequacy of our security education programs.

However, this is not to say that two-factor authentication is a worthless effort, quite the contrary. ANY two-factor authentication is better than none, and there are ongoing developments in this space which will make these attacks less feasible.

Currently, security keys supporting the U2F protocol (such as Yubikeys, Nitro keys, Solo keys, etc.) are the best available protection and I invite everyone to at least explore that option. The report provides some more elaborate considerations and recommendations about this, so I invite you to read it in full.
