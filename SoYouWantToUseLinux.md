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


## Desktops

On Linux, everything you see on the screen is normally provided by the Desktop Environment.  When you install Linux, the DE is usually included, but can be freely swapped out, like changing the launcher on Android.

There are really only three DEs I would suggest bothering with. KDE, Cinnamon, and Gnome.


KDE is windows-like, very easy, and extremely customizable.  It would be my top suggestions for most, although you may need to install it yourself from the "app store" if your chosen distro doesn't come with it. It is included with Kubuntu.

Cinnamon is similar, but simplified and missing some features. It's included with Mint, and is honestly probably good enough for most.

GNOME is a bizzare mashup of Android and maybe MacOS inspired design, that apparently has good touchscreen and accessibility support for those with disabilities, but I would otherwise stay away.  It comes with vanilla Ubuntu.


## Distros

As a free OS, there are many versions and variants available based on the core Linux Kernel, called distros.

The act of switching between them rapidly is known as distro hopping, somewhere between a hobby, educational experience, and addiction.  I'd suggest not doing too much of this.

Although there are thousands, the vast majority are not worth your time.

In fact, you probably already know most of the ones that are. Being free, anyone
Can make one, but very few people can make one well, as that takes an incredible amount of effort.


The biggest ones are mostly all variants of Ubuntu, itself a variant of Debian. If you're wondering what distro
to use and just want the easy one word answer, it's probably Kubuntu or Mint.

Do *not* trust DistroWatch. They do not track what people are using, they track search
traffic. 

You do not want the distros that people read about a lot! The reliable ones being
used at home and in industry get a moderate and steady flow of traffic. People are too busy using
them to discuss details online, and they rarely break, so the support forums may look quiet.

Top DistroWatch distros are very likely to be the shiny new toy for distro hoppers, rather than
a solid and reliable platform.

The other important thing about distros is that almost none of them are truly limited.  They can all do just about anything Linux can do.  The big difference is in community support, and in how much is preconfigured.

There's no need to "Graduate" from the easy distros, even for professional users.


### Ubuntu Family 
Kubuntu, Mint, Pop!_os,  and KDE Neon are all perfectly good.

Coming from windows, you won't find any surprises.

They use fixed point releases, meaning there are discrete versions, like windows, that recieve updates for a time, and then are deprecated, and you must upgrade.

This upgrade process is usually painless, but has a chance to go wrong, just like it does on Windows.

The advantage is much greater consistency.  The fixed releases are stable platforms for developers, not moving targets, and the goal is that things break far less, even if you forget to update for a long time.

#### Snap Packages 
The major complaint is the use of Snap packages for many things on Ubuntu and Kubuntu, but not as much on most of the derivatives.

Snap packages are a new way of distributing software, heavily pushed by Canonical, Ubuntu's company.

Snap packages use a lot of storage space, and have an automatic update feature that you can't disable.   But most things, with the exception of the Chromium browser, are still non-snapped.

Chrome itself is still non-snapped, if you are fine with using Google's proprietary browser.


In practice, it's mostly fine.   Auto updates download in the background, and the switch is  near instant, so you likely won't see any big issues.  There's even a new feature that disables updates while apps are running.


But it is something to keep in mind, especially as the app stores and even command line tools, if you choose them, will install snaps for you when you expect traditional packages, for certain apps.


Of course, the advantage of all this, is that you get up to date packages in a much more reliable format, because packages include everything they need, and you don't run into compatibility issues with other packages.

I would personally be totally in favor of snaps, if they would open source the snap server code, and allow us to disable auto-update.

As is, I'd suggest not purposely going out of your way to use snaps, and to consider using  Mint or Pop!.

#### Arch and Manjaro 

Arch seems to be the most popular distro among enthusiasts.  They promote them heavily, but this is NOT an easy distro. It doesn't even include an installer!

They even recommend reading forums before installing updates, so you don't break things.  They also recommend you definitely don't forget to update for too long, or you may face problems when you finally do.

Even it's consumer friendly derivative Manjaro may not be as easy as others, although it is said to be perfectly usable for non-technical people.  I still don't trust the reliability quite as much.

The reason is the rolling release.  New packages are delivered continually, and with more frequent updates, leading to less testing happening before you get the software.  More changes means less predictability, but more features.

## The Software 

The best part about Linux is all the great software!

Linux allows downloading from the internet, like windows, or installing from trusted repositories through an app store or command line.

For the most secure experience, use the trusted repos!

Here's some free apps you should know, most of which you can pick up and use without reading the manual:

Programming: VS Code
Image Editing: Krita or Gimp
Sync Files between machines: SyncThing

Make backups: Back in Time
Spreadsheet, word processor: LibreOffice

3D Modeling: Blender
CAD: RealThunder's FreeCad variant Assembly3

PCB Design: LibrePCB



## Dual Booting 

You can have Windows and Linux on one machine.  But Windows may break Linux.  You won't lose files, but you'll need to repair the boot info on your disk, and it will be annoying.


## The UNIX philosphy 

If you hand out with older Linux users, you'll hear this a lot.  Basically, it means that programs should be small and easily connected by the user as needed on the command line, rather than large premade apps that handle your entire workflow.

It is, of course, a philosphy, and opinions vary on whether it is useful.  I personally do not believe in it at all, but many will throw it around as an unqualified, absolute good.

## Systemd

One thing to be aware of is the controversy surrounding systemd.  Systemd replaced sysvinit, a core bit of system software, in most Linux distros.

The important thing to note is that the big players overwhelmingly choose systemd. The people who hate it are a significant, but small minority.


There were a few security issues, as with any software, which got resolved.

Some people take offense to what they see as the developer's dismissive attitude.

Most just don't like that it's large and Integrated. They see it as being too much like Windows, not following the UNIX philosphy, etc.

Some also feel it was "forced on them", because large companies don't want to spend the resources to keep support for sysvinit, and they frame it as an issue of freedom.

As I see it, they really aren't obligated to maintain support for something very few people want, and there are in fact, several community supported distros for systemd-haters.

You can probably safely ignore any and all discussions of, or related to, systemd, unless you are developer.

I personally think systemd is one of the best things to happen to Linux in decades, and I wouldn't touch a distro without it.
