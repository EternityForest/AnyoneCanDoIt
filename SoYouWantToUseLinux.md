# So you want to use Linux?

Here's what you should know!

## The Terminal

This is the one that scares new users the most, but the good news is, you can just ignore it.

The console is useful for many things.  The main thing is that a sequence of actions
can be written and shared with others,and another great feature is that you can log in
remotely over SSH.

Many claim that it is the best way to do almost anything, but I disagree.

The console is powerful, but it doesn't not watch your back.  Files deleted with rm are
truly deleted, not moved to trash.  Flashing a disk image to an SD card can overwrite your hard disk,
should you type the path of your main disk, not the external.

You will probably want to learn the terminal eventually, but it's
not any more necessary than it is on windows.

However, if you look around, you'll find many people doing things on the command line.
You may get the impression that there is no other way to do those things, but there usually is.

## Flashing a Live USB and trying it out

Linux can be installed, but it can also run straight from a USB stick, making no changes to the machine
This makes it very easy to safely try it out.  Everything works, but your changes and files dissappear when you
shut down, if you are in Live USB mode.

This is often used for people who want to do security stuff and leave no trace.

Generally, the installers and the live USB versions are exactly the same.  You boot, try it out,
and when you're ready to install, you click the installer on the desktop.

But first, you must flash the distro.  There are two good ways to do this: Etcher, and Multibootusb.

Just use Etcher for single distros, but check out multibootusb to pack two versions of Linux on one USB card.


## Hardware Support

It's generally pretty good.   Your biggest issue is likely to be with Nvidia graphics, or A few specific WiFi
drivers.  Test everything in live USB mode to ensure you can make it work!

## Distros 

There is not one single "Linux OS".  
People have made thousands of variants, called Distros.

The distro you choose will affect your experience *greatly*.  If you want the quick answer,
I'm going to say you should go download Kubuntu or Mint, and not spend too much time looking at the others.

The act of switching between them rapidly is known as distro hopping.  It's somewhere between a hobby, a meme,
an educational pursuit, and an addiction.  I wouldn't suggest doing too much of this!

Although there are thousands, the vast majority are not worth your time
In fact, you probably already know most of the ones that are.  Being free, anyone
Can make one, but very few people can make one well, as that takes an incredible amount of effort.


The biggest ones are mostly all variants of Ubuntu, itself a variant of Debian. If you're wondering what distro
to use and just want the easy one word answer, it's probably Kubuntu or Mint.

Do *not* trust DistroWatch.  They do not track what people are using, they track search
traffic.  You do not want the distros that people read about a lot!  The reliable ones being
used at home and in industry get a moderate and steady flow of traffic, people are too busy using
them to discuss details online.

Top DistroWatch distros are very likely to be the shiny new toy for distro hoppers, rather than
a solid and reliable platform.

### Arch 

This seems to be the most popular distro among enthusiasts. It
has no installer, you install yourself with a sequence of commands.  This is perfectly
fine, according to the fans.

It is not an easy distro.  It is advised that you read the forums before
updating any software, to be sure you don't break something.

It is loved for how much you learn while using it, and for it's up-to-data packages, but
that's not always a good thing.

You definitely *cannot* get by on this one without using the command line, although you probably can on
Manjaro.

#### Manjaro

This is built on Arch,but with a lot of things preconfigured. It
is easy enough for just about anyone, they say, but it still has some remnants
oof it's Arch heritage.


### Ubuntu Family (Ubuntu, Mint, Pop, Kubuntu)

This is what I would very strongly suggest.  Kubuntu has the
most full featured UI thanks to KDE Plasma, but you can install that later on others.


They are extremely popular, and designed for stability.

One notable thing is that they are fixed release.  Like windows,
there are versions that come out periodically.  With Arch, there is one
Arch that gets constant upgrades, so there is no true stable platfom.

The downside is that you will need to upgrade between fixed point. This is extremely easy if
you stick with LTS(Long Term Service) releases. Those are the ones generally suggested for most users.


There is of course, a chance that something breaks when upgrading, but
Arch can also break when upgrading packages.

### Rescue-oriented distros

There are many distros specifically meant to repair broken systems. It may be worth it
to have one, but Linux shouldn't break much.


## Systemd

This is probably the very biggest controversy in Linux, which is most likely completely irrelevant to you.
I only mention it here because of how often it comes up in discussion,  causing new users to think they need to avoid it.

What happened was a core piece of system software, known as sysvinit, was replaced with  systemd in most popular distros, about 5-10 years ago,
and a lot of people got angry.

The important thing to note is that most professional large scale users seem to love systemd.

But, if you want to be part of the community, it's important to understand the depths of
hate some people feel for it.

The big complaint is that it's too big.  Old school Linux fans
like software to be small, and assembled by the user to fit the application.

The other big complaint is security.  There was, and may still be, a few bugs, mostly patched in a hurry,
but the attitude of the dev team scared many.

The biggest one I can think of, is that configuring a service to autorun under a non-existent user's account,
resulted in that service running with full Admin privileges.

Fairly obscure, and the team has reasons for this, and systemd actually includes many security sandboxing features.

But to the "Keep a loaded gun in case the printer gains sentience" types, or anyone who's primary focus with Linux is security,
they may be uncomfortable with things like that, and doubly uncomfortable with the sometimes dismissive attitude of the devs.

Another issue is that some claim systemd was "forced" on them, because popular distros dropped support for non-systemd alternatives.

As of now, however, systemd free distros like Devuan still exist, although some are afraid there won't be enough interest to
maintain them indefinitely.  It takes more development resources to support more than one system, and standardization and consistency
was one of the main reasons people wanted to switch to systemd in the first place, so I find it hard to blame anyone for dropping support.

systemd has some major benefits.  It provides and integrated and standardized way to 
manage things, that were originally done by piecemeal assemblies of tools and scripts, and the majority
of people complaining about systemd just don't like anything large and Integrated.

Most people seem to like, or not mind it. It most likely will have no effect on your experience as a normal user.
Even Arch, the premier tinkerers and DIYers distro, accepts it.

But if you really want to do something else, there are alternatives.


