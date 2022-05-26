---
title: "Welcome"
date: 2022-05-26T22:00:00-00:00
---

# Project Breakdown: _Masking_ Discourse 
This past quarter I took a class called *Surveillance Aesthetics: Provocations About Privacy and Security in the Digital Age* and the goal of this class was to create an art installation/piece of work that *provokes* people about the surveillance and (lack of) privacy and security around them. Our class (University of Chicago Computer Scientists) partnered with another class at the School of the Art Institute of Chicago (SAIC) with amazing artists of many different mediums and backgrounds and together the two classes formed groups of 3-5 people to collaborate on the aesthetics and code of our projects. I'm going to breakdown, **Masking**, what my group made throughout our time in this class.

---
## Project Introduction
![picture of **Masking**](https://raw.githubusercontent.com/cmdkev/cmdkev.github.io/master/assets/images/masking_2.jpg)

Now more than ever there are significant barriers and intermediaries of communication and discussion. Those barriers manifest themselves differently in digital and physical contexts. In digital contexts consider a social media network like Twitter, take a few seconds to think about what Twitter or TikTok do to control speech on their respective platforms. 

Maybe you remembered how Twitter has handled politicians like [Donald Trump](https://www.nbcnews.com/tech/tech-news/twitter-permanently-bans-president-donald-trump-n1253588) and [Marjorie Taylor Green](https://www.cbsnews.com/news/marjorie-taylor-greene-twitter-suspended-covid-misinformation/) - i.e. simply removing them from the platform. Maybe this reminds you -slightly - of that [Black Mirror episode](https://www.imdb.com/title/tt3973198/) where one person is continuously blocked from interactions with more and more people. Admittedly, de-platforming hate speech and dangerous rhetoric concerning COVID-19 is very different than being completely blocked from human interaction, but there are other examples of platforms [allegedly "shadow banning" content from black creators](https://www.digitaltrends.com/social-media/black-creators-claim-tiktok-still-secretly-blocking-content/) and [harming moderators who manually review sometimes disturbing content](https://www.theverge.com/2021/12/24/22852817/tiktok-content-moderation-lawsuit-candie-frazier). Moderation has been a huge issue for every large social platform or forum that has existed and on major platforms like Twitter and Facebook, there has not been significant effort and resources into even considering how to control the content until recently. 

Enter our project **Masking**: a look into what the future of communication control could be if we continue to allow for only the platforms with profit incentives or groups with questionable moral incentives to *write* and *control* the flow of information. **Masking** is a physical and digital mask (see above picture) that processes what you're saying and decides what to do with it from there in real-time (for the non-technical folks out there, it basically can behave like an Alexa or Google Home device). This leaves the question still, **what does it do**?? Its function is up to the decision of the programmer/designer/group in charge of development. They have the capability to censor and block words and phrases that they decide may be unwanted and to celebrate and boost words and phrases that they like. Initially, the idea for **Masking** began as a fun way to translate colloquial sayings between two people of different cultures or perhaps a way to ease communication behind a mask with live transcription as well as amplified voices. We quickly saw how easy it would be to simply change what people say and we arrived at the devious conclusion that we could control what one says. 

During our initial installation of **Masking**, we played a [censor tone](https://www.soundjay.com/censor-beep-sound-effect.html) over words and phrases like:
```python
[
	 'crisis', 'socialism', 'communism', 'communist', 
	 'socialist', 'think', 'democrat', 'military', 'congress', 
	 'conservative', 'liberal', 'protests', 'creepy', 'invasive', 
	 'government', 'republican', 'like', 'covid', 'violence', 'i think', 
	 'i believe', 'my opinion', 'gun control', 'climate change', 
	 'privacy rights', 'livable wage', 'black lives matter', 
	 'i just think'
]
```
The purpose of this being so on the nose was to prevent and disrupt normal discussions of normal things. By imagining a device that is disruptive of discourse and conversation we hope to provoke people into considering the situations in which their own speech may be controlled against their own wishes (and without their knowledge) for the advancement of an agenda that harms people in general.

---
## Technical Breakdown 
*This is for my technical folks, feel free to skip if you don't know what a *python* is, but I promise its not as scary as you may think it is.*

Our hardware consisted of a raspberry pi 4, and a USB speaker and microphone as well as the mask of course. The speech recognition ran off a library called [*Vosk*](https://alphacephei.com/vosk/) that provides tiny models that are more than capable of doing live speech recognition (which is crazy to me) on a tiny raspberry pi that has a fraction of the processing power available to it as the typical machine learning machines you may normally think of. As a programmer, it was fun to know my restrictions of processing power and memory size and to then find a solution to a problem constrained as such. We then use [NLTK](https://www.nltk.org/) to process the text form of the speech recognized by Vosk. 

Although not easy to develop, the technical solution for a mobile device capable of real-time speech recognition and processing is quite simple, consisting of only a few moving parts. What I find most funny and thought-provoking about the technical experience is when people would ask us something like "can it block {insert word/phrase here}?" to which we'd simply reply "Sure." and type whatever it was at the end of the list you see above.

---
## Implications 
I suggest you take from this **breakdown** what you will! Form your own opinions! Do your own research (but trust experts, and not your [cousin in Trinidad](https://twitter.com/NICKIMINAJ/status/1437532566945341441?s=20) <3)! But if you're interested in what I think is important, read on :)

I strongly believe and urge people to consider consider the technology they engage with, especially as they relate to your own privacy or identity! It's a large part of my research interests after all. In addition to that, a thought that may be going through your head now is "what can I do to influence what Twitter or whoever is doing with my data or my voice/speech?" as a single person its powerful to just be conscientious about these things, but beyond being aware its also possible to [make your voice heard to governments](https://morningconsult.com/2022/01/12/federal-data-privacy-legislation-polling/) and platforms about what policies you need. There are groups like the [Electronic Frontier Foundation](https://www.eff.org/) who educate and advocate on behalf of the people with no profit incentive, simply the moral prerogative to "[defend] civil liberties in the digital world". 

---
## Wrap-up
One of my friends always jokes on conspiracy theorists saying something like, "some of them are so dumb because no one even benefits from this" probably in reference to the lizard people controlling the country without anyone ever knowing. While it is funny, it is also a good question to ask yourself when using new technology (especially free technology). Ask yourself and others around you, why is this free? What do the creators gain from me using this? **Masking** was meant to exemplify how easy it is for 3 people to control your speech, so consider other ways in which you are controlled against by groups larger than our team of 3. 
