---
title: Some Thoughts On Operating Systems
published_at: December 26, 2014 4:00 PM
updated_at: December 26, 2014 4:00 PM
---

I've run [FreeBSD](https://www.freebsd.org/), [OpenBSD](https://www.openbsd.org/), many Linuxs, and OSX at various times in my life. I was fortunate enough to get into computers late, late enough that Linux had already taken over the minds of my friends, and I more or less skipped Windows.

## Starting

The thing that got me into computers to begin with was the web. I wanted to build web pages for my band, [Counterfit](http://en.wikipedia.org/wiki/Counterfit). I sort of understood the Internet to be Aol and mp3's. I wanted to meet as many punks as I could and I wanted them to hear my band, so I started learning how to make web pages. It wasn't long before I learned about servers and then Unix. I couldn't play with Solaris, but I could download Linux for free. It was my crappy car version of the expensive stuff and I loved it.

Most people I knew that were into computers thought Linux was great, but I had one friend, who seemed to know everything, advocating FreeBSD instead. I switched to FreeBSD and from there learned about the long history of the System V and BSD unixs that eventually evolved in 1998's Solaris and FreeBSD. The system was amazingly solid too, so instead of feeling like I was in a crappy car, I thought I was on some new kind of high speed train that hadn't gone mainstream yet.

## So Many Ways To Think

Operating systems were both fascinating and full of combat. All my opinions were right and wrong all the time and I hardly knew enough to defend any of them. I just wanted to make the computer that my band's website ran on. Not just the code, but the whole machine and OS.

I eventually just became the kind of person who'll try anything. My willingness to try anything sometimes leads me down paths that don't produce any new ideas, but I don't mind. From time to time, you find fascinating stuff, making all the time you put in worthwhile.

There was so much choice at the user interface level. It blew my mind. I was known to flip flop on Window Managers often, too. From [Window Maker](http://windowmaker.org/) to [Gnome](http://www.gnome.org/) to [Afterstep](http://www.afterstep.org/) to [Blackbox](http://xwinman.org/blackbox.php) to [KDE](https://www.kde.org/) to [XFCE](http://www.xfce.org/)... everything.

I didn't so much care what someone's opinion was. I wanted to experience any points in thinking where someone had an opinion. Go figure, That leads to trying lots of different OSs, as many features are done at the OS-level. So many great ideas, all free! [PF in OpenBSD](http://www.openbsd.org/faq/pf/), [jails in FreeBSD](https://www.freebsd.org/doc/handbook/jails.html), [Docker containers in CoreOS](https://coreos.com/using-coreos/docker/), etc.

## Progress Can Be Unstable

One of the benefits of the Linux model is that it's a wild, wild west. Lots of ideas get tried quickly and, as a result, things are sometimes unstable. Maybe a fundamental change happens and, just like that, things are permanently different.

FreeBSD was a place that didn't take many chances. They wanted the system to be as stable as possible, no compromises. Of course, they'd watch what the other systems were doing and bring back any ideas they liked, done their way. They replaced their packet filter with OpenBSD's, introduced Jails, and then... Apple hired away a bunch of the core developers to work on OSX instead, which itself was built out of FreeBSD.

Ouch. FreeBSD was going to be significantly stalled while they figure out how to replace half the team. No OS was safe from disruption.

I really liked FreeBSD, but for my laptop I wanted something that supported all my media too. Basically, the experimentation would continue, server-side, but I wanted my laptop to just be one system for a long time. The best answer back then was Ubuntu Linux.

## Apple On My Desk

Ubuntu was mostly fine. It was annoying to use it for watching DVDs. Music software my friends were starting to use wasn't supported. But it was close enough to the servers I ran that I could use it for work.

And then came Apple's new OS. I had already become the kind of person who wants stability on whatever machine is my HQ and OSX was new, so I didn't jump in right away. I was, however, pretty into the idea that a Mac would offer a single, great window manager, support all my media in a sensible way, and put a lot of energy behind it.

Mac's became my main machine once I hooked my guitar up to my laptop with Garageband. Mac's are great. I still use them for my main workstation. Garageband is there too and I use it all the time. I run all the same software I used on Linux, like Vim, Emacs, Postgres, Python, etc.

I lost interest in the Linux desktop wars a while ago. I basically just live in a Terminal, so the rest almost doesn't matter. In other words, the arguments that used to compel me to use Linux over a proprietary system just don't sway me the way they used to.

## Apple In My Pocket

Things are different in almost-2015. I've been an OSX user and an iPhone user for a long time now. I get that 10% of the mobile users use iOS, but all of my friends are in that 10%.

I look at iOS as BSD for mobile. It's solid. Apps are added to the app store (bsd users, read: ports library) unless they're rejected for not working well. Advocates of the open models hate this, but I think a typical user appreciates having Apple rejecting the riff-raff.

Android, on the other hand, is very much a wild, wild west. Anything goes. And because of that, it's gaining the most features and moving very fast across different hardware. The developer experience is fragmented, just like it was back on Linux. The software's compatibility is fragmented, just like it was on Linux. Android, as a whole, feels the same to me as when I ran Linux on my desktop.

What I want is the BSD experience. The one that is stable, the software works, and I can trust it to be my rock. I know there are reasons to use Linux, I just don't want them in my pocket.

## Linux On My Servers

I am happy to say that after 15 years of being a Linux user, in some form or another, the progress has been relentless. The infrastructure world is being turned inside-out right now by the proliferation of Docker, which lead to CoreOS. CoreOS is a new Linux that changed things dramatically in a way I really love, so I've been using that when I setup new servers. It's a similar experience to FreeBSD jails, but taken to an extreme. And it's aweeeesssomeeee.

Linux's progress is relentless. They'll try just about anything to see what happens.

## Stable Life, Progressive Code

There's a theme to this story. I want my personal experience of computing to be solid. And I want as much progress as possible, just not in my pocket.
