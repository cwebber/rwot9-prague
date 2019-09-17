# Secure User Interfaces

## Abstract

As critical human activities are increasingly being conducted online such as personal and commercial communications, transmission of funds, voting, providing legally-binding digital signatures, and so on, the importance of designing interfaces that are both user-friendly and secure is growing.

Using a social messaging interface as a use case, we focus on the need to co-design user experience and underlying security foundations.

<!-- This paper has three parts. -->

<!-- First we will define criteria of a secure communication system including technical feasibility, ethical desirability and usability.  -->

<!-- We will then explore the requirements of a user interface that conveys the security of the system to users in an intuitive way, with an emphasis on inclusive design.  -->

<!-- We will conclude by issuing recommended design patterns and principles illustrated via best practices for decentralized applications. -->

<!-- ## Requirements -->

## Introduction

> Interface: a surface regarded as the common boundary of two bodies, spaces, or phases. ([from dictionary.com](https://www.dictionary.com/browse/interface))

By enabling us humans to interact with our private and shared digital realities, user interfaces occupy a critical position in the information and communication systems our world depends on.
We imagine the user interface as the surface between two informational realities: the digital space of the machine and its network, as well as the conceptual space of a human’s interior awareness.
The user interface is the means by which our interior thoughts can be recorded privately and broadcasted publicly.
In an era of electronic communication it has become an organ for both storing memories and projecting our voice.

<!-- (Reference suggestion: Marshall Mcluhans Understanding Media: The Extensions of Man https://en.wikipedia.org/wiki/Understanding_Media) -->

As information has value and knowledge is power, user interfaces present significant security challenges.
Because of this, system security depends on the security of user interface design.
In the context of the decentralized web and self-sovereign identities, many of the user protections provided by centralized authorities are removed.
We accept the risks inherent to claiming the responsibility of maintaining custody of our own private keys - and, therefore, sovereignty over our funds and personal data - because we believe the benefits outweigh the risks and violations innate to ceding custody of our data to centralized authorities.
However, mitigating the risks of self-sovereignty is the moral obligation of designers of decentralized applications.
To this end, we propose these principles for the design of secure user interfaces.

When users interact with a program through its iterface, they carry with them a set of assumptions of what behaviors will occur through their actions in the program.
Some of these assumptions are pre-conceptions, and some of them are taught to users through exposure to the interface itself.
Most interactions through a program thus become routine; the user is not very actively thinking about the structure of the program, but relying on the intuition they have built up about how the program will behave.
There will always be some degree of misalignment between the user's intuition and the behavior embodied by its interface; such moments open up a user to vulnerability.
It is our goal that when this misalignment occurs that the behavior of the program "fails safe".

The focus of our study will be on building secure, decentralized social networks.
However, we believe that the lessons from examining social networks can be extrapolated to nearly all user interface programs.

The crux of such a secure communication system surrounds identity and the naming of users, for when naming is misunderstood, users may communicate, exchange money, or perform other actions with users whom they did not intend.
The consequences of getting this wrong range from a violation of privacy to (as communication systems are increasingly interwoven with payment mechanisms) being tricked out of one's money.
Our assertion is that by and large, user interfaces today (particularly in the examples of social systems) *do not* "fail safe".
The general perception is that building security into user interfaces necessarily requires inconveniencing users.
We counter that building a secure user interface necessarily requires that safety be part of the default, comfortable, intuitive user experience that users expect and demand.<a href="#fn.one-click" id="fnr.one-click">[fn:not-one-click]</a>

Due to the centrality that it plays in solving the issues of naming, readers are encouraged to read up on [petnames](https://github.com/cwebber/rebooting-the-web-of-trust-spring2018/blob/petnames/draft-documents/making-dids-invisible-with-petnames.md) as a prerequisite to continuing with this paper.

## User flows by comparison

We have decided to perform this study by starting with a well known interface to decentralized social media software, [Mastodon](https://joinmastodon.org/)'s default web interface.
We will examine the current behavior of the interface with a critical eye for security concerns, present proposed modifications for the interface where appropriate, and then examine what security benefits those modifications would bring.

What we are not trying to do is to criticize Mastodon for having a particularly "bad" interface.
In a sense the opposite is the case; Mastodon's web UI was chosen because it is clear that the developers have given great care that users are given a pleasant and comfortable experience.
The issues and concerns we raise are pervasive throughout contemporary interfaces as a whole;
we do not blame Mastodon's developers for the current behavior since the concept of security as being a first-order principle in user interface design is not broadly acknowledged.
We do, however, hope that this paper will be able to contribute somewhat towards changing that state of affairs.

### Composing a private message
### Composing public vs private messages
### Onboarding new users
### Viewing profile
### Searching for users
### Adding connections
### Contact management
### Receiving message

<!-- Petnames, edge names, proposed names -->

<!-- Phishing attack -->

## Design patterns and principles
### Original design principles
### New principles
## Conclusion
## Glossary

## Footnotes

<a id="fn.one-click" href="#fnr.one-click"><pre>[fn:not-one-click]</pre></a>
See also [Not One Click for Security](https://www.hpl.hp.com/techreports/2009/HPL-2009-53.html).

