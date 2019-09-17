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

> Interface: a surface regarded as the common boundary of two bodies, spaces, or phases. -- [dictionary.com](https://www.dictionary.com/browse/interface)

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

We have decided to perform this analysis by starting with a well known interface to decentralized social media software, [Mastodon](https://joinmastodon.org/)'s default web interface.
We will examine the current behavior of the interface with a critical eye for security concerns, present proposed modifications for the interface where appropriate, and then examine what security benefits those modifications would bring.

What we are not trying to do is to criticize Mastodon for having a particularly "bad" interface.
In a sense the opposite is the case; Mastodon's web UI was chosen because it is clear that the developers have given great care that users are given a pleasant and comfortable experience.
The issues and concerns we raise are pervasive throughout contemporary interfaces as a whole;
we do not blame Mastodon's developers for the current behavior since the concept of security as being a first-order principle in user interface design is not broadly acknowledged.
We do, however, hope that this paper will be able to contribute somewhat towards changing that state of affairs.

### Composing a private message

<!-- * Current behavior -->
<!--    * Typing results in a completion suggestion box with people I’m following by their proposed names -->
<!-- * Changes -->
<!--    * The suggested names are the names we’ve chosen for them (pet names). NOTE: not yet edge names -->
<!-- * Accomplishment -->
<!--    * Avoids risk of phishing by having one of our followers changed their proposed name to appear to be someone else. -->

### Composing public vs private messages

<!-- * Current behavior -->
<!--    * In Mastodon messages are public by default (in the previous case the user would have shown a “world” icon and the user needs to click the “envelope” icon to make the message private. -->
<!-- * Changes: maybe none! -->
<!--    * Consider changing default from private mode vs. public mode -- perhaps this could be made obvious by a change from light mode to dark mode.  -->
<!--    * NOTE: private by default is like e-mail (may start with To: box on top), public by default is like twitter (make it look like a tweet box)..  -->
<!--    * NOTE: movies sometimes use different color balance to guide the viewer to understand when multiple timelines are interleaved. -->
<!-- * Accomplishment -->
<!--    * User should not be confused about if message composition is public or private. -->

### Onboarding new users

<!-- * Current behavior -->
<!--    * User chooses their user address (“username”), proposed name and user avatar -->
<!-- * Changes -->
<!--    * In the future user address may be opaque (hidden from the user). For example self-authenticating-designators may be hidden. -->
<!--    * NOTE: perhaps we want to encourage users to self host (and thus we may discuss setting up a node) < which increases the level of decentralization in the system. -->
<!--    * There isn’t a need to make a distinction between a username and a proposed name; instead, a user only gives a proposed name. -->
<!--    * The user may also give their proposed avatar, but the execution of this is a bit out of scope -->
<!-- * Accomplishment -->
<!--    * The rationale for removing user address is that 1) it is likely that in the future this will be a long, complicated string of characters [example: in the C language a pointer variable refers to a memory address, but we don’t care about the specific value of that memory address] and 2) We want to consciously move away from giving the user address importance (and specifically giving it real estate in the UI). NOTE: this will be hard for users because we are accustomed to giving importance to usernames and email addresses. -->

### Viewing profile

<!-- * Current behavior -->
<!--    * View proposed name -->
<!--    * View user address (“username”) -->
<!--    * View user avatar -->
<!--    * View other info: toots, followers, following, proofs (e.g. keybase, DNS rel=me) -->
<!--    * Show user content: toots, toots & replies, media. NOTE: may be helpful to confirm (or not) the identity of a user -->
<!-- * Changes -->
<!--    * Make user address opaque -->
<!--    * Consider: show edge names for this person -->
<!--    * Follow: propose a pet name, prompt for an edge name (may have a suggested one: proposed one or uncorroborated edge name or corroborated edge name). NOTE: concern about prioritizing edge names over proposed names. One one hand proposed names could be used for phishing, on the other hand the proposed name may change due to marital status while the edge names would propagate the outdated name. Thus the user should probably see both (and make the choice). -->
<!--    * Not follow: propose a pet name, provide option to add a pet name (think badgargron). -->
<!--    * Merge with payment systems: leveraging my web of trust (social web, currency web often the same) Consider WeChat. -->
<!--    * NOTE: when and edge name is created is it private by default? Should it have multiple levels of visibility (none, mutuals, followers, public). Perhaps a profile setting for default (e.g. mutuals) and the ability to control the visibility on a per followee basis. -->
<!--    * NOTE: Mastodon private queue for user actions -->
<!-- * Accomplishment -->
<!--    * Phising resistent -->
<!--    * Edge names help bootstrap relationships securely -->
<!--    * We’ve opened ourselves up to sadness - using SADs (self authenticating designators) -->

### Searching for users

<!-- * Current behavior -->
<!--    * Enter partial information: Mastodon shows a list of proposed matches (each with proposed name, user address and user avatar). -->
<!-- * Changes -->
<!--    * Each result will show pet names and user avatars (but not user addresses). Next results comprise matching edge names showing integrity and corroborations. NOTE: the edge name results should be shown differently visually such that it’s clear that they are edge names (e.g. using arrows, cwebber->emacsen). -->
<!--    * NOTE: pet names and probably edge names sorted based on inertia (e.g. frequency of use, machine learning, etc.) -->
<!--    * NOTE: consider the ability to search on edge names -->
<!-- * Accomplishment -->
<!--    * Avoided phishing attacks -->
<!--    * Added a discoverability mechanism (find other contacts you may be interested in which may have confidence based on existing corroberation). -->
<!--    * NOTE: Inertia would increase search result relevance and quality of user experience. -->

### Adding connections

<!-- * Current behavior -->
<!--    * There is a “follow” button in search results -->
<!--    * Can paste a user address into the search bar (and then that user will be show as if a search result). -->
<!--    * NOTE: it is possible to click on a user address in results to view the profile (presumably to add confidence prior to following… See Viewing Profile). -->
<!-- * Changes -->
<!--    * Add a plus icon (add user image) to aid discovering the add connection feature from the search bar. -->
<!--    * This changes the interface to enable dragging and dropping (or copy and pasting) the encapsulated address, or the scanning of a QR code. User addresses encapsulated : presented as proposed names. -->
<!--    * TODO: cwebber to define “encapsulated” (or alternate term) -->
<!-- * Accomplishment -->
<!--    * Freed from the assumption that user addresses are meaningful to the user experience on their own. And this opens a path to using self authenticating designators (saddness :) ). -->
<!--    * Aiding discoverability of adding connections via search results -->

### Contact management

<!-- * Current behavior -->
<!--    * One must view one’s own profile and then click on followers to access contacts. -->
<!-- * Changes -->
<!--    * NOTE: An idea for a future change is to view our contacts as a visual graph. -->
<!--    * As in Viewing Profile there is an opportunity to change the pet name for a contact. -->
<!-- * Accomplishment -->
<!--    * By adopting the other changes contact management will benefit. -->

### Receiving message

<!-- * Current behavior -->
<!--    * Shows user avatar, proposed name, user address and then the message. -->
<!--    * The body of the message may contain references to users, shown as unqualified user address (a security information deficiency ). -->
<!--    * Clicking on a user will bring up their profile -->
<!-- * Changes -->
<!--    * Either we do NOT show an avatar, or we show a pet avatar or an edge avatar (which we have not defined yet). -->
<!--    * TODO: cwebber needs to define the above terms! -->
<!--    * Shows the pet name and the message. -->
<!--    * The body of the message is shown with users (that are our conte rendered the best way possible: -->
<!--       * pet names -->
<!--       * edge names [with integrity and corroboration UX] -->
<!--       * proposed names -->
<!--          * Displayed in a distinct way, including numbering where necessary (1 through 9, with ellipsis for 9+) (e.g. “?” instead of “@”) -->
<!-- * Accomplishment -->
<!--    * No phishing via avatar (how this works comes later), nor via proposed name -->
<!--    * Hiding user address (enabling sadness :) ) -->
<!--    * Intuitive distinction between “level of integrity” between petnames vs edge names (and amount of corroboration) vs proposed names -->

<!-- Petnames, edge names, proposed names -->

<!-- Phishing attack -->

<!-- Phishing attack: if @emacsen=>tmarble sends a mail about ?mallet who wants to trick me into thinking it was about ?mark -->
<!-- Gargron’s response: -->
<!-- “The completion prioritizes people you follow. I personally remember display names more than usernames. A petname system would provide convenience in case of people who change their display name often for jokes, but I don't see what protections it would provide that prioritizing people you follow doesn't. It's not like you would define petnames for people you don't follow, would you?” https://mastodon.social/@Gargron/102730145345440621 -->


## Design patterns and principles
### Original design principles
### New principles
## Conclusion
## Glossary

## Footnotes

<a id="fn.one-click" href="#fnr.one-click"><b>[fn:not-one-click]</b></a>
See also [Not One Click for Security](https://www.hpl.hp.com/techreports/2009/HPL-2009-53.html).

