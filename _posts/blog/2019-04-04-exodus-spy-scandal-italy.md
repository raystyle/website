---
layout: post
title: "Exodus: How the Discovery of a Malware Revealed a Spy Scandal in Italy"
newsletter: True
categories: blog
---
On Friday 29th Security Without Borders in collaboration with Motherboard published a new investigation into a previously unknown surveillance vendor from Italy called eSurv.

[https://securitywithoutborders.org/blog/2019/03/29/exodus.html](https://securitywithoutborders.org/blog/2019/03/29/exodus.html)

This company, which purported to only be a surveillance cameras manufacturer, in reality has been producing intrusion software (spyware) since at least 2016. We dubbed this spyware "Exodus" after a domain name used as Command & Control.

[https://motherboard.vice.com/en_us/article/43z93g/hackers-hid-android-malware-in-google-play-store-exodus-esurv](https://motherboard.vice.com/en_us/article/43z93g/hackers-hid-android-malware-in-google-play-store-exodus-esurv)

As originally noted by Motherboard through publicly available documents, and as now confirmed by public prosecutor's offices, this software was in use by law enforcement all over Italy.

What made this software particularly worrying for us was, firstly, that it was widely distributed through the Google Play Store and publicly accessible for anybody to install. As a matter of fact, hundreds of installations were registered across 25 different copies of the spyware. Secondly, the spyware is able to collect much more information than what is normally mandated by law in Italy. Thirdly, the spyware would establish  unencrypted reverse shells to the Command & Control, that could be prone to man-in-the-middle attacks. Lastly, and even more worryingly in my mind, it would enable terminal access to the device by simply connecting to various fixed TCP port numbers, effectively leaving the phone exposed to further compromise or data tampering by anybody who would share the same network (such as a public Wi-Fi, or potentially even the same cellular network).

This story gained significant attention on Italian press and received coverage on all major newspapers, online and print, as well as on prime time television news on Saturday. While the initial press coverage wasn't particularly accurate, it opened up to some interesting and unexpected developments that are still unfolding.

The prosecutor of Napoli informed the press that an investigation was active on the company and that few days prior to our publication a judge issued a seizure warrant for eSurv and its assets, as well as another company, STM s.r.l.<sup id="a1">[1](#f1)</sup>

Italian press reports that STM s.r.l. had numerous contracts with public prosecutor's offices across Italy to setup and maintain the Exodus system they purchased from eSurv. The prosecutor's office of Benevento recently realized, during yet another apparent malfunction, that the Exodus spyware in their use wasn't exfiltrating and storing data on the local server in the premises of the office (as mandated by Italian law), but on Amazon cloud instances instead. As a matter of fact, the press reports, the server provided to the public prosecutor's office wasn't even equipped with an Operating System, and contained no data at all. Essentially it was an empty box. Additionally, it appears that interception data from invesigations by several other public prosecutor's offices was stored on this same Amazon instance, and that the companies maintained privileged access.<sup id="a2">[2](#f2)</sup>

This is wild.

The Exodus servers are being analyzed and people are being investigated. It is unclear currently what was the purpose and who was the operator of the malicious apps we discovered on the Play Store and how many of the hundreds of victims were intended and how many were accidental.

More recent reports are now suggesting that the story might go deeper and darker than originally anticipated. The press is currently suggesting that illegal spying might have been operated on behalf of unknown entities<sup id="a3">[3](#f3)</sup> and that this investigation is crossing with separate investigations dealing with corruption in Calabria<sup id="a4">[4](#f4)</sup>.

By all accounts, it seems that this story is still unfolding. More information will likely follow as more details from the investigations will come to light.

Hopefully, this case will reinvigorate a much needed debate on the nature of lawful interception intrusion software and the Wild West that is the industry behind it. In these years we have mostly debated on how to properly export these technologies out of Europe, but if anything, this case should highlight the very serious legal, technical, and constitutional issues raised by its current use here.

<span id="f1"></span>1: [Exodus, 4 indagati a Napoli. Intercettati illegalmente centinaia di italiani: "Dati giudiziari salvati su un cloud Amazon" - Il Fatto Quotidiano](https://www.ilfattoquotidiano.it/2019/04/01/exodus-4-indagati-a-napoli-intercettati-illegalmente-centinaia-di-italiani-dati-giudiziari-salvati-su-un-cloud-amazon/5078359/)  
<span id="f2"></span>2: [Benevento, software spia farlocchi e server giudiziari vuoti: sui cloud Amazon anche le intercettazioni di altre procure - Il Fatto Quotidiano](https://www.ilfattoquotidiano.it/2019/04/02/benevento-software-spia-farlocchi-e-server-giudiziari-vuoti-sui-cloud-amazon-anche-le-intercettazioni-di-altre-procure/5079009/)  
<span id="f3"></span>3: [Il sospetto di dossieraggi e ricatti con il software spia nei telefonini - Corriere.it](https://roma.corriere.it/notizie/cronaca/19_aprile_01/sospetto-dossieraggi-ricatti-il-software-spia-telefonini-c2347232-54b6-11e9-a9e2-a0d1446d1611.shtml)  
<span id="f4"></span>4: [Magistrati e investigatori, gli amici calabresi del poliziotto della "spy story" - Corriere della Calabria](https://www.corrieredellacalabria.it/regione/cosenza/item/181508-magistrati-e-investigatori-gli-amici-calabresi-del-poliziotto-della-spy-story/)
