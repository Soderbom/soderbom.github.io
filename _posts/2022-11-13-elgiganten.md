---
layout: post
title: You won an iPhone 14 Pro!
date: 2022-11-13 15:00:00 +200
categories: [phishing, scam]
tag: [phishing, scam, junkmail]
---

Another scam e-mail! This time someone is impersonating Elgiganten, a Swedish retailer of consumer electronics. They are telling the victim they have won a new iPhone 14 Pro. 

Let's dig and see if we are that lucky.

## First impressions
This message has a whole bunch of red flags and the author mostly feeds on the victims possible excitement of winning an expensive phone. Most scammers use this sense of urgency or excitement to trick their victims. As mentioned in the previous scam post it is important to use Kahneman's *system 2* and not get carried away.

### Main attachment
![](/assets/images/elgiganten/main_pic.png)

The main attachment is full of odd formatting and the obvious use of "Google translate" which should be a red flag. The whole image is also clickable and leads to a hxxps://affiliateprogram[.]pw/ domain. More on that later.

If we look more carefully it is also very likely that this message isn't from Elgiganten, since their actual domain doesn't show up anywhere. 

### Who sent this?
Ok, so now we are suspicious. Who sent this to us?
![](/assets/images/elgiganten/address.png)

Certainly not the domain you'd expect Elgiganten to use. They do however refer to the receiving e-mail address in the subject line which is a little more effort than the scammers that were impersonating the Swedish police.

### Footer
This e-mail contains a footer that is trying to mimic an unsubscribe option, which most legitimate e-mail advertisements have. 

![](/assets/images/elgiganten/unsub.png)

Both of these fields are clickable.

The message also contains an address that I looked up on Google Maps, and it doesn't look right.

![](/assets/images/elgiganten/googlemaps.png)

None of the links point towards any domain used by Elgiganten. Let's take a look at what domains are being used. 

## Domains
Both the main attachment and the footer point towards hxxps://affiliateprogram[.]pw/ which is not owned by Elgiganten. Each of the links points to an end-point of the domain which is a long string of letters and numbers, reminiscent of baseXX but doesn't decode to anything useful. Three different links are pointing to different end-points but using the same structure. 

## Tracking
Since this e-mail was not sent directly to my junk mail I won't be following any links this time. Since they used the name in the subject and these randomly generated links it is likely they have some user tracking to be more efficient in their scams. The tracking could be used to determine if the receiver opens the mail or not, which in turn could lead to more junk being sent to the address. That said there is a risk of the tracker already being triggered by simply viewing the image. Security and convenience are often at odds, but if you want to avoid these trackers you can stop most e-mail services from fetching images from remote sources. Read more about that [here](https://www.wired.com/story/how-to-tell-which-emails-track-you/). 

## Tips and tricks
If you want to be extra careful while opening, you should disable the e-mail services' ability to reach out to external links for images. You can also use a trick to track who leaked your address by adding a plus sign to your e-mail address. Use youremailaddress+servicename@provider[.]domain, the addition after the plus sign won't be parsed so you will still get the e-mail but the addition will be added in the "from" field. This won't reduce the amount of spam you will receive, but at least you know who sold/leaked your information. Most e-mail services are free, so don't be afraid of having multiple addresses for different purposes. You should not mix your business e-mail with other services, since it increases your attack surface. 

### Things to look out for:
- Does the domain match the supposed sender?
- Does the sender want you to act with urgency?
- Is the message sent to multiple people?
- URL shortening
- HTML to legitimize brands
- Link manipulation
- Poor grammar and typos
- Does the message contain unrequested or unexpected attachments?

## Final thoughts
This scam campaign is low effort and therefore it is probably not directed. However, it has elements of automation to incorporate usernames and possibly tracking. The unsubscribe addition is interesting since it might lower the guard of the victim. Think of it as a magician's redirection, your eyes are focused on the obvious "win an iPhone" so you might not look twice at the other link. The message body is pretty much covered in clickable content, which is probably made to increase the chance of accidentally clicking one of the links.

They are most likely not Swedish natives since the grammar is off. I would expect that clicking the link takes you to a page where you are asked to fill in personal information or credentials. For a trained eye, the message looks very suspicious but for many, it might be enough to click. A campaign like this is directed to a lot of people so even if just a fraction clicks the link it might be enough for the scammers. 

Be careful.
