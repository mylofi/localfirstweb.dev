---
title: I wrote a static web page and accidentally started a community
description: "The flap of a butterfly’s wings on one continent, so the story goes, can cause a
tornado a year later in another. Here’s my story of how something like that can
happen on the web too."
layout: post
author: James Pearce
author_link: https://twitter.com/jamespearce
---

The flap of a butterfly’s wings on one continent, so the story goes, can cause a
tornado a year later in another. Here’s my story of how something like that can
happen on the web too.

## I’m on a boat

First, the back story. Last year, after a wonderful ten years at Facebook (and
then Meta), I left my position as Engineering Director, and, with my wife Jayne,
moved onboard our sailing boat, [Scout](https://scoutsailing.com/). We quickly
got accustomed to a life of going wherever or whenever the weather wanted to
take us.

But there’s a lot of downtime on a boat. Me? I’ve been using this opportunity to
grow and maintain an open source project called
[TinyBase](https://tinybase.org/), a way to store structured data in a browser
and react to its changes.

As I got TinyBase going last year, there were two tweets that really got my
attention. The first was from Cory House who drew attention to “[a new
collaborative software
architecture](https://twitter.com/housecor/status/1492203985335373825)” (and as
follow up gave the project a well-needed and generous
[shout out](https://twitter.com/housecor/status/1492859757941637126)!). The
second was from Geoffrey Litt, who, with colleagues, published [an excellent
essay](https://twitter.com/geoffreylitt/status/1499083601387864069) about
running relational, reactive databases on the client.

Both referred to the phrase “Local-First”, and I wanted to know more. Over a
decade ago, I’d been swept up in the
“[Mobile-First](https://www.lukew.com/resources/mobile_first.asp)” movement, and
this second “First” sounded just as intriguing - especially given my new
maritime circumstances.

## But what is this Local-First you speak of?

You see, connectivity is generally good on a boat - wifi, cell coverage, and
satellite options abound - so we survive. But when it isn’t good, it _really_
isn’t good. And then suddenly, it dawns on you just how much of your life is
beholden to the cloud. Your documents don’t load. Your photos don’t sync. Your
messages don’t send. Without necessarily consciously realizing it, we have all
moved most of our online existence to [other people’s
computers](https://www.chriswatterston.com/article/success-of-my-there-is-no-cloud-sticker)!

Now, of course, there are many advantages to this shift: collaboration, backups,
multi-device access, and so on. But it’s a trade! In exchange, we’ve lost the
ability to work offline, user experience and performance, and indeed true
dominion over our own data.

I was fascinated by this shift, but also surprised by how much we all - both
users and developers - have taken this for granted. It’s almost heretical to
build a web-based application that _doesn’t_ have the cloud as the source of truth
for data, and the client as merely a dumb display of a cached copy of it. I
wondered why.

As I disappeared down this rabbit-hole, I quickly stumbled on the canonical
essay on the topic, “[Local-first software: you own your data, in spite of the
cloud](https://www.inkandswitch.com/local-first/)”, by research lab Ink &
Switch. In summary, they identify seven principles for local-first
applications:

- No spinners: your work at your fingertips
- Your work is not trapped on one device\
- The network is optional
- Seamless collaboration with your colleagues
- Your work should continue to be accessible indefinitely
- Security and privacy by default
- You retain ultimate ownership and control

Now we’re talking!

But I was equally surprised by how little this was being discussed, or (as far
as I could tell) practiced in the real world. While there seemed to be endless
threads on Twitter about server-side React (to get the UI generation closer to
the data), no-one was talking about the opposite: moving the _data_ to be closer
to the UI, and onto the client!

Nevertheless, I realized that TinyBase could theoretically fit nicely into this
picture: a way to have a structured store of data on the client side (with a
close-by binding to the user interface), and took the slightly cheeky
opportunity to update the project’s strap line: “The reactive data store for
local-first apps”.

Still, I wasn’t exactly sure that people knew what “local-first” meant. What
could I do about that?

## A butterfly flaps: the creation of localfirstweb.dev

In a previous life, I had worked with some excellent developer relations teams,
and if there’s one thing I remembered from then, it was that one of the
ingredients of raising awareness around a topic is to have a good landing page.
And it didn’t seem like such a thing existed for local-first.

The Ink & Switch article was a great start, but as I explored, I came across
many projects from people trying to build the scaffolding for a local-first
future - databases, synchronization techniques, best practices. But they were
scattered around and I could see a lot of value in curating a list of the
activity that was happening in this space.

So, one free day on the boat, I rolled up my sleeves, dusted down some old
Jekyll skills, and got started. I didn’t really have much more of a plan than to
take my ‘local first’ browser bookmark folder and put all the items onto the
page: basically a web directory just like it was 1994!

A few hours later, I had the skeleton of
[localfirstweb.dev](https://localfirstweb.dev/) up and running - my first .dev
domain too! - and published with GitHub Pages. Add in a quick [launch
tweet](https://twitter.com/jamespearce/status/1623773053447729152), some
mentions to some of the projects on the page, and it was done. I didn’t really
expect to hear much more.

Time passed. But not very much!

Well of course, the likes started coming. And then the retweets. And then the
pull requests. Within _literally_ an hour, I could see the site getting
traction. And, rather humbly, it was extremely surprising. After all, it was
just a list of links! But apparently the concept struck a chord, and perhaps a
lot of latent interest in the idea suddenly had a focus.

## Enter Yonatan

Evidently that interest was quickly going to outgrow my static web page. And as
if to make sure I got that point, I got a message from Yonatan
([@founderYonz](https://twitter.com/founderYonz)), a Harvard Business School
graduate who started using TinyBase after discovering my [local-first
talk](https://tripleodeon.com/2022/11/closing-the-gap-between-your-users-and-their-data)
@JavaScriptCon. The two of us had been chatting about creating a local-first
world. He spotted that it needed to become more of a human community with people
buying into the movement - especially if the goal was to raise awareness of the
local-first architecture across the industry as a whole.

And within a day, he leapt to action, and set up a [Discord
server](https://discord.gg/lfwdev) with the new logo, added a link to it from
the top of the site, and was busy welcoming and introducing all the new members
as they joined. He had people building apps, people building frameworks, people
who just wanted to hang out and chat about CRDTs and the like. The start of a
community!

Yonatan’s energy was infectious, and within just days, the ideas started
flowing. What about swag? What about a newsletter? What about a conference? We
agreed that the first step would be giving people a chance to get together, at
least online, and the first meetup was scheduled for February 28th.

## A tornado begins: the #lfw.dev community takes off

The first meetup, held in February, exceeded everyone’s expectations. Honored to
be joined by [Peter van Hardenberg](https://twitter.com/pvh) from Ink & Switch -
‘the father of local-first’ - and other speakers, the community heard kick-off
keynotes, deep dives into sync technologies, and a lengthy and rich Q&A session.

Since that first meetup, there have been three further blockbuster meetups, five
paper reading group sessions and ~700 members building, discussing and
sharing their passion for local-first. (In a follow on post, Yonatan will dig
into the work behind the LoFi community!)

But here’s my chance to say something very important. It doesn’t take on that
life of its own _on its own_. While my personal involvement has stayed
lightweight, the lion’s share of the community curation and leadership has been
squarely on Yonatan’s shoulders. While on one hand I am surprised at how quickly
things have grown, on the other, I shouldn’t be, knowing that it’s in his safe
and motivated hands. In case I don’t say it enough, I want to recognize how
awesome he has been in driving #lfw.dev forward.

## Onwards and upwards

Local-first as a movement still seems to be young. The principles are solid, the
enthusiasm is strong, and examples of it in use are appearing.

But there is a long way to go! There are still not as many local-first apps in
production as you might think, perhaps because they are still a little harder to
build - and the infrastructure to make that task easier is still being built
out.

But the demand is clearly there, both for applications that meet these ideals,
and certainly for this community of builders who want to make this happen. These
are people who are willing to question some of the assumptions of the current
status quo of web development, and who want to help shape a future of something
a little different.

And as for me? I’m proud of the fact that I built a web page that catalyzed
hundreds of people to come together to work on a shared vision. But it was just
a web page! And really the credit for where this community is today rests
squarely with other giants upon whose shoulders I merely wrote some HTML - and
to Yonatan in particular who has shown ceaseless energy and commitment in
getting things going.

Again, I’m reminded of Lorenz’s assertion about butterflies and tornados when I
think back on this series of extraordinary events from the last few months. A
web page flapped its wings, and, as others took the initiative and ran with it,
the resulting community tornado was a wonder to watch. Here’s to a local-first
future!

–

Want to know more and get involved? What better time to get involved than our
next meetup? We’ll see you there!

<a href="https://discord.gg/cVYugNvT?event=1102927548079423518"
    target="_blank"><img class="feature" src="/assets/images/meetup4.png" />
</a>
