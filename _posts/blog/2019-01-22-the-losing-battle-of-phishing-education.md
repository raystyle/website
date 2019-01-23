---
layout: post
title: The Losing Battle of Phishing Education
newsletter: True
categories: blog
---
Today Google Jigsaw launched a new resource self-descriptively called Phishing Quiz. I generally applaud these efforts and I myself often recur to quizzes in my occasional trainings. This one is well designed and straightforward to use.

[https://phishingquiz.withgoogle.com/](https://phishingquiz.withgoogle.com/)

The declared purpose of these quizzes is to enable potential at-risk individuals to train their eyes in spotting suspicious elements in email messages and web pages. For me, the purpose is rather to highlight the difficulty in recognizing well-crafted phishing attacks, and the numerous design inconsistencies across online service providers.

Google's quiz perfectly highlights many of these inconsistencies, and I invite you to try it for yourself. I did the same and at the end of it I tried to anticipate how an individual approaching this subject for the first time might leave confused.

Training individuals to detect phishing attacks through visual references is hard, because those don't follow a logic shared across platforms and because they change occasionally.

*[SPOILER ALERT: I am going to reference certain results from the Google Phishing Quiz, so do not read further if you don't want any anticipations.]*

In this quiz the primary two key visual elements the exercises are based upon are the email sender's address and the links contained in the body of the message. Ideally, through this, individuals should identify patterns and construct a mental model to apply to any similar real-case scenario. However, we immediately see inconsistencies.

In one exercise we are suggested that an email is in fact legitimate because, along with the validity of a contained link, the sender's email address contain the domain @dropboxmail.com, which is an actual domain in use by Dropbox instead of the more intuitive @dropbox.com. At the same time, however, a different exercise alerts us that an email sender with @google.support is malicious because the domain is not in use by Google.

Perhaps an agreement among service providers to all adopt a similar scheme would be beneficial. For example, instead of using various domain names, all should stick to their primary domain for email communications, e.g. *noreply@dropbox.com* or *noreply@google.com* instead of *dropboxmail.com* or *googlemail.com*.

When it comes to links contained in the body of email messages we could expect similar confusion. Forged domains intended to deceive (such as "*paypal.com-myaccount-login-issuespayment-global.realbaddomain.com*") should immediately stand out, but we also need to be alert of other more insidious techniques!

As Google's quiz exemplifies, a phishing link could come in the form of an actual Google domain for example:

**https://google.com/amp/gmail-account-activation.support/**

This would be a valid Google link redirecting to an hypothetical phishing site. Similarly, an email could also contain a valid Google link that will lead to a prompt requesting a malicious app to be enabled on our Gmail account. Ironically, even the domain of the quiz could be deceiving: what is withgoogle.com?

Essentially we are demanding individuals to not only be able to discern clearly forged domains from legitimate sites, but also to be aware of all the possible tricks to abuse existing functionality (such as OAuth[1] or redirects). Additionally, we are demanding them to be aware of what email addresses or message formats are commonly used by legitimate services at any point in time.

This is unattainable. If the burden relies so heavily on users, the underlying technology appears inadequate to me.

Without entering in the merit of mitigations such as two-factor authentication (which I discussed in the previous newsletter), or with other complications such as spoofing, we have identified enough booby traps already to likely dissuade most people from learning about online accounts security.

We need more consistency across services. Consistency of procedures, language and available mitigations. And perhaps it is time to sacrifice some convenience and functionality in favor of a smaller attack surface.

p.s.: As you might have noticed, I am making excessive use of the term "individuals". I am purposefully trying to avoid "users", which I generally don't like. If you have any recommendations for more suitable words, I would very much appreciate them!

[1]: https://duo.com/blog/gmail-oauth-phishing-goes-viral
